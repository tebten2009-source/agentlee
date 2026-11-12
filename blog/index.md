---
layout: default
title: 마음공부 게시판
permalink: /blog/
---

<style>
  .mind-board { max-width: 900px; margin: 2.5rem auto 4rem; padding: 0 1.25rem; color: #243247; }
  .mind-board-header { padding: 2rem 0 1.5rem; border-bottom: 1px solid #dce3ec; margin-bottom: 1.5rem; }
  .mind-board-label { margin: 0 0 .5rem; color: #9a7820; font-size: .85rem; font-weight: 700; letter-spacing: .08em; }
  .mind-board h1 { margin: 0 0 .75rem; color: #1e3a5f; font-size: 2rem; line-height: 1.35; }
  .mind-board-intro { max-width: 680px; margin: 0; color: #526174; line-height: 1.8; }
  .mind-post-list { display: grid; gap: 1rem; margin: 0; padding: 0; list-style: none; }
  .mind-post-card { padding: 1.35rem 1.5rem; border: 1px solid #e0e6ee; border-left: 4px solid #c9a227; border-radius: 12px; background: #fff; box-shadow: 0 5px 18px rgba(30, 58, 95, .05); }
  .mind-post-title { color: #1e3a5f; font-size: 1.2rem; font-weight: 700; line-height: 1.55; text-decoration: none; }
  .mind-post-title:hover, .mind-post-read:hover { text-decoration: underline; }
  .mind-post-meta { margin-top: .4rem; color: #68778a; font-size: .88rem; }
  .mind-post-excerpt { margin: .8rem 0 .65rem; color: #465568; line-height: 1.8; }
  .mind-post-read { color: #315b87; font-size: .92rem; font-weight: 700; text-decoration: none; }
  .mind-board-back { display: inline-block; margin-top: 2rem; color: #315b87; font-weight: 600; text-decoration: none; }
  @media (max-width: 600px) { .mind-board { margin-top: 1.25rem; } .mind-board h1 { font-size: 1.65rem; } .mind-post-card { padding: 1.1rem; } }
</style>

<main class="mind-board">
  <header class="mind-board-header">
    <p class="mind-board-label">마음을 살펴보는 글</p>
    <h1>마음공부 게시판</h1>
    <p class="mind-board-intro">일상에서 만나는 마음의 움직임과 알아차림의 연습을 함께 살펴봅니다. 새 글은 이 목록에 차례로 추가됩니다.</p>
  </header>

  <ul class="mind-post-list">
    {% for post in site.categories["마음공부"] %}
    <li class="mind-post-card">
      <a class="mind-post-title" href="{{ post.url }}">{{ post.title }}</a>
      <div class="mind-post-meta">{{ post.date | date: "%Y년 %m월 %d일" }} · {{ post.categories | join: ", " }}</div>
      <p class="mind-post-excerpt">{{ post.excerpt | strip_html | strip_newlines | truncate: 180 }}</p>
      <a class="mind-post-read" href="{{ post.url }}">글 읽기 →</a>
    </li>
    {% endfor %}
  </ul>

  <a class="mind-board-back" href="/">← 홈페이지로 돌아가기</a>
</main>
