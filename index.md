---
layout: default
title: 主页
---

# 你好
这里是我的安全研究与技术笔记站点，记录漏洞分析、系统机制、逆向与工程实践。

## 最近文章
{% if site.posts and site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts limit: 10 %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="muted">{{ post.date | date: "%Y-%m-%d" }}</span>
  </li>
  {% endfor %}
</ul>
<p class="muted"><a href="{{ '/posts/' | relative_url }}">查看全部文章 →</a></p>
{% else %}
<p class="muted">暂时还没有文章。你可以在 <code>_posts/</code> 下创建第一篇。</p>
{% endif %}
