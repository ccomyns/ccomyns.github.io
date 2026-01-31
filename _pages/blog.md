---
layout: page
permalink: /blog/
title: blog
description: 
nav: true
nav_order: 1
---

<div class="post">
  <h1>blog</h1>
  
  <ul class="post-list">
    {% for post in site.posts %}
    <li>
      <h3>
        <a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p>{{ post.description }}</p>
      <p class="post-meta">
        {{ post.date | date: '%B %d, %Y' }}
      </p>
    </li>
    {% endfor %}
  </ul>
</div>
