# Event-Vision · Event-Driven Visual Verification

[中文](README.md) | English

How can a device observe on demand and return a trustworthy result associated with the triggering event?

Normalize an external trigger, capture one frame locally, run pedestrian detection and return a result or error with the same event key. Software triggers allow independent development without any particular sensor.

Status: October 13, 2026 — a design starting point. No new firmware, model training or hardware acceptance has been completed.

## Start here

1. [Next task](CODEX_START.en.md).
2. [Design and scope](docs/design.en.md).
3. [Implementation roadmap](docs/roadmap.en.md).
4. [Hardware and baseline](hardware/baseline.en.md).
5. [Learning path](learning/README.en.md).
6. [First experiment](experiments/P01.en.md) and [record template](experiments/template.en.md).
7. [Design origin and reference management](references/origin.en.md).

## Distinct goal and scope

The first version covers triggering, single-frame detection and correlated responses. It does not infer user intent or control actuators, and concurrent RTSP streaming is not required.

This repository stands on its own, with its own design, learning path and experiments. Build evidence through measurements; do not present unperformed experiments as results.
