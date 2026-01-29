---
layout: default
title: Sculptures
permalink: /sculptures/
---

<header class="hero">
  <h1>Sculptures</h1>
  <p class="subtitle">A curated selection of sculptures</p>
</header>

<div class="grid">
{% assign sculpture_works = site.artworks | where:"category","Sculptures" %}
{% for work in sculpture_works %}
  <a href="{{ work.url }}" class="grid-item">
    {% if work.image %}
      <img src="{{ work.image }}" alt="{{ work.title }}">
    {% elsif work.images %}
      <img src="{{ work.images[0] }}" alt="{{ work.title }}">
    {% endif %}
    <div class="overlay">
      <span>{{ work.title }}</span>
    </div>
  </a>
{% endfor %}
</div>
