---
layout: page
title: "ACIM Macro - FeFET(PDK: GF28SLPe)"
description: "4-kb FeFET compute-in-memory macro with 64×64 crossbar array and on-chip 4-bit Flash ADC."
img_gds: assets/img/chips/2024_fefet_acim_gds.png
img_die: assets/img/chips/2024_fefet_acim_die.JPG

tech: "GF 28nm FeFET"
year: 2024
importance: 1
related_publications: true
---

## Overview

This chip implements a 4-kb FeFET-based compute-in-memory (CIM) macro fabricated in GlobalFoundries 28-nm HKMG FeFET process. It features a 64×64 crossbar array with on-chip 4-bit Flash ADCs for analog-to-digital conversion.

## Key Results

- **Energy efficiency**: 346.6 TOPS/W (9.5× improvement over prior 40-nm RRAM-CIM)
- **Inference accuracy**: 89.1% on CIFAR-10 (VGG-8), close to 89.7% software baseline
- **Innovation**: ISPP (Incremental Step Pulse Programming) scheme to reduce current variation

## Publications

{% cite 11277307 %}
