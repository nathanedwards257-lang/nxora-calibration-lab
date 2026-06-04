# NXORA Public Safety Boundary

This document defines the public safety boundary for the NXORA Calibration Lab repository.

The purpose of this repository is to showcase NXORA’s assessment-engineering discipline without exposing private intellectual property, protected scoring logic, calibration data, or examiner materials.

---

## 1. Purpose of the Boundary

NXORA is being developed as a deterministic examiner-behaviour calibration system.

That means some parts of the project are suitable for public explanation, while other parts must remain private.

This boundary protects:

- proprietary engine design
- scoring route logic
- calibration thresholds
- protected test ladders
- examiner-marked material
- private audit traces
- future commercial value
- student and assessment integrity

The public repository should explain the philosophy and architecture without giving away the working engine.

---

## 2. Public-Safe Material

The following material is suitable for this repository.

| Public-Safe Area | Reason |
|---|---|
| Project overview | Explains the purpose without exposing implementation. |
| Architecture summaries | Shows engineering discipline at a high level. |
| Calibration philosophy | Explains how the system is improved safely. |
| Permission ladder explanation | Describes the evidence flow without private thresholds. |
| Route door concepts | Shows protected scoring governance in abstract form. |
| Blocker concepts | Explains safety thinking without internal conditions. |
| Synthetic examples | Allows demonstration without using real examiner scripts. |
| Diagrams | Useful if they remain high-level and non-secret. |
| Development logs | Safe if they avoid private code and exact scoring internals. |

Public-safe content should help a reader understand the system’s seriousness, not replicate the system.

---

## 3. Private Material

The following material must not be published in this repository.

| Private Area | Reason |
|---|---|
| Engine source code | Core proprietary implementation. |
| Anchor files | Reveal signal detection strategy. |
| Weight files | Reveal scoring influence and calibration bias. |
| Scoring thresholds | Reveal protected decision boundaries. |
| Route conditions | Reveal high-level access logic. |
| Governor logic | Reveals promotion and blocking mechanics. |
| Gold scripts | May contain protected examiner or student material. |
| Examiner-marked examples | May create copyright, privacy, or assessment integrity risk. |
| Protected ladder outputs | Reveal calibration targets and route behaviour. |
| Internal JSON traces | Reveal evidence flow, internal signals, and scoring paths. |
| Run logs | May reveal engine state, filenames, versions, or private data. |
| Private snapshots | May expose historical implementation and sensitive logic. |

If there is doubt, the file should remain private.

---

## 4. Rule of Abstraction

Public documents may describe what NXORA does at a conceptual level.

They should not disclose exactly how the private engine does it.

Safe:

> NXORA uses a permission-based evidence model to separate detected signals from authorised scoring influence.

Unsafe:

> Publishing exact rule conditions, thresholds, scoring weights, route gates, or validator formulas.

The public repo should show the shape of the system, not the executable recipe.

---

## 5. Rule of Synthetic Demonstration

Public examples should use synthetic, invented, or heavily simplified material.

They should not use:

- real student scripts
- protected examiner scripts
- official mark scheme excerpts beyond brief fair-use discussion
- private calibration outputs
- internal JSON traces
- screenshots showing exact route internals

Synthetic examples are useful because they demonstrate the idea without exposing sensitive evidence or private development material.

---

## 6. Rule of No Exact Thresholds

The public repository should avoid exact private scoring thresholds.

Safe language:

- cautious recovery
- protected route
- higher-level access
- safety blocker
- maturity signal
- examiner-rewardable behaviour

Unsafe language:

- exact cut-off values
- exact numerical route requirements
- exact formulas
- exact weighted contribution rules
- exact full-mark access conditions

The public repo can explain governance without publishing the key.

---

## 7. Rule of No Private Calibration Ladders

Protected calibration ladders should remain private.

They may contain:

- target scripts
- reference marks
- route behaviour
- error patterns
- protected regression checks
- full internal scoring outcomes

Public summaries may say that NXORA uses protected calibration ladders, but should not publish the ladder itself.

---

## 8. Rule of No Engine Reconstruction

A reader should not be able to reconstruct NXORA from this repository.

The repository may show:

- purpose
- philosophy
- public architecture
- safety boundaries
- high-level calibration principles

It should not show:

- enough code to rebuild the engine
- enough thresholds to copy the scoring behaviour
- enough examples to reverse-engineer route logic
- enough traces to infer private validators

The repository is a showcase, not the engine.

---

## 9. Safe GitHub Practice

The repository should remain public-safe by default.

Before uploading any new file, ask:

- Does this reveal private implementation?
- Does this reveal exact scoring logic?
- Does this expose protected calibration material?
- Does this include real examiner or student content?
- Could someone use this to replicate the engine?
- Could this weaken NXORA’s future commercial value?

If the answer might be yes, do not upload it.

---

## 10. Current Safety Controls

The repository currently uses:

- a public-safe README
- a private-file `.gitignore` boundary
- high-level documentation only
- no private engine code
- no anchors or weights
- no gold scripts
- no protected outputs
- no internal JSON traces

These controls should be preserved as the repository grows.

---

## Summary

NXORA Calibration Lab is designed to demonstrate engineering quality, not expose the engine.

The public boundary is simple:

> Explain the architecture. Protect the implementation.

This repository should help people understand that NXORA is serious, disciplined, auditable, and carefully governed, while keeping the private system safe.
