---
layout: page
title: All Posts
permalink: /en/posts/
---

{% assign lang_posts = site.posts | where: "lang", "en" %}
{% if lang_posts.size > 0 %}
<ul>
  {% for post in lang_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>
{% else %}
No posts published yet. The first batch is still being prepared.
{% endif %}
