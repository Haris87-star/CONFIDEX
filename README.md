# CONFIDEX: Intelligent Confidential Data Protection & Real-Time Exfiltration Alerting

**Theme:** *Detect → Understand → Score → Alert → Investigate → Respond*  
**Event:** IdeateBLR Ideathon 2026  
**Developed by:** Harish P (Harish Hari) & Team Zenith  
**Affiliation:** Department of Computer Science & Engineering, Vijaya Vittala Institute of Technology (VVIT / VTU), Bengaluru  

---

## 🛡️ 1. Executive Summary

**CONFIDEX** is an intelligent organizational data-protection platform designed to detect suspicious attempts to copy, move, or transfer confidential information. 

Instead of treating every raw file operation as a security incident, CONFIDEX dynamically combines **file sensitivity**, **user context**, **device trust**, **destination risk**, **transfer volume**, **policy rules**, and **behavioral anomalies** to determine the real-time seriousness of an event. When risky activity is detected, the platform creates an incident and provides an actionable, prioritized alert to an authorized manager or security officer.

---

## ⚠️ 2. The Problem We Are Solving

Organizations protect sensitive assets such as:
- Proprietary source code & repositories
- Customer & financial records
- Strategic business plans & research data
- Employee confidential records & trade secrets

A major security gap is that authorized personnel with legitimate credentials can intentionally or accidentally exfiltrate confidential data using untrusted USB drives, unsanctioned cloud drives, or private messaging channels. Conventional monitoring tools flood administrators with thousands of raw logs (e.g. *"file copied"*) without context, leading to alert fatigue and delayed incident response.

---

## 🏗️ 3. System Architecture & Detection Pipeline

CONFIDEX introduces a multi-tier threat classification pipeline:

1. **Endpoint Activity Sensor:** Low-overhead file and peripheral monitor tracking file copy, rename, delete, and bulk write operations.
2. **Contextual Metadata Enrichment:** Evaluates file sensitivity tags, target device UUID, USB volume serial, network destination, and user privilege level.
3. **Multi-Vector Risk Scoring Engine:** Evaluates 7 risk factors in real-time to compute a standardized Exfiltration Risk Score (0–100).
4. **Automated Alerting & Action Engine:** Triggers instant notifications, isolates rogue sessions, and logs verifiable forensic audit trails.

---

## 📊 4. Multi-Vector Risk Scoring Formula

```text
Risk Score = w1*(Sensitivity) + w2*(Destination Trust) + w3*(Volume/Velocity) + w4*(Temporal Anomaly) + w5*(User Baseline)
```

- **Low Risk (0–39):** Normal business operation; passive telemetry logging.
- **Medium Risk (40–69):** Elevated anomaly (e.g., bulk copy to personal device); manager notification generated.
- **High / Critical Risk (70–100):** Suspected unauthorized exfiltration; real-time USB transfer block, session containment, and automated incident triage.

---

## 📂 5. Pitch Presentation & Project Assets

This repository includes the complete ideathon pitch deck slides (1–10) and comprehensive project summary documentation submitted for the IdeateBLR Ideathon:
- `CONFIDEX_Ideathon_Project_Summary.docx` — Complete functional specification and threat response blueprint.
- Slides `1.jpg` through `10.jpg` — Ideathon presentation visuals covering problem, solution, architecture, market impact, and implementation timeline.
