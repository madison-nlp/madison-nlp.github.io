---
layout: default
title: "Welcome to Madison NLP"
---

<div class="hero">
  <div>
    <h1 class="mb-2">{{ site.title }}</h1>
    <p class="lead mb-3">{{ site.description }}</p>

    <p>We are a community of faculty and students at the University of Wisconsin–Madison interested in natural language processing, machine learning, and artificial intelligence.</p>

    <p>Across our research groups, we explore how machines can understand, generate, and reason with language, and how language technologies can better serve people across different communities, cultures, and applications.</p>

    <p>Madison NLP is a place for collaboration, learning, and exchanging ideas. Explore our members, research, and courses to learn more about what’s happening in NLP at UW–Madison.</p>

  </div>

<div class="carousel-frame">
  <div id="labCarousel"
     class="carousel slide"
     data-bs-ride="carousel"
     data-bs-interval="3000">

    <div class="carousel-inner">
      {% for photo in site.data.carousel %}
      <div class="carousel-item{% if forloop.first %} active{% endif %}">
        <img
          src="{{ site.baseurl }}/{{ photo.image }}"
          class="d-block w-80 carousel-img"
          alt="{{ photo.alt | default: photo.caption | default: 'Lab photo' }}"
        />
        {% if photo.caption and photo.caption != "" %}
          <div class="carousel-caption d-none d-md-block">
            <p class="mb-0">{{ photo.caption }}</p>
          </div>
        {% endif %}
      </div>
      {% endfor %}

    </div>

    <button class="carousel-control-prev" type="button" data-bs-target="#labCarousel" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#labCarousel" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</div>
