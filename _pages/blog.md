---
layout: single
title: Blog
permalink: /blog/
---

Welcome to my blog! Here, I share my thoughts, experiences, and discoveries on various topics. Feel free to explore the articles below.


<style>
.blog-list {
  list-style: none;
  padding: 0;
}
.blog-list li {
  margin-bottom: 2em;
  text-align: center;
}
.blog-list img {
  display: block;
  margin: 0 auto 0.5em auto;
}
</style>
<ul class="blog-list">
{% for post in site.posts %}
<li>
  {% if post.teaser %}
    <img src="{{ post.teaser }}" alt="Thumbnail for {{ post.title }}" style="width:80px;height:auto;">
  {% endif %}
  <a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}
  <p>{{ post.excerpt }}</p>
  <hr style="margin:2em auto;width:60%;border:0;border-top:1.5px solid #ccc;">
</li>
{% endfor %}
</ul>
