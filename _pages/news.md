---
layout: page
title: News
permalink: /news/
nav: true
nav_order: 3
---

<div class="news">
  <table class="table table-sm table-borderless">
    {% assign news = site.news | reverse %}
    {% for item in news %}
      <tr>
        <th scope="row" style="width: 140px;">
          {{ item.date | date: "%b %-d, %Y" }}
        </th>
        <td>
          {% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            <a class="news-title" href="{{ item.url | relative_url }}">
              {{ item.title }}
            </a>
          {% endif %}
        </td>
      </tr>
    {% endfor %}
  </table>
</div>