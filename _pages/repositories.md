---
layout: page
permalink: /repositories/
title: repositories
description: |
  Most of my professional software engineering work has happened either outside GitHub or in private repos.
  Below are some of my public GitHub repos.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub activity information

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

{% endif %}
