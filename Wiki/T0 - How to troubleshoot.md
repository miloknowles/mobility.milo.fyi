## Basics

The assessments ([[U0 - Upper Body Mobility Assessment]], [[L0 - Lower Body Mobility Assessment]]) tell you *that* a range is limited. A troubleshoot session tells you *why*, so you train the right thing. It works like debugging: change one variable, remeasure, and see what moves.

The same limit can come from very different causes, and each one is trained differently:

| Cause | How fast it changes | What to do |
| --- | --- | --- |
| **Bone** (e.g. femoral version, bone spurs) | Never | Accept the range and train strength within it. Don't chase symmetry. |
| **Joint capsule or glide** | Weeks to months | End-range loading, joint mobilizations |
| **Muscle length** | Weeks | The [[A3 - How to improve mobility]] process |
| **Tone, guarding, position** | Minutes | A short reset as a warm-up, then load the new range so it sticks |
| **Control** (passive range is fine, active isn't) | Weeks | End-range strength (RAILs, step 4 of [[A3 - How to improve mobility]]) |

General testing rules from [[A2 - How to assess mobility]] still apply.

## Rules

- **Only troubleshoot a test that fails or stalls.** If a core test meets its standard, there's nothing to debug.
- **Differentiate by what each tissue crosses.** Change the position of a neighbouring joint (knee, trunk, elbow, pelvis). If the limit moves, a tissue that crosses that joint is involved.
- **Use reset tests as experiments.** Do one 2–3 minute intervention, then remeasure right away. Bone doesn't change in minutes and muscle length barely does, so an immediate gain points to tone, position or joint glide.
- **Control for warm-up.** On another day, swap the reset for 2–3 minutes of easy movement or rest, then remeasure. If that gives the same gain, the reset isn't what's working. When a page has more than one reset, vary the order across sessions.
- **Only count changes bigger than noise.** Until you know your own test–retest noise, assume ~5° for angles and ~1 cm for distances.
- **Expect more than one cause.** Run every step rather than stopping at the first positive. The flowcharts only set priority.
- **Don't diagnose by palpation.** Static landmark palpation (ASIS/PSIS heights) and motion palpation tests (standing/seated flexion, Gillet) have poor reliability between examiners and don't match imaging. Measure ranges instead.
- **Treat patterns as hypotheses.** Postural patterns like PRI's Left AIC are ideas to test, not diagnoses. Evidence for them is mostly case reports, and pattern-specific treatment hasn't been shown to beat good general training.
- **Pain = stop.** Pain, rather than stretch or stiffness, is a PT question.

## Outputs

Every session ends with:
1. **Raw measurements**, including any post-reset numbers
2. **A classification**, which may include more than one cause, plus a confidence note
3. **A program bucket**, linking to the layer 1 page for that region
4. **A retest date**, by default 2–4 weeks

On retest, track the **pre-reset baseline**. That's the number that shows lasting change. If a reset stops producing gains while the baseline rises, the factor it targeted is resolved. Rerun the session.

## Pages

| Page | Starts from |
| --- | --- |
| [[T1 - Hip Rotation Asymmetry]] | Hip IR/ER tests in [[L0 - Lower Body Mobility Assessment]] |
| [[T2 - Ankle Dorsiflexion]] | `ankle-dorsiflexion-wall` in [[L0 - Lower Body Mobility Assessment]] |
| [[T3 - Overhead Reach]] | `supinated-overhead-reach` in [[U0 - Upper Body Mobility Assessment]] |

## App notes

- **Entry point:** the app suggests a troubleshoot session when an assessment flags a limit.
- **Node types:**
  - Measurement: angle or distance input, with a demo video
  - Computed: deltas and totals, filled in automatically
  - Branch: thresholds, configurable per user once their noise is known
  - Reset: a timed intervention, then an automatic remeasure prompt
  - Observation: a picker for end-feel or where the limit is felt
- **Stored data:** keep the raw numbers and the order of resets, not just the classification, so sessions can be re-run if thresholds change.
- **Safety gate:** ask about pain at the start and before any end-feel step. A yes ends the session with a PT referral message.
