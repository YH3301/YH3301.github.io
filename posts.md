---
layout: default
title: Posts
permalink: /posts/
---

## Posts
Assorted posts, ramblings, short notes, and updates.

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%b %-d, %Y" }}
{% endfor %}