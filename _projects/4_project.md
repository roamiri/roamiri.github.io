---
layout: page
title: On-Device AI Efficiency & Model Quantization
description: Compressing large neural networks for deployment on mobile and edge hardware
img: assets/img/9.jpg
importance: 1
category: work
---

## On-Device AI Efficiency

Running state-of-the-art AI models on mobile devices — phones, cars, AR glasses — requires squeezing them through a tight bottleneck: limited compute, constrained memory bandwidth, and strict power budgets. **Model quantization** is one of the most effective tools for this.

At **Qualcomm AI Research**, my work focuses on quantization and compression techniques that preserve model accuracy while dramatically reducing the cost of inference on Snapdragon SoCs.

### Quantization

Quantization replaces full-precision (FP32) weights and activations with low-bit integer representations (INT8, INT4, or lower). The challenge is doing this without degrading model quality:

- **Post-training quantization (PTQ)** — calibrate a pre-trained model with a small dataset; no retraining required, but accuracy degrades more at very low bits
- **Quantization-aware training (QAT)** — simulate quantization during training to let the model adapt; achieves better accuracy at the cost of training compute
- **Mixed-precision quantization** — assign different bit-widths to different layers based on their sensitivity, maximizing compression for a given accuracy budget

### LLM Quantization

Large language models (LLMs) bring new challenges: extreme scale, outlier activations, and sensitivity to weight rounding errors. Current research directions include:

- Activation-aware weight quantization strategies that handle outlier channels
- Function-preserving transforms that reshape weight/activation distributions before quantization
- Per-channel and per-group quantization schemes calibrated to model structure

### Target Hardware

All compression work is co-designed with Qualcomm's **Hexagon NPU** and **Adreno GPU** architectures — the quantized model must not only be accurate, but also fast on real silicon.

### Tools

Qualcomm's open-source [AIMET (AI Model Efficiency Toolkit)](https://github.com/qualcomm/aimet) implements many of these techniques and is available for public use.
