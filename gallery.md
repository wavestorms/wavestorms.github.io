---
layout: default
title: Gallery
permalink: /gallery/
---

<h1>Image Gallery</h1>
<div class="gallery-grid">
  {% for item in site.data.gallery %}
    <div class="thumb">
      <a href="/gallery/{{ item.id }}/">
        <img src="{{ item.thumb }}" alt="{{ item.title }}">
        <p>{{ item.title }}</p>
      </a>
    </div>
  {% endfor %}
</div>

<style>
.gallery-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}
.thumb {
  width: 200px;
  text-align: center;
}
.thumb img {
  width: 100%;
  height: auto;
}
</style>

