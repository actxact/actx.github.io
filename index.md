---
layout: default
title: "Мой Дневник"
---

# Добро пожаловать в мой дневник!

Здесь собраны все мои записи:

<ul>
  {% for post in site.posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%d.%m.%Y" }}</span> — 
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
