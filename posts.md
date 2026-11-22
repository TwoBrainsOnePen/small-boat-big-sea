---
layout: page
title: 全部文章
lang: zh
permalink: /posts/
---

{% assign lang_posts = site.posts | where: "lang", "zh" %}
{% if lang_posts.size > 0 %}
<ul>
  {% for post in lang_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}</li>
  {% endfor %}
</ul>
{% else %}
还没有发布的文章。第一批正在准备中。
{% endif %}
