---
layout: default
title: Gallery
permalink: /gallery/
---

<h1>Image Gallery</h1
<h2>Here you will find pictures and schematic made by members of the WAVESTORMS team. Feel free to re-use them for presentations, lectures, etc, with appropriate credits, listed on each image's page.</h2>
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

