---
layout: page
permalink: /blog/
title: blog
description: 
nav: true
nav_order: 1
---

<div class="post">
  <ul class="post-list">
    {% for post in site.posts %}
    <li>
      {% if post.pdf_link %}
      <a href="{{ post.pdf_link }}" target="_blank" rel="noopener noreferrer" onclick="window.open(this.href, '_blank'); return false;" style="text-decoration: none; color: inherit; display: block; cursor: pointer;">
      {% else %}
      <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: inherit; display: block;">
      {% endif %}
        {% if post.thumbnail %}
        <div class="row">
          <div class="col-sm-3">
            <img class="card-img" src="{{ post.thumbnail | relative_url }}" style="object-fit: cover; height: 100%; border-radius: 5px;" alt="{{ post.title }}">
          </div>
          <div class="col-sm-9">
        {% endif %}
            <h3 class="post-title">{{ post.title }}</h3>
            <p>{{ post.description }}</p>
            <p class="post-meta">
              {{ post.date | date: '%B %d, %Y' }}
            </p>
        {% if post.thumbnail %}
          </div>
        </div>
        {% endif %}
      </a>
    </li>
    {% endfor %}
  </ul>
</div>
