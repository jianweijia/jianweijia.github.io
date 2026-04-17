---
layout: page
title: "Nanoscale Cap Measurement & DCIM Macro - FeFET(PDK: GF28SLPe)"
description: "aF-resolution on-chip nvCAP C–V characterization across scaled geometries & 4-kb FeFET non-volatile digital compute-in-memory macro with power-gating"
img_gds: assets/img/chips/2025_dcim_cap_measure_gds.png
img_die: assets/img/chips/2025_dcim_cap_measure_die.png

tech: "GF 28nm FeFET"
year: 2025
importance: 1
related_publications: true
---

## Overview

This tapeout includes two co-fabricated structures on the GlobalFoundries 28 nm FeFET process:

1. **nvCAP CVCM Macro** — A standalone on-chip capacitance-to-voltage converter measurement (CVCM) circuit for direct aF-resolution characterization of sub-fF non-volatile capacitance (nvCAP) in nanoscale FeFET devices, with MOSCAP-assisted calibration.

2. **nvDCIM Macro** — A 4-kb non-volatile digital compute-in-memory (nvDCIM) macro using a novel 2-FeFET voltage-divider bitcell for weight storage. The bitcell produces a binary voltage output via the voltage-divider effect, directly driving CMOS adder trees without additional sensing circuitry. Non-volatility enables power-gating with instant on/off operation, eliminating the need for weight reloading.

## Circuit 1: aF-Resolution nvCAP Characterization (CVCM Macro)

---
## Circuit 2: Non-Volatile DCIM Macro

### Architecture

- **Array**: 4 Kb FeFET voltage-divider array (1024 input × 32 output channels)
- **Bitcell**: 2-FeFET n-type voltage-divider (area: 0.482 µm²), 16% smaller than 28 nm non-push-rule 6T SRAM
- **MAC operation**: 4b×4b INT4, single-cycle compute
- **On-chip logic**: LUT-assisted multiplier, 4-parallel adder trees, shift-accumulate
- **Total macro area**: 0.184 mm²
- **Power supply**: 0.8–1.1 V (dual power rails for compute and FeFET array)

### Key Results

- **Throughput**: 106.6 TOPS/W @ 0.8 V (10% input toggle, 50% weight = 1)
- **Compute cycle time**: 5 ns
- **Idle power saving**: −77.7% vs. comparable 28 nm SRAM DCIM (1% activity factor, full macro power-gating)
- **Memory-only power-gating saving**: −5.43%
- **Bitcell static leakage**: 6.25 pW @ 0.8 V (67.7% lower than 6T SRAM cell)
- **MAC accuracy**: up to 99.89% with 3.5/3.8 V program/erase pulses
- **Inference accuracy**:
  - 89.66% on CIFAR-10 (VGG-8) — matches software baseline
  - 79.41% on ImageNet (ResNet-18), vs. 79.97% software baseline (−0.56%)
- **Non-volatile retention**: confirmed over 5 days

### Key Innovation

The dual n-type FeFET voltage-divider bitcell clamps the output to ~V_DD (logic "1") or ~V_SS (logic "0") depending on the stored polarization state, enabling lossless, amplifier-free binary readout directly into the CMOS adder tree. Non-volatility supports power-gating with no weight-reload penalty — a key advantage for edge AI inference at low activity factors.


---

## Publications

{% cite 11457631 %}
