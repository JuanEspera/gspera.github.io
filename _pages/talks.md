---
layout: page
permalink: /talks/
title: Talks
description: Here you can find a complete list of my talks and poster presentations.
# years: [Invited, Seminars,Contributed talks,Poster]
years: [2025, 2024, 2023, 2022]
nav: true
nav_order: 2
---
<!-- _pages/talks.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f talks -q @*[year={{y}}]* %}
{% endfor %}

</div>
