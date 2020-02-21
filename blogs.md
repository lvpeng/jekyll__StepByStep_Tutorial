---
layout: default
title: Blogs 
tag: tag1
---
<ul>
{% for post in site.posts %}
	<li>
		<h2><a href="{{post.url}}"> {{post.title}} </a></h2>
		<p>{{post.excerpt}}</p>
		<p>{{post.date | date_to_string  }} categories: {{post.categories}}</p>
		{%if page.tags %}
			<p>tags: {{page.tags}} </p>
		{% endif %}
	</li>
{% endfor %}
</ul>
