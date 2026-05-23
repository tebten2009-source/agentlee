---
layout: default
title: 공지사항
permalink: /blog/
---

<h1>📋 공지사항</h1>

<ul style="list-style: none; padding: 0;">
{% for post in site.posts %}
  <li style="margin-bottom: 15px; padding: 15px; background: #e8f5e9; border-radius: 8px; border-left: 4px solid #009688;">
    <a href="{{ post.url }}" style="font-size: 1.1rem; font-weight: bold; color: #2c3e50; text-decoration: none;">{{ post.title }}</a>
    <br>
    <small style="color: #7f8c8d;">{{ post.date | date: "%Y년 %m월 %d일" }} · {{ post.categories | join: ", " }}</small>
  </li>
{% endfor %}
</ul>

<p style="margin-top: 30px;">
  <a href="/" style="color: #009688;">← 메인 대시보드로 돌아가기</a>
</p>
