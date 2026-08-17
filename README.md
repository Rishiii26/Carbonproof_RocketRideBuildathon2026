# Carbonproof_RocketRideBuildathon2026
AI verification layer that cross-checks self-reported carbon claims against real operational data (sensors, energy, production) to flag inconsistencies before they reach a regulator or auditor.
# CarbonProof

**An AI Verification Layer for Carbon Claims**

Built for **SGU × RocketRide AI-Thon 2026** by Team Teen Titans Go

---

## The Problem

> They claimed 20%. Their sensors said 9%.

Self-reported carbon claims and a company's own operational data disagree far more often than anyone checks:

- **~74%** of S&P 500 firms have restated emissions data
- **135M+** tons unreported in original disclosures
- **~13.5%** higher emissions reported by "assured" companies
- **~9.5%** higher carbon intensity vs. unaudited peers

*Sources: HBS Institute for Business in Global Society (Dec. 2025); MIT Sloan — Berg, Huidobro & Rigobon*

Self-reported figures submitted for ESG/regulatory disclosure are difficult to independently validate when supporting evidence is fragmented across sensors, meters, and documents. These claims aren't occasional outliers — they're structurally unverified until an external, evidence-based check is applied.

## The Solution

CarbonProof uses AI to cross-verify industrial carbon claims against real operational evidence — detecting anomalies and estimating whether reported emission reductions are genuinely supported by the data.

Built for **carbon auditors and ESG assurance teams** as a continuous evidence layer — **not a replacement for the auditor.**

```
Carbon Claim + Operational Data + Documents
              ↓
       AI Verification Layer
              ↓
     Evidence Cross-Validation
              ↓
       Explainable Verdict
```

## A Five-Module AI Verification Stack

| Module | Function | Status |
|---|---|---|
| **Claim Consistency Engine** | Cross-source consistency analysis validates reported reductions against independent operational evidence | Prototyped |
| **Anomaly Detection** | Time-series anomaly detection flags irregular sensor and operational patterns | Prototyped |
| **Predictive Emissions Model** | Regression-based modeling sets the emissions baseline the Consistency Engine checks each claim against | Prototyped |
| **Document AI** | OCR and information extraction pull figures from reports, invoices, and certificates | Planned |
| **Explainable AI Audit Agent** | Confidence-scored, human-in-the-loop reasoning explains each verdict | Planned |

**Core differentiator:** the Claim Consistency Engine doesn't run anomaly detection in isolation — it cross-correlates each claim against 3+ independent operational signals at once (energy draw, throughput, sensor telemetry). A claim can look normal against any single signal and still be flagged when the joint pattern is inconsistent.

### vs. the status quo

| | Traditional Audit | CarbonProof |
|---|---|---|
| Cadence | Periodic, sampled | Continuous, 100% screening |
| Method | Manual | Automated pre-screen |
| Turnaround | Weeks per cycle | Near real-time |

Manual third-party audits (DNV, SGS, Bureau Veritas) rely on periodic, sampled review. Existing AI-based ESG platforms (Persefoni, Watershed, Sweep) largely automate emissions *calculation* from self-reported inputs — they don't cross-check the claim against independent operational signals. CarbonProof validates the claim itself.

## Worked Example

| Claim | Operational Signal | Flag | Verdict |
|---|---|---|---|
| "20% Scope 1 reduction, Q3 2026" | Energy draw −6%, production −4% → implied max ~9–10% | Inconsistent — claim exceeds signal by ~10 pts | 82% confidence — **Requires Human Audit** |

Confidence score = weighted agreement across signals (energy, throughput, telemetry) minus the regression model's residual error.

**Output categories:** Verified · Consistent · Inconsistent · Requires Human Audit

## System Architecture

```
DATA SOURCES          PROCESSING             AI INTELLIGENCE            VERIFICATION
─────────────         ──────────             ────────────────           ────────────
IoT / CO₂ sensors  →  Cleaning &          →  Anomaly + predictive   →   Evidence correlation
Energy & production   normalization          models                     Confidence scoring
  data                Feature extraction     Claim consistency          Explainable reasoning
Reports &              Time-series            engine
  certificates          alignment             Document AI
```

**Data handling:** Role-based access control; data encrypted at rest and in transit; raw sensor/production data stays in the customer's environment.

**Pilot status:** Core pipeline (ingestion → anomaly detection → consistency scoring) is prototyped against a partnered manufacturer's dataset (~150 claims/yr, 12 mo. of data). Document AI and explainability are near-term. Today's output is the flag + confidence score above.

## Expected Impact

*Illustrative impact model — projected/estimated, modeled on a mid-size manufacturer reporting ~150 claims/year where manual sampled audit covers ~20–30% of claims at ~2–3 auditor-days each. No live pilot outcomes exist yet.*

- **100%** of claims screened continuously (vs. ~25% under sampled manual audit)
- **~15%** of high-risk claims pre-flagged for priority human review
- **40–60%** estimated auditor triage-time reduction vs. manual sampled review

| Dimension | Value |
|---|---|
| **Environmental** | Strengthens credibility of reported carbon reductions; helps identify potentially inconsistent emissions claims |
| **Operational** | Automates preliminary cross-checking of fragmented evidence; pre-flags high-risk claims ahead of manual review |
| **Governance** | Creates an auditable, evidence-based trail per claim; flags inconsistencies before third-party assurance, avoiding late-stage restatements |
| **Business** | SaaS pre-screening layer priced per-claim/per-report; buyers = assurance firms and large emitters facing CSRD/SEC-aligned mandates; addressable base ~50K CSRD-covered EU entities by 2026, plus SB 253 and SEC-aligned filers |

## Roadmap

1. **Prototype Validation** — core pipeline against a partnered industrial dataset
2. **Real-Time IoT Integration** — continuous claim monitoring
3. **Remote-Sensing Integration** — satellite data as independent evidence
4. **Advanced Multimodal AI** — fuses satellite & sensor data by sector
5. **Scalable Infrastructure** — for auditors, manufacturers, regulators, ESG

### Why now?

EU CSRD now requires third-party assurance for first-wave large entities on FY2024 data; California SB 253 and Australia's climate-disclosure regime are phasing in comparable assurance mandates — expanding the buyer base for a continuous, audit-ready verification layer.

### What we're looking for

A pilot partner (manufacturer or assurance firm) and mentorship to move Document AI and the Explainable AI Audit Agent from planned to prototyped.

---

## Repo Contents

- `TeenTitansGo_CarbonProof_RocketRideBuildathon2026.pptx` — full pitch deck

## Team

Team **Teen Titans Go** — SGU × RocketRide AI-Thon 2026
