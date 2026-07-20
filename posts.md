---
layout: page
title: Posts
---

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%B %d, %Y" }}

{{ post.excerpt }}

{% endfor %}

<script src="https://giscus.app/client.js"
        data-repo="Wosarpy/Wosarpy.github.io"
        data-repo-id="R_kgDOTcljPQ"
        data-category="Announcements"
        data-category-id="DIC_kwDOTcljPc4DBmWJ"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="bottom"
        data-theme="light"
        data-lang="en"
        crossorigin="anonymous"
        async>
</script>
