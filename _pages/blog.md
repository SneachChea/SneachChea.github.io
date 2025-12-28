---
layout: single
title: Blog
permalink: /blog/
---

Welcome to my blog! Here, I share my thoughts, experiences, and discoveries on various topics. Feel free to explore the articles below.


<ul>
{% for post in site.posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}
  <p>{{ post.excerpt }}</p>
  </li>
{% endfor %}
</ul>
