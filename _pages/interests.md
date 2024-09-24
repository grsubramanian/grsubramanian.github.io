---
layout: page
title: interests
permalink: /interests/
description: A collection of my interests and some relevant links
nav: true
nav_order: 3
horizontal: true
---

<!-- pages/interests.md -->
<div class="interests">

{% assign sorted_interests = site.interests | sort: "importance" %}

<!-- Generate cards for each interest -->
{% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for interest in sorted_interests %}
      {% include interests_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
{% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for interest in sorted_interests %}
      {% include interests.liquid %}
    {% endfor %}
  </div>
{% endif %}
</div>
