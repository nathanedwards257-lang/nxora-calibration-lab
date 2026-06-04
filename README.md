# NXORA Calibration Lab

NXORA Calibration Lab is a public-safe showcase of a deterministic examiner-behaviour calibration project for structured essay assessment.

The project explores how an assessment system can move beyond simple keyword matching and instead model whether written evidence is meaningful, validated, trustworthy, and suitable for higher-level scoring decisions.

This repository does **not** contain the private NXORA engine, scoring thresholds, protected calibration data, anchors, weights, examiner scripts, or internal route logic.

It exists to document the public architecture, design philosophy, safety boundaries, and calibration discipline behind the project.

---

## Project Focus

NXORA is being developed around a simple but demanding question:

> Can a deterministic system evaluate essay behaviour in a way that is transparent, auditable, and closer to disciplined examiner judgement than raw keyword scoring?

The current focus is A-Level Economics essay assessment, with particular attention to:

- economic reasoning quality
- evaluation strength
- question focus
- context integration
- maturity recognition
- over-scoring protection
- under-scoring recovery
- auditability and deterministic repeatability

---

## Core Principle

NXORA is not designed as a keyword counter.

The system is built around the idea that detected evidence must earn permission before it can influence higher-level scoring.

A phrase such as “however”, “therefore”, or “it depends” is not automatically treated as strong analysis or evaluation.

Instead, the system asks whether the evidence is connected to real reasoning, context, judgement, and examiner-rewardable behaviour.

---

## Permission Ladder

NXORA uses a public-safe permission model:

| Stage | Meaning |
|---|---|
| P0 Observed | A signal has been detected. |
| P1 Validated | The signal appears meaningful in context. |
| P2 Trusted | The signal is reliable enough to support scoring. |
| P3 Authorised | The signal is strong enough to open a protected scoring route. |

This protects against shallow signal inflation.

Seeing a word is not the same as understanding an argument.

---

## Route Doors

Higher-level outcomes are protected by route doors.

These represent controlled decisions rather than automatic score jumps.

| Route Door | Purpose |
|---|---|
| P3-L4 | Tests whether evidence supports genuine Level 4 maturity. |
| P3-RA | Allows cautious recovery of mature under-recognised responses. |
| P3-RB | Allows cautious recovery of compact but complete responses. |
| P3-A | Controls access to A-band outcomes. |
| P3-FM | Protects rare full-mark outcomes. |
| P3-PF | Checks whether the response fits the exact question. |

The purpose of these route doors is to prevent the system from treating “strong-looking” evidence as automatically high-quality evidence.

---

## Behavioural Blockers

NXORA also uses blocker concepts to prevent unsafe promotion.

Examples include:
 
- evaluation theatre
- false Level 4 recognition
- route near-miss behaviour
- prompt drift
- full-mark rarity failure
- thinness or basicness

These blockers help separate genuine examiner-rewardable maturity from surface-level performance.

---

## Calibration Philosophy

NXORA development follows a disciplined calibration cycle:

**Observe → Map → Diagnose → Preserve → Refine**

The aim is not to chase higher marks or force the engine to agree with one script.

The aim is to improve behavioural reliability across a protected calibration ladder.

This means every change should be tested against both:

- over-scoring risk
- under-scoring risk

A good calibration change should improve one area without damaging another.

---

## Public Safety Boundary

This repository is intentionally public-safe.

It may include:

- architecture summaries
- calibration philosophy
- public-safe diagrams
- synthetic examples
- non-sensitive development notes
- high-level pseudocode

It will not include:

- private engine source code
- protected scoring rules
- exact thresholds
- anchor files
- weight files
- examiner-marked scripts
- protected ladder outputs
- internal calibration JSON traces
- proprietary route conditions

The goal is to demonstrate engineering discipline without exposing private intellectual property.

---

## Why This Matters

Essay assessment systems can become unreliable when they reward visible signals too easily.

For example, a weak response may contain evaluation-looking words, but still lack meaningful judgement.

A strong response may be compact and restrained, but still show genuine maturity.

NXORA is designed to explore this distinction through deterministic, auditable calibration logic.

The long-term aim is to support clearer, safer, and more explainable assessment feedback for students, teachers, and exam preparation environments.

---

## Documentation

Public-safe project documentation:

- [Architecture Overview](docs/architecture_overview.md)
- [Calibration Philosophy](docs/calibration_philosophy.md)
- [Public Safety Boundary](docs/public_safety_boundary.md)
- [Calibration Case Study](docs/calibration_case_study.md)
- [Evidence-Driven Assessment](docs/evidence_driven_assessment.md)
## Current Status

This repository is an early public showcase.

The private NXORA engine remains under active development and is not included here.

Future public-safe additions may include:

- architecture overview documents
- calibration flow diagrams
- synthetic case studies
- public development logs
- safety boundary notes
- explainability examples

---

## Author

Built by Nathan Edwards as part of the NXORA assessment-engineering project.
