---
layout: page
permalink: /publications/
title: publications
description: 📄papers~
years: [2025, 2024, 2023, 2022, 2021]
nav: true
---

<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
  {% for entry in site.data.papers %}
    {% if entry.year == y %}
      <a href="{{ entry.url }}" target="_blank">{{ entry.title }}</a>
    {% endif %}
  {% endfor %}
{% endfor %}

</div>