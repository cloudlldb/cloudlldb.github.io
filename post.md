---
layout: default
title: 文章
permalink: /posts/
---

# 文章

{% if site.posts and site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li class="post-row">
    <div class="post-row-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>
    <div class="post-row-meta muted">
      {{ post.date | date: "%Y-%m-%d" }}
      {% if post.tags %}
        ·
        {% for tag in post.tags %}
          <span class="tag">{{ tag }}</span>
        {% endfor %}
      {% endif %}
    </div>
    {% if post.excerpt %}
      <div class="post-row-excerpt muted">{{ post.excerpt | strip_html | truncate: 140 }}</div>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="muted">暂无文章。</p>
{% endif %}
