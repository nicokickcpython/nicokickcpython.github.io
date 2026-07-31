---
layout: default
title: 技术博客
---

<section class="home-hero">
  <h1>{{ site.title }}</h1>
  <p>{{ site.description }}</p>
</section>

<section class="post-list">
  {% for post in site.posts %}
  <a class="post-card" href="{{ post.url }}">
    <h2>{{ post.title }}</h2>
    {% if post.excerpt %}
    <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    {% endif %}
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
  </a>
  {% endfor %}
</section>
