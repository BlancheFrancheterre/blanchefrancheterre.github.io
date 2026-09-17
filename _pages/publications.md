---
layout: page
permalink: /publications/
title: Publications
description: publications in reversed chronological order.
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<h2>Preprints</h2>
{% bibliography --query "@*[category=preprint]" %}

<h2>Publications</h2>
{% bibliography --query "@*[category=publication]" %}

<h2>Conferences</h2>
{% bibliography --query "@*[category=conference]" %}

</div>
