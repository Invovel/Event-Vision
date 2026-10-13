# Design and modules

[中文](design.md) | English

## Goal

Normalize an external trigger, capture one frame locally, run pedestrian detection and return a result or error with the same event key. Software triggers allow independent development without any particular sensor.

Data path: Fake / PIR / external trigger → protocol validation → single-event gate → capture → pedestrian detection → coordinate restoration → terminal response

| Module | Responsibility |
| --- | --- |
| trigger | Adapt inputs and validate fields; keep USB diagnostics separate from the application UART. |
| gate | One in-flight event, explicit busy rejection and a cache of the latest complete terminal response. |
| vision | Capture independently, infer, restore original-image coordinates and release resources. |
| result | Return result/error with the same boot_id/event_id; empty detections are a valid result. |

## Draft interface

Candidate protocol: JSONL, at most 1024 bytes per line including newline; fields v/kind/boot_id/event_id/source/level. Return vision_busy when busy and vision_result or vision_error for accepted events. Replay the cached terminal response for a completed key without capturing again. Coordinates use camera space with original image_size. Cache only the latest result within the current process; no exactly-once guarantee across power loss.

This contract has no validated implementation yet. Add examples, edge cases and migration notes when freezing it.

## Scope

The first version covers triggering, single-frame detection and correlated responses. It does not infer user intent or control actuators, and concurrent RTSP streaming is not required.

## Open decisions

- Pin dependency versions and confirm compatibility.
- Use initial measurements to set numerical acceptance thresholds.
- Confirm available hardware and resource budgets.
