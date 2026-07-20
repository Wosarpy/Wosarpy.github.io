---
layout: default
title: Blog
---

# Blog Posts

{% if site.posts.size == 0 %}
No posts found.
{% endif %}

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})
{{ post.date | date: "%Y-%m-%d" }}

{{ post.excerpt }}

{% endfor %}
