## Basics

Every test view gets a structured setup description so the app can order a session automatically. It groups tests that share a setup and puts the expensive changes as few times as possible. A session can mix batteries ([[U0 - Upper Body Mobility Assessment]], [[L0 - Lower Body Mobility Assessment]], [[F0 - Posture & Movement Screen]]), so one comprehensive session could run every lying-on-your-back test together, whatever region it's for.

Setup is described per view (each side of a test), not per test, because left and right can need different setups.

**Every test must be doable alone.** No partner tests. If a test needs a partner, replace it with a solo version (gravity, a weight, a wall or the floor doing the partner's job) or drop it.

## Two parts: the camera and the body

The camera is described relative to the room, and the body relative to the camera. Changing the camera is what costs time. Turning or flipping your body is cheap, so where possible left and right are handled by turning or lying the other way, not by moving the camera.

### Camera

| Field   | Values                                                                                            |
| ------- | ------------------------------------------------------------------------------------------------- |
| Height  | floor, knee, hip, shoulder, head                                                                  |
| Station | where the tripod stands in the room (e.g. A, B), with a floor mark so it's the same every session |
| Tilt    | level, angled down, straight down from above                                                      |
| Framing | full body, or one body region                                                                     |

Height bins are set from your own body **while standing**: the tripod height that matches your knee, hip, shoulder and head. Calibrate once and reuse. This is the closest fixed version of the rule in [[A2 - How to assess mobility]] to put the camera at the height of the joint being tested.

### Body

| Field | Values |
|---|---|
| Base position | standing, sitting (chair / floor), tall kneeling, half kneeling, kneeling sat back on heels, hands and knees, lying on back, lying face down, lying on your side (left / right), hanging |
| Surface | floor, bench, wall, bar |
| Facing the lens | front, back, left side, right side, top of head, feet |
| Props | stick, towel, bench, strap, dumbbell |

"Facing the lens" names which part of the body points at the camera. This replaces "front view / side view", which become ambiguous once you're lying down.

### Plane of motion

Each test also records the plane it measures (sagittal, frontal or transverse). For a 2D angle the camera has to look straight at that plane, so the plane plus the base position decide which part of the body must face the lens. The app can use this to check that a setup actually works.

## Ordering

Sort by transition cost, most expensive first, so the costly changes happen least often:

1. Camera height
2. Camera station
3. Getting down to or up from the floor (base position)
4. Props
5. Which way you face
6. Side (left / right)

Rules from [[A2 - How to assess mobility]] still take priority over convenience: weaker side first, active tests before their passive follow-ups.

## Open questions

- **Floor height.** Lying tests need the camera near the floor, which none of the standing body landmarks covers. Proposed: add "floor" as its own height bin (it's included above).
- **Existing partner tests** to replace with solo versions:
  - ~~Cervical flexion-rotation test (U0 follow-ups)~~: replaced by the chin-tucked neck rotation follow-up.
  - Steps 2, 5 and 8 in [[T3 - Overhead Reach]]
