---
layout: page
title: Neural RF-SLAM & AI-Native Positioning
description: Simultaneous positioning and mapping from 5G channel state information
img: assets/img/7.jpg
importance: 3
category: work
related_publications: true
---

## Neural RF-SLAM and AI-Native Indoor Positioning

Traditional indoor positioning relies on fingerprinting databases, known maps, or dedicated localization infrastructure. This project explores a different approach: using **5G channel state information (CSI)** as the sole sensing modality to simultaneously estimate a mobile agent's position and build a map of its environment — no GPS, no pre-existing maps, no labeled data required.

### Neural RF-SLAM

We introduced **Neural RF-SLAM**, an unsupervised framework for simultaneous radio-frequency positioning and mapping. The system combines:

- A **neural implicit representation** of the radio environment, mapping spatial coordinates to expected channel responses
- A **SLAM-style optimization** loop that jointly refines the agent's trajectory and the learned RF map
- Training directly from raw 5G CSI measurements, with no ground-truth position labels

The result is a system that discovers the geometry of an indoor space purely from the way wireless signals propagate through it.

### AI-Native 5G Indoor Localization

Building on RF-SLAM, we developed a supervised localization pipeline with **IMU supervision** that achieves sub-meter accuracy indoors. Key ideas:

- IMU measurements used as a supervisory signal during training — teaching the network about physical motion constraints without requiring position ground truth
- At inference, the model estimates position from CSI alone, with no IMU dependency
- Evaluated in challenging multipath environments at 5G NR Sub-6 GHz frequencies

### Indoor Environment Learning via RF-Mapping

The third line of work learns a **dense environmental representation** (not just a position estimate) from RF measurements. The learned map captures structural features of the environment — walls, openings, material properties — purely from radio propagation effects.

### Publications

{% cite amiri2023indoor kadambi2022neural ermolov2023neural %}
