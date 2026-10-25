# Optimizing Urban Traffic Signals Through Mathematical and Camera-Based Adaptive Control

Independent research by **Daniel Melnikov** · Advisor: Dr. Mark Vondracek · Evanston Township High School

**Live project site:** https://danielzmelnikov-ui.github.io/dmelnikov_traffic_optimization.github.io/

## What this is

If far more vehicles travel through an intersection in one direction, should both directions get equal green time? I counted traffic for one hour at Lincoln Street and Green Bay Road in Evanston, Illinois, then built a two-stage model to see how much delay smarter signal timing could remove.

## Headline results

| Result | Value |
|---|---|
| Vehicle arrivals recorded (one hour, from about 8:00 AM) | 3,122 |
| Share traveling North–South | 71.65% |
| Optimized fixed split vs. 60/60 (modeled delay) | 18.75% lower |
| Camera-aware controller vs. arrival-only adaptive (queue delay) | 16.77% lower |
| Camera-aware controller vs. optimized fixed (queue delay) | 42.02% lower |

Phase I and Phase II measure different things (expected red delay vs. persistent queue delay), so their percentages should not be compared directly.

## Method

**Phase I: fixed optimization.** Using directional arrival totals, I derived the North–South/East–West split that minimizes expected red-signal delay in a simplified two-phase, 120-second cycle. Green time comes out proportional to demand: about 85.98 s North–South and 34.02 s East–West.

**Phase II: queue-aware adaptive control.** Using the minute-by-minute record of arrivals, queues, and discharge, I simulated four strategies on identical data: equal fixed, optimized fixed, arrival-only adaptive, and queue-aware (camera-style) adaptive. Queues carry over between minutes, and controllers use only past information.

**Appendix: nine hypothetical intersection types.** The same idea is tested on synthetic road layouts, from wide–wide to narrow–narrow. These are scenario demonstrations, not field measurements.

## Limitations

- One one-hour observation at one intersection.
- Simplified two-phase model: no turn phases, pedestrians, transit, or corridor coordination.
- Service capacity is a simplified assumption, not a lane-by-lane calibration.
- The camera system is a proposed design. It has not been built or tested, so detection error, occlusion, and weather are open questions.

## Context

Lincoln Street at Green Bay Road is part of the City of Evanston's Green Bay Road Corridor Improvements Project, which includes traffic-signal improvements. This project is a student-scale model, not a replacement for municipal traffic engineering.

## Repository contents

- `index.html`: the interactive project website
- `README.md`: this file

## Next steps

Repeat the counts across more days and conditions, build the video pipeline and compare it with hand counts, and run the model in shadow mode against real timing plans.
