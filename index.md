# 你好，我是 XXX
这里是我的个人博客。

## 最新文章
{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})（{{ post.date | date: "%Y-%m-%d" }}）
{% endfor %}

