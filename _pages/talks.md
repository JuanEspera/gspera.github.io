---
layout: page
permalink: /talks/
title: Talks
description: Here you can find a complete list of my talks.
years: [2023]
nav: true
nav_order: 2
---
<!-- _pages/talks.md -->
<div class="publications">

{%- for y in page.years %}
  <h1 class="year">{{y}}</h1>
  {% bibliography -f talks -q @*[year={{y}}]* %}
{% endfor %}

</div>
