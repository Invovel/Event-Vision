# Project-driven learning path

[中文](README.md) | English

For each stage, record: question → principle → minimal experiment → observations → interpretation and limits.

## P01: Host protocol simulation

Cover valid, oversized, duplicate, busy and timeout cases without a camera or board.

Explain inputs, outputs, failure conditions and design choices.

## P02: Minimal buildable project

Create a standalone project, pin camera and model dependencies, and save build evidence. A successful build is not on-device validation.

Explain inputs, outputs, failure conditions and design choices.

## P03: Single-board fake trigger

Twenty sequential events each receive a matching terminal response. Record occupied and empty scenes; capture must work without an RTSP client.

Explain inputs, outputs, failure conditions and design choices.

## P04: External trigger adapters

Start with a simulated source, then optionally a sensor. Validate event keys, restarts and packet loss without changing the vision algorithm.

Explain inputs, outputs, failure conditions and design choices.

## P05: On-demand evaluation

Compare periodic and event-driven operation; record misses, response latency and active duty cycle. Energy requires instrumented measurement.

Explain inputs, outputs, failure conditions and design choices.

Add references for the current task rather than collecting a curriculum in advance.
