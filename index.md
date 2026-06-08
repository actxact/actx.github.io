---
layout: default
title: "Main"
permalink: /
---

<style>
  /* Локальные стили для создания медитативной, книжной атмосферы */
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Georgia, Garamond, serif;
    line-height: 1.8;
    color: #2c3e50;
    background-color: #fcfcf9; /* Мягкий бумажный оттенок */
    max-width: 650px;
    margin: 40px auto;
    padding: 0 20px;
  }
  
  header {
    margin-bottom: 60px;
  }
  
  .motto {
    font-style: italic;
    color: #7f8c8d;
    font-size: 0.95em;
    letter-spacing: 0.05em;
    word-spacing: 0.1em;
  }

  .motto span {
    transition: color 0.3s ease;
  }
  .motto span:hover {
    color: #2c3e50;
  }

  h2 {
    font-weight: 400;
    font-size: 1.4em;
    margin-top: 40px;
    color: #34495e;
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
  }

  ul.posts-list {
    list-style: none;
    padding: 0;
    margin: 20px 0;
  }

  ul.posts-list li {
    margin-bottom: 18px;
    display: flex;
    justify-content: space-between;
    align-items: baseline;
  }

  ul.posts-list li a {
    color: #2980b9;
    text-decoration: none;
    border-bottom: 1px transparent;
    transition: all 0.2s ease;
  }

  ul.posts-list li a:hover {
    color: #c0392b; /* Акцент благородного увядания */
    border-bottom: 1px solid #c0392b;
  }

  .post-date {
    font-size: 0.85em;
    color: #95a5a6;
    font-family: monospace;
    white-space: nowrap;
    margin-left: 20px;
  }

  .nav-links {
    margin-top: 60px;
    font-size: 0.9em;
  }
  
  .nav-links a {
    color: #7f8c8d;
    text-decoration: none;
    margin-right: 15px;
  }
  .nav-links a:hover { color: #2c3e50; }
</style>

<header>
  <p class="motto" style="font-size: 0.85em; text-transform: uppercase; letter-spacing: 0.1em;">
    Writing is good, thinking is better. <br>
    Cleverness is good, patience is better.
  </p>
</header>


## Хроника наблюдений

<ul class="posts-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="post-date">{{ post.date | date: "%Y &middot; %m &middot; %d" }}</span>
    </li>
  {% endfor %}
</ul>

{% if site.posts.size == 0 %}
  <p style="font-style: italic; color: #95a5a6;">Мир замер в ожидании первой мысли...</p>
{% endif %}

---

<div class="nav-links">
  <a href="{{ '/about/' | relative_url }}">Кто здесь?</a>
  <a href="{{ '/feed.xml' | relative_url }}" target="_blank">RSS</a>
</div>
