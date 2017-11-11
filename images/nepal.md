---
layout: page
title: Nepal Gallery
regenerate: true
---

<p style="text-align:center">
</p>


{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files reversed %}
  {% if myimage.path contains 'nepal' %}
  <p style="text-align:center">
  <a href = "{{ myimage.path }}">
  <img src = "{{ myimage.path | replace: 'photos','thumbs'}}"
  alt="{{ myimage.name }}">
  </a>
  </p>
  {% endif %}
{% endfor %}