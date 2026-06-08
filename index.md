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

### Страницы:
<ul>
  {% for page in site.pages %}
    {% if page.title and page.permalink != '/' %}
      <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

