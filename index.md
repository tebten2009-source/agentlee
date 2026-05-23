---
layout: default
title: Home
---

# {{ site.title }}

## 최신 공지

<ul>
{% for post in site.posts limit:5 %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <small>{{ post.date | date: "%Y-%m-%d" }}</small>
  </li>
{% endfor %}
</ul>

[전체 공지 보기](/_posts/)
