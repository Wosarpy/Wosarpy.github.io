---
layout: page
title: Posts
---

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%B %d, %Y" }}

{{ post.excerpt }}

{% if page.comments %}
  {% include comments.html %}
{% endif %}

{% endfor %}
