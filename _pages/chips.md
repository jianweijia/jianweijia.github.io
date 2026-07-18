---
layout: page
title: chips
permalink: /chips/
description: Silicon chips I have taped out — most with full-flow involvement (design, synthesis, APR, and sign-off), and some with contributions to the design phase.
nav: true
nav_order: 6
---

<div class="projects">
  <div class="row row-cols-1">
    {% assign sorted_chips = site.chips | sort: "importance" %}
    {% for chip in sorted_chips %}
      {% include chips.liquid %}
    {% endfor %}
  </div>
</div>
