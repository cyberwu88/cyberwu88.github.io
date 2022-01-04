---
layout: page
permalink: /publications/
title: Publications
description: An up-to-date list is available on Google Scholar.
years: [2021, 2020, 2019, 2018, 2016, 2013]
nav: true
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
