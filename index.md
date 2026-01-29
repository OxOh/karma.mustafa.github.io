---
layout: default
---

<header class="hero">
  <h1>Karma Mustafa</h1>
  <p class="subtitle">Paintings & Sculptures</p>
</header>
<div class="grid">
{% for work in site.artworks %}
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

