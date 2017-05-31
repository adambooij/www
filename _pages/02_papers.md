---
layout: page
title: Working Papers
permalink: /papers/
---

<ul>
{% assign items = site.categories.papers | sort: 'date' %}
{% for post in items reversed %}
	<li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
	{% if post.authors != site.name %}
<<<<<<< HEAD
	{% assign and_name = site.name : append ' and' %}
	{% assign name_and = 'and ' append : site.name %}
	({{ post.authors | strip_newlines | remove: and_name | remove: name_and | prepend: 'with ' }})
=======
	({{ post.authors | strip_newlines | remove: 'Adam S. Booij and' | remove: 'and Adam S. Booij' | prepend: 'with ' }})
>>>>>>> f59f32992e6f4aed804b8d1fd24d0e8de76db030
	{% endif %}
	</li>
{% endfor %}
</ul>
