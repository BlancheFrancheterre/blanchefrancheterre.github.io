---
layout: page
permalink: /repositories/
title: Repositories
description: GitHub profile and pinned repositories.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

## GitLab repositories

<!--
  Hosted on forge.inrae.fr (GitLab), so they can't use the GitHub-only cards
  above (repo.liquid hardcodes github.com and an external GitHub-stats API).
  This is a hand-built equivalent using the site's own .card component
  instead, styled via the "other-repos" rules in _sass/_themes.scss.
-->
<div class="repositories other-repos d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <div class="repo p-2">
    <a href="https://forge.inrae.fr/blanche.francheterre/monique">
      <div class="card h-100 p-3">
        <img src="/assets/img/monique_logo.png" alt="Monique logo" class="repo-logo" />
        <h5 class="card-title">Monique</h5>
        <p class="card-text">R package for joint network inference across conditions, including DSNS.</p>
        <span class="repo-link">forge.inrae.fr/blanche.francheterre/monique</span>
      </div>
    </a>
  </div>
  <div class="repo p-2">
    <a href="https://forge.inrae.fr/blanche.francheterre/dsns_paper_simulations">
      <div class="card h-100 p-3">
        <h5 class="card-title">DSNS paper simulations</h5>
        <p class="card-text">Simulation code for "Data Shared Neighbourhood Selection for multi-condition network inference."</p>
        <span class="repo-link">forge.inrae.fr/blanche.francheterre/dsns_paper_simulations</span>
      </div>
    </a>
  </div>
</div>
