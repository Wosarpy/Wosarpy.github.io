---
layout: page
title: Posts
---

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%B %d, %Y" }}

{{ post.excerpt }}

{% endfor %}

<div class="comments">
  <script src="https://giscus.app/client.js"
    data-repo="Wosarpy/Wosarpy.github.io"
    data-repo-id="R_kgDOTcljPQ"
    data-category="Announcements"
    data-category-id="DIC_kwDOTcljPc4DBmWJ"
    data-mapping="specific"
    data-term="{{ page.slug }}"
    data-strict="1"
    data-reactions-enabled="0"
    data-input-position="bottom"
    data-theme="light"
    data-lang="en"
    crossorigin="anonymous"
    async>
  </script>
</div>
