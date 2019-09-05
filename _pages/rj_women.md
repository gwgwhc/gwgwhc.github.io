---
title: Women of Rajasthan
layout: default
description: oh yeah, can do!
type: project
order: 4
---

<div class="section main">
	<div class="container">
		<div class="row">
			{% assign k = page.name.size | minus: 3 %}
			{% assign n = page.name | slice: 0, k %}
			{% assign coll = site.collections | where: "label", n | first %}
			{% assign l = coll.files.size | divided_by: 2 | ceil %}
			<div class="one-half column">
				{% for image in coll.files limit: l %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ '/' | append: coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>
			<div class="one-half column">
				{% for image in coll.files offset: l %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ '/' | append: coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>
		</div>
	</div>
</div>
<div id="Fullscreen">
	<img src="" alt="" />
</div>