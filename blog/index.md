---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

## Blog Posts

{% for page in site.pages %}
  {% if page.path contains 'blog/' and page.path != 'blog/index.md' %}
    <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork">
      <h2 class="archive__item-title" itemprop="headline">
        <a href="{{ page.url | relative_url }}" rel="permalink">{{ page.title }}</a>
      </h2>
      <p class="page__meta"><i class="far fa-clock" aria-hidden="true"></i> {{ page.date | date: "%B %d, %Y" }}</p>
      {% if page.excerpt %}<p class="archive__item-excerpt" itemprop="description">{{ page.excerpt | markdownify | strip_html | truncate: 160 }}</p>{% endif %}
    </article>
  {% endif %}
{% endfor %}
