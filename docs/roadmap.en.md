# Implementation roadmap

[中文](roadmap.md) | English

Advance on deliverables and acceptance evidence, not assumed calendar progress.

| Stage | Task | Completion criteria | Status |
| --- | --- | --- | --- |
| P01 | Host protocol simulation | Cover valid, oversized, duplicate, busy and timeout cases without a camera or board. | Not started |
| P02 | Minimal buildable project | Create a standalone project, pin camera and model dependencies, and save build evidence. A successful build is not on-device validation. | Not started |
| P03 | Single-board fake trigger | Twenty sequential events each receive a matching terminal response. Record occupied and empty scenes; capture must work without an RTSP client. | Not started |
| P04 | External trigger adapters | Start with a simulated source, then optionally a sensor. Validate event keys, restarts and packet loss without changing the vision algorithm. | Not started |
| P05 | On-demand evaluation | Compare periodic and event-driven operation; record misses, response latency and active duty cycle. Energy requires instrumented measurement. | Not started |

Research extension: Study the benefits and missed-event costs of triggered observation. Keep the vision model and scenes fixed across trigger sources to avoid attributing model accuracy changes to trigger policy.

Update learning notes, results and next steps after each iteration. Preserve failures and their conditions.
