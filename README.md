# Autonomous Vehicles — Obstacle Negotiation & Rule-Compliance Analysis
The screenshots show the repository level
<img width="794" height="547" alt="image" src="https://github.com/user-attachments/assets/8a1cc0cd-222d-4998-b1de-2b0b64669b24" />


An independent analysis of recurring rule-compliance and obstacle-negotiation
failures in autonomous-vehicle perception systems, based on real labelling and
annotation-quality work on Level-4 AV perception data (ego-motion, VLM, deep maps).

## What's in this repo

| File | What it is |
|------|------------|
| `Obstacle Negotiation & Rule Compliance Analysis.pdf` | The analysis write-up: observed failure modes, impact, and suggested improvements, framed against functional safety (SOTIF) and Level-4 validation. |
| `AV_Obstacle_negotiation_&_Rule_Compliance_Analysis.ipynb` | A reproducible notebook demonstrating the analysis methodology on a small synthetic dataset. |

## The real observation

While annotating AV perception data for Level-4 driving, I observed recurring
failure patterns at complex and occluded intersections — primarily failure-to-yield,
late braking, and path ambiguity near obstacles — concentrated under poor-visibility
conditions (glare, shadows) and around parked or lead vehicles. These are documented
in the write-up.

## The methodology demo (and its limits)

The notebook reproduces the *shape* of the analysis on a small synthetic dataset,
so the method is shareable without exposing any proprietary data.

**Important:** the synthetic violation rule is injected by design. The resulting
rates (8.8% vs 15.3%) therefore reflect that injected rule — they are an illustration
of the pipeline, **not** an empirical finding. The real-world pattern lives in the
write-up, derived from the perception work; the notebook only shows how such data
would be processed and visualised.

## Tools

Python · pandas · NumPy · matplotlib · annotation tooling (SuperAnnotate,
human-in-the-loop) for the underlying real-world work.

## Note on data

No proprietary data is included. All data in the notebook is synthetic and
generated in-code.
