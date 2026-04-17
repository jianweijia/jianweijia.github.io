---
layout: page
title: chips
permalink: /chips/
description: Silicon chips I have designed and taped out.
nav: true
nav_order: 6
---

<div class="projects">
  <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3">
    {% assign sorted_chips = site.chips | sort: "importance" %}
    {% for chip in sorted_chips %}
      {% include chips.liquid %}
    {% endfor %}
  </div>
</div>
