---
layout: default
title: "think wait fast"
---

### Список:

<ul>
  {% for post in site.posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%d.%m.%Y" }}</span> — 
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
