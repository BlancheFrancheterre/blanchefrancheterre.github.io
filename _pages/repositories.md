---
layout: page
permalink: /repositories/
title: Repositories
description: Pinned repositories.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_repos.size > 0 %}

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
      <div class="card h-100 p-3 repo-card-horizontal">
        <img src="/assets/img/monique_logo.png" alt="Monique logo" class="repo-logo" />
        <div class="repo-card-text">
          <h5 class="card-title">Monique</h5>
          <p class="card-text">R package for joint network inference across conditions, including DSNS.</p>
          <span class="repo-link">forge.inrae.fr/blanche.francheterre/monique</span>
        </div>
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
