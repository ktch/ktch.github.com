---
layout: blog
---

{% for post in site.posts %}

<h1>{{ post.title }}</h1>

{{ post.content }}

{% endfor %}