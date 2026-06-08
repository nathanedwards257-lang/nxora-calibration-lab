# Calibration Evidence Warehouse

## Introduction

NXORA is being developed as a deterministic examiner-behaviour calibration project.

A key challenge in deterministic assessment work is not simply producing an output.

The harder challenge is preserving enough evidence to understand why a system behaved as it did, whether that behaviour was reliable, and whether future changes improve or damage calibration quality.

The Calibration Evidence Warehouse is a public-safe architectural concept for storing, organising, and reviewing calibration evidence across repeated system runs.

This document explains the concept at a high level.

It does not disclose private engine code, scoring thresholds, examiner materials, protected calibration datasets, route logic, anchors, weights, validators, governors, or implementation details.

---

## The Core Problem

Calibration systems can become unreliable when evidence is scattered across:

- terminal outputs
- screenshots
- one-off reports
- temporary JSON files
- manual notes
- isolated script comparisons

This creates several risks:

- important evidence may be lost
- repeated failure patterns may be missed
- patch decisions may become reactive
- regressions may be harder to detect
- future changes may lack a stable comparison baseline

A serious calibration system needs memory.

The Calibration Evidence Warehouse exists to support that memory.

---

## Purpose of the Warehouse

The warehouse is designed to preserve calibration evidence in a structured and repeatable way.

Its purpose is to help answer questions such as:

- What changed between calibration runs?
- Which failure classes keep appearing?
- Which scripts serve as regression guards?
- Which behaviours are stable?
- Which behaviours remain unsafe?
- Which future patches are justified by evidence?
- Which proposed changes create unacceptable risk?

The warehouse does not replace judgement.

It gives judgement a stronger evidence base.

---

## Public-Safe Warehouse Structure

A public-safe warehouse may be described using the following conceptual structure:

```text
calibration_evidence_warehouse/
├── 00_schema/
├── 01_build_scripts/
├── 02_data_exports/
├── 03_reports/
└── README.md
