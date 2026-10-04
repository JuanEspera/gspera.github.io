---
layout: page
permalink: /publications/
title: Publications
description: Here you can find a complete list of my publications.
# years: [2027,2026,2025, 2024]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<!-- <div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div> -->

<div class="publications">

{% assign years = site.data.bibliography.papers | map: "year" | uniq | sort | reverse %}

{% for y in years %}
  <h2 class="year">{{ y }}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>