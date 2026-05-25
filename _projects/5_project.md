---
layout: page
title: Reinforcement Learning for Self-Organizing Networks
description: Multi-agent RL for distributed power control in heterogeneous and mmWave networks
img: assets/img/8.jpg
importance: 4
category: work
related_publications: true
---

## Reinforcement Learning for Self-Organizing Wireless Networks

My PhD dissertation — **"Reinforcement Learning in Self-Organizing Cellular Networks"** (Boise State University, 2020) — addressed a fundamental challenge in dense heterogeneous networks: how should thousands of small cells coordinate their behavior without a central controller?

### Problem

5G heterogeneous networks (HetNets) mix macro base stations with dense layers of small cells (picocells, femtocells). Getting these cells to cooperate on power allocation, handover decisions, and activation scheduling — in real time, at scale, with incomplete information — is computationally intractable for centralized approaches.

### Approach

I developed **distributed multi-agent reinforcement learning** algorithms where each cell acts as an autonomous agent learning from local observations:

- **Q-learning and deep RL** for distributed power control and QoS-aware resource allocation
- **Self-organizing activation policies** — cells learn when to turn on/off based on local traffic and interference measurements
- **Clustering-based coordination** — grouping nearby cells to limit the action space while preserving cooperation benefits

The algorithms were validated through system-level simulation at realistic network densities using [GeoNS](/projects/1_project/), the spatial network simulator developed in parallel.

### mmWave Self-Organization

A second research thread applied RL to **mmWave (60 GHz) MIMO systems**, where beam management, small-scale fading, and shadowing create additional complexity:

- Lens-based MIMO architectures for simultaneous fading and shadowing suppression
- RL-driven beam selection and power allocation under blockage uncertainty
- Topology management for mmWave backhaul in integrated access-and-backhaul (IAB) networks

### Publications

{% cite amiri2019reinforcement amiri2018machine amiri2018joint almasi2020mmwave amiri2020spatial %}
