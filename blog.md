---
layout: default
title: Blog
---

# Latest Thoughts

<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item">
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h2 class="post-title">
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
