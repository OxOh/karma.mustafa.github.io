---
layout: default
title: Paintings
permalink: /paintings/
---

<header class="hero">
  <h1>Paintings</h1>
  <p class="subtitle">A curated selection of paintings</p>
</header>

<div class="grid">
{% assign painting_works = site.artworks | where:"category","Paintings" %}
{% for work in painting_works %}
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
