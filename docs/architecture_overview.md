# NXORA Architecture Overview

This document provides a public-safe overview of the NXORA calibration architecture.

It does not disclose private engine code, scoring thresholds, anchors, weights, protected calibration files, examiner scripts, or internal route logic.

NXORA is presented here as a deterministic examiner-behaviour calibration system: a structured approach to assessing whether essay evidence is meaningful, validated, and suitable for higher-level scoring decisions.

---

## 1. Architectural Purpose

NXORA is designed to explore a central assessment problem:

> How can an essay assessment system recognise genuine reasoning quality without being misled by surface-level signals?

Traditional automated scoring systems can become vulnerable to:

- keyword inflation
- repeated evaluation phrases
- excessive connector use
- long but unfocused answers
- weak arguments that appear busy
- compact answers that are wrongly treated as underdeveloped

NXORA is built to separate signal detection from scoring authority.

A detected phrase is only the beginning of the process. It must pass through validation, behavioural profiling, and controlled authorisation before it can influence higher-level outcomes.

---

## 2. Public Stack Summary

The private NXORA engine is not included in this repository.

At a public architectural level, the system can be understood as the following stack:

| Layer | Public Description |
|---|---|
| Input Layer | Receives the essay response and question context. |
| Normalisation Layer | Standardises text into stable units for deterministic analysis. |
| Signal Detection Layer | Identifies public-safe categories of reasoning, evaluation, context, and structure. |
| Line Analysis Layer | Reviews sentence-level behaviour and evidence patterns. |
| Route Analysis Layer | Examines whether reasoning develops as a connected chain rather than isolated claims. |
| Profile Layer | Converts raw signals into behavioural profiles such as reasoning, judgement, fit, and integration. |
| Validation Layer | Checks whether detected signals are meaningful enough to be trusted. |
| Response Structure Model | Interprets the maturity and shape of the answer. |
| Governor Layer | Prevents unsafe promotion and protects higher-level outcomes. |
| Mark Placement Layer | Converts authorised behavioural judgement into an estimated outcome. |
| Audit Layer | Preserves traceability, repeatability, and calibration evidence. |

The central design principle is simple:

> Scoring should follow validated behaviour, not raw signal volume.

---

## 3. Signal Detection Is Not Scoring

NXORA treats detected signals as evidence candidates.

For example, a response may contain words such as:

- however
- therefore
- depends on
- overall
- in the long run
- government failure

These may be useful, but they are not automatically strong evaluation or analysis.

The system must ask:

- Is the signal connected to an economic mechanism?
- Is it relevant to the question?
- Is it supported by reasoning?
- Does it help form a judgement?
- Is it integrated into the argument?
- Could it mislead the system into over-scoring?

This distinction is central to the project.

---

## 4. Permission-Based Evidence Flow

NXORA uses a permission-based evidence model.

| Stage | Role |
|---|---|
| P0 Observed | The system detects a possible signal. |
| P1 Validated | The system checks whether the signal appears meaningful. |
| P2 Trusted | The signal is reliable enough to support the scoring profile. |
| P3 Authorised | The signal is strong enough to open a protected route. |

This helps protect the system from treating surface-level essay features as high-level academic quality.

---

## 5. Protected Route Doors

Some scoring outcomes require additional authorisation.

These are represented publicly as route doors.

| Route Door | Public Purpose |
|---|---|
| Level 4 Door | Checks whether evidence supports genuine high-level maturity. |
| Recovery Door A | Allows cautious recovery of mature but under-recognised responses. |
| Recovery Door B | Allows cautious recovery of compact but complete responses. |
| A-Band Door | Controls access to top-band outcomes. |
| Full-Mark Door | Protects rare full-mark outcomes. |
| Prompt-Fit Door | Checks whether the response answers the exact question. |

Route doors are designed to avoid automatic promotion.

A response may look strong in one area but still fail a higher-level route if its evidence is thin, unfocused, unsupported, or misaligned with the question.

---

## 6. Behavioural Blockers

NXORA also uses blocker concepts to prevent unsafe scoring movement.

Public-safe examples include:

- evaluation theatre
- false high-level recognition
- route near-miss behaviour
- prompt drift
- full-mark rarity failure
- thinness or basicness

These blockers help the system avoid rewarding answers that appear sophisticated but do not provide enough examiner-rewardable evidence.

---

## 7. Examiner-Behaviour Modelling

NXORA is not trying to simulate a human examiner emotionally or intuitively.

Instead, it attempts to approximate disciplined examiner behaviour through deterministic rules and auditable evidence flow.

This means the system focuses on whether a response demonstrates:

- controlled reasoning
- relevant economic mechanisms
- question focus
- contextual integration
- supported judgement
- maturity of argument
- resistance to surface-level inflation

The goal is examiner-style discipline, not hidden judgement.

---

## 8. Calibration Philosophy

NXORA development follows the cycle:

**Observe → Map → Diagnose → Preserve → Refine**

This means calibration changes should not be made just to force one script to match an expected mark.

Instead, changes should be tested against a protected calibration ladder to check whether they improve the system without causing regression elsewhere.

A strong calibration change should:

- reduce dangerous over-scoring
- recover genuine under-scoring where justified
- preserve correct existing outcomes
- improve behavioural explanation
- maintain deterministic repeatability

---

## 9. Auditability

A major goal of NXORA is traceability.

A public-safe assessment architecture should be able to explain:

- what evidence was detected
- what evidence was trusted
- what evidence was blocked
- what evidence was authorised
- why higher-level access was allowed or denied
- whether the system behaved consistently across repeat runs

This is why audit design is treated as part of the architecture, not an afterthought.

---

## 10. Public Safety Boundary

This repository does not include:

- private source code
- scoring thresholds
- exact route conditions
- anchor files
- weight files
- protected calibration outputs
- examiner-marked scripts
- gold script banks
- internal JSON traces
- proprietary calibration ladders

The aim is to show the architecture and engineering discipline without exposing the private engine.

---

## 11. Long-Term Direction

The longer-term NXORA vision is to support clearer, safer, and more explainable essay feedback.

A future product could help students understand not just a likely mark, but why their essay is being limited or rewarded.

The project direction is therefore both technical and educational:

- technical because it requires deterministic calibration architecture
- educational because feedback must be understandable and useful
- ethical because scoring systems must avoid shallow or misleading judgement
- commercial because trustworthy assessment tools require strong governance before public use

---

## Summary

NXORA is a deterministic calibration architecture for essay assessment.

Its core belief is that higher-level scoring should only happen when evidence is not merely detected, but validated, trusted, and authorised.

This public repository documents that philosophy while protecting the private engine.
