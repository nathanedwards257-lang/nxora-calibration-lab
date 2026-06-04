 # NXORA Calibration Philosophy

This document explains the public-safe calibration philosophy behind NXORA.

It does not disclose private engine code, scoring thresholds, anchors, weights, examiner scripts, protected ladder results, or internal route logic.

NXORA is being developed as a deterministic examiner-behaviour calibration system. Its aim is not simply to produce a mark, but to make scoring behaviour more disciplined, explainable, and resistant to shallow signal inflation.

---

## 1. Core Calibration Question

NXORA is built around one central question:

> Can a deterministic system recognise genuine essay quality without being misled by surface-level signals?

In essay assessment, weak answers can sometimes look stronger than they are.

They may include:

- economic keywords
- evaluation phrases
- connective language
- long paragraphs
- repeated judgement words
- broad topic relevance

But these features do not automatically prove high-quality reasoning.

NXORA calibration is therefore focused on separating visible signals from examiner-rewardable behaviour.

---

## 2. Calibration Is Not Score-Chasing

NXORA calibration does not mean forcing the system to match one script at any cost.

A scoring change is not automatically good just because it improves one example.

A good calibration change must be tested against wider behaviour.

It should ask:

- Did the change reduce a real error?
- Did it create a new over-score risk?
- Did it damage a script that was already correct?
- Did it improve the explanation of the outcome?
- Did it preserve deterministic repeatability?
- Did it move the system closer to examiner realism?

This is why NXORA treats calibration as behavioural engineering, not simple mark adjustment.

---

## 3. The Calibration Cycle

NXORA development follows this cycle:

**Observe → Map → Diagnose → Preserve → Refine**

Each stage has a specific purpose.

| Stage | Purpose |
|---|---|
| Observe | Review how the system currently behaves. |
| Map | Identify where errors, risks, and patterns appear. |
| Diagnose | Understand why the system is over-scoring or under-scoring. |
| Preserve | Protect correct behaviour before making changes. |
| Refine | Make controlled improvements and retest. |

The order matters.

Refinement should not happen before diagnosis.

---

## 4. Over-Scoring Risk

Over-scoring happens when a response is trusted too much.

Public-safe examples include:

- weak evaluation being treated as strong evaluation
- repeated connectors being treated as deep analysis
- topic relevance being mistaken for question focus
- visible density being mistaken for maturity
- a near-miss response being allowed through a protected route
- a good answer being treated as full-mark rare when it is not

Over-scoring is dangerous because it weakens trust.

If the system gives high outcomes too easily, the whole scoring model becomes less credible.

---

## 5. Under-Scoring Risk

Under-scoring happens when a response is trusted too little.

Public-safe examples include:

- compact but complete answers being treated as thin
- restrained judgement being missed because it lacks obvious signposting
- mature reasoning being overlooked because it is not very long
- integrated evaluation being missed because it is implicit
- coherent argument structure being undervalued

Under-scoring is also dangerous.

A reliable assessment system must not only block false high scores. It must also recover genuinely strong responses when the evidence supports it.

---

## 6. Protected Calibration Ladder

NXORA uses the idea of a protected calibration ladder.

This means test cases are used to check whether changes improve the system without causing regression.

A protected ladder should include different types of responses, such as:

- weak responses
- mid-level responses
- clear but not mature responses
- mature but compact responses
- strong responses
- near-miss responses
- prompt-drift responses
- full-mark rarity tests

The aim is to check the shape of system behaviour, not just one isolated result.

---

## 7. Preservation Before Refinement

A key NXORA rule is:

> Do not damage correct behaviour while fixing incorrect behaviour.

Before changing a scoring route or validation rule, the system should identify which behaviours are already working.

These must be preserved.

For example, if a system correctly protects against false high-level answers, a new recovery route should not accidentally reopen that danger.

Good calibration improves one weakness without breaking existing strengths.

---

## 8. Controlled Recovery

Some scripts may be under-recognised.

NXORA uses the public-safe idea of controlled recovery to describe cautious movement upward when evidence supports it.

Controlled recovery should not mean:

- automatic A-band access
- automatic full-mark access
- rewarding compactness by itself
- rewarding maturity signals without validation

It should mean:

- the response was genuinely under-recognised
- evidence has been validated
- blockers do not apply
- the recovery range is limited
- the system remains auditable

Recovery is a safety-controlled correction, not a shortcut.

---

## 9. Blockers and Safety Controls

Blockers are used to prevent unsafe promotion.

They help stop the system from trusting evidence that looks strong but is not strong enough.

Public-safe blocker examples include:

- evaluation theatre
- false high-level recognition
- route near-miss behaviour
- prompt drift
- full-mark rarity failure
- thinness or basicness

Blockers are important because high-level scoring should require more than strong-looking language.

---

## 10. Deterministic Repeatability

NXORA is designed around deterministic repeatability.

The same input, under the same conditions, should produce the same output.

This matters because assessment systems need consistency.

A calibration change should preserve:

- stable execution
- repeatable outputs
- traceable decisions
- clear audit evidence
- explainable behaviour

A system that cannot repeat its own decisions cannot be trusted as an assessment tool.

---

## 11. Explainability

Calibration is not complete unless the system can explain its behaviour.

A useful assessment system should be able to show:

- what evidence was detected
- what evidence was validated
