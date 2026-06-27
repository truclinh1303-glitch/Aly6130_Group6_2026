# Enterprise Risk Assessment — Amazon's Proposed Acquisition of an AI-Powered Last-Mile Delivery Optimization Platform (RIVR)

> **ALY 6130 — Risk Management Analytics · Northeastern University · Group 6**
> A term-long enterprise risk management (ERM) analytics project that assesses the risks and opportunities of Amazon's proposed acquisition of an AI-powered last-mile delivery optimization platform, moving from qualitative identification to a fully reproducible quantitative model.

![Course](https://img.shields.io/badge/Course-ALY%206130-232F3E)
![Frameworks](https://img.shields.io/badge/Frameworks-ISO%2031000%20%C2%B7%20COSO%20ERM%20%C2%B7%20NIST%20AI%20RMF-FF9900)
![Made with](https://img.shields.io/badge/Made%20with-Python%20%C2%B7%20Jupyter-146EB4)

---

## Overview

Amazon moves roughly **8 million packages per day** at an estimated **$14–$17 per residential package**, and the last mile accounts for **50–60% of total parcel cost** (BCG, 2026). In March 2026, Amazon acquired RIVR, an AI-powered last-mile route-optimization platform spun out of ETH Zurich's Robotic Systems Lab, to close its optimization gap against incumbents such as UPS ORION ($300–400M/yr savings, 14 years to build), FedEx Surround (~15M shipments/day), and Oracle/SAP TM ($5M–$30M switching cost per client).

This repository documents a complete ERM analysis of that acquisition, organized by course assignment (Modules 1–4) with a final consolidated **Signature Assignment**, and grounded in **ISO 31000:2018**, **COSO ERM (2017)**, and the **NIST AI RMF 1.0 (2023)**. It progresses from a SWOT analysis and a 32-risk register, through qualitative Scenario Analytics and Industry Fusion Analytics, to a quantitative model combining Indicators & Warning (I&W) analysis, a 50,000-trial Monte Carlo simulation, and machine-learning early-warning detection — and closes with response strategies and a KRI monitoring framework.

---

## Repository structure

```
.
├── README.md
├── LICENSE
├── .gitignore
│
├── Assignment 1                                      # Module 1 — assignment brief
├── Data Source References                            
├── Group6_benchmark_parameters-1-assignment 4.csv
├── Group6_indicator-1-assignment 4.csv              
│
├── Assignment_2/                                     # Module 2 — problem statements + KRIs, risk register
│   ├── Assignment2_Problem_Statement.md
│   └── Assignment2_Risk_Register.md
│
├── Assignment_3/                                     # Module 3 — qualitative heat-map assessment (revised)
│   ├── A3_HeatMap_Python.ipynb
│   ├── A3_Risk_Calculator.md
│   ├── A3_Risk_HeatMap_Report.md
│   ├── REVISED_risk_heatmap_report
│   ├── REVISED_risks_calculator
│   └── Assignment 3 update.zip
│
├── Assignment 4/                                     # Module 4 — I&W quant, Monte Carlo, ML, response & mitigation
│   ├── Group6_IW_Quantitative_Risk_Assessmen.ipynb
│   ├── Group6_Risk_Mitigation.md
│   ├── Group6_benchmark_parameters.csv
│   └── Group6_indicator.csv
│
└── Signature Assignment/                            # Final consolidated deliverable
    ├── data/
    │   ├── Risk_HeatMap_Risk_Register.xlsx           
    │   ├── benchmark_parameters.csv                 
    │   └── market_indicator.csv                      
    ├── notebooks/
    │   ├── IW_Quantitative_Risk_Assessmen.ipynb      
    │   └── Risk_calculator_Notebook.ipynb            
    └── report/
        ├── Group6_Final_Report 1.pdf                 
        └── Group6_Presentation.pdf    
```

> **Module → deliverable map**
> - **Module 1 (Assignment 1 + SWOT docx):** SWOT analysis, stakeholder/PESTLE/pre-mortem brainstorming, preliminary risk factors and controls.
> - **Module 2 (`Assignment_2/`):** Three competitive problem statements with KRIs; the initial risk register and scoring scales.
> - **Module 3 (`Assignment_3/`):** Probability × Impact heat-map assessment and risk calculator; the `REVISED_*` files hold the consolidated 32-risk register — the canonical source for risk names, scores, and severity.
> - **Module 4 (`Assignment 4/`):** Indicators & Warning analysis, Beta/PERT distributions, the 50,000-trial Monte Carlo simulation, ML early-warning models, and risk response strategies.
> - **Signature Assignment (`Signature Assignment/`):** The final aggregated report, presentation, reproducible notebook, and supporting data — the single deliverable that brings the full term's work together.

---

## The problem

Amazon's last-mile network faces compounding, interconnected risks — financial overpayment, operational disruption, competitive displacement, cybersecurity breach, algorithmic bias, low user adoption, vendor lock-in, and regulatory non-compliance — that cannot be managed without a comprehensive ERM framework governing every phase of the platform's acquisition, integration, and operation. Left unmanaged, they erode acquisition ROI, weaken Amazon's competitive position, and expose the company to CCPA, EU AI Act, and antitrust enforcement.

**Quantified stakes:**
- **$400M–$1.36B/yr** in unrealized savings if routing efficiency is not captured (10–25% per-package reduction × 8M daily packages at $14–$17 each)
- **$10.22M** average US data-breach cost (IBM, 2025)
- **~$50.2B** EU AI Act exposure — 7% of FY2025 revenue of $716.9B
- **$7,500/violation** CCPA, across 200M+ Prime customers

---

## The consolidated risk register

Risk identification began with five structured brainstorming techniques (stakeholder mapping, PESTLE scan, pre-mortem, process mapping, KRI brainstorming), producing 60 candidate risks consolidated to **32 distinct negative risks across 7 categories** and a separate register of **4 opportunities**.

| # | Category | Risks | Count | VH / H | Highest-severity risk (score) |
|---|----------|-------|-------|--------|-------------------------------|
| 1 | AI Strategy & Governance | R1–R4 | 4 | 1 / 1 | R1 AI strategy failure (56) |
| 2 | AI Decision Quality | R5–R9 | 5 | 2 / 0 | R7 Peak-ops system downtime (63) |
| 3 | Cybersecurity & Privacy | R10–R13 | 4 | 0 / 2 | R10 Breach of AI platform (45) |
| 4 | Algorithmic Bias & Fairness | R14–R17 | 4 | 0 / 2 | R14 Delivery-zone bias (45) |
| 5 | Vendor & Third-Party Dependency | R18–R21 | 4 | 0 / 2 | R18 Vendor lock-in (42) |
| 6 | Financial & ROI | R22–R26 | 5 | 3 / 2 | R26 Cost of lagging in AI adoption (72) |
| 7 | Legal & Regulatory Compliance | R27–R32 | 6 | 1 / 2 | R27 EU AI Act non-compliance (56) |

**Severity distribution: 7 Very High · 11 High · 14 Moderate · 0 Low.** The portfolio clusters in the upper-middle of the Likelihood × Impact grid — high-consequence, mid-likelihood — not in the extreme tails. R7 (peak-operations downtime, score 63) and R26 (cost of lagging in AI adoption, score 72) occupy the highest-severity cells.

**Scoring scale:** Likelihood (1/3/5/7/9) × Impact (1/2/4/6/8/9), max score 81. Severity tiers: Very High (≥54), High (40–53), Moderate (18–39), Low (<18).

**Opportunities register (separate):**
1. AI route-efficiency cost savings — 9×8 = 72 (High)
2. Competitive market leadership — 56 (High)
3. Platform commercialization — 30 (Medium)
4. Sustainability and ESG gains — 28 (Medium)

---

## The three priority risks

From the consolidated register, three risks were selected for deep quantitative analysis, labeled **PR1–PR3** to avoid clashing with the register's own R1–R3 numbering.

| ID | Risk | Type | Register cross-reference | Qualitative score |
|----|------|------|--------------------------|-------------------|
| **PR1** | Commercial market-entry / enterprise win-rate failure | Threat | R26 + opportunities O2/O3 | 7 × 6 = 42 (High) |
| **PR2** | Cybersecurity breach of geolocation & address data | Threat | R10 + R11 | 5 × 9 = 45 (High) |
| **PR3** | Cost-reduction & sustainability leadership | Opportunity | Opportunity O1 | 9 × 8 = 72 (High upside) |

**PR1** — Amazon enters the commercial logistics-software market without a sales-engineering or SLA capability, allowing incumbents (ORION, Surround, Oracle, SAP) to leverage lock-in and push enterprise win-rate below 40%, eroding acquisition ROI. The platform's data from 8M daily stops cannot be monetized externally without a fully developed enterprise sales function.

**PR2** — A new attack surface (driver geolocation, customer addresses, delivery photos, carrier APIs) is exposed before zero-trust controls are deployed, enabling ransomware or unauthorized API access and triggering CCPA 72-hour notification. A breach turns Amazon's data-density advantage into a multi-jurisdictional liability. Asymmetric profile: moderate probability but extreme regulatory and reputational tail.

**PR3** — AI optimization across 8M daily packages delivers 15–25% per-package cost reduction ($400M–$1.36B savings) and CO₂ cuts, while pre-compliance with California Clean Miles becomes a competitive moat. Every year of delay forfeits another year of ORION's compounding $400M advantage.

---

## Qualitative assessment

Two methods from Fleisher & Bensoussan (2015) were applied: **Scenario Analytics** (Ch. 22) and **Industry Fusion Analytics** (Ch. 17).

| Risk | Base-case scenario | Industry-fusion benchmark | Proceed? |
|------|--------------------|--------------------------|----------|
| PR1 | Win-rate settles near 38% for three quarters; positive internal ROI but missed external targets. | Oracle–PeopleSoft (36-mo ramp); Google Cloud (<30% win-rate for 3 yrs despite better tech). | Yes |
| PR2 | Months 6–9 are peak exposure; attack detected via geo-API anomaly before exfiltration. | IBM 2025 ($10.22M US avg); 33% logistics AWS credentials exposed; Colonial Pipeline ($4B+). | Yes |
| PR3 | Adoption ~70% in 12 months; ~14% per-package reduction ≈ $490M/yr. | UPS ORION ($300–400M/yr); Walmart (30%); Shuaibu et al. (15–25%). | Yes |

> **Key insight:** the commercial maturity of the logistics-software market — not the technology — is the primary source of PR1 risk.

---

## Key quantitative results

Reproduced from `Signature Assignment/notebooks/IW_Quantitative_Risk_Assessmen.ipynb` (`SEED = 42`, 50,000 Monte Carlo trials). All real-world dollar figures are anchored to official sources in `benchmark_parameters.csv`. The indicator panel in `market_indicator.csv` is **synthetic and seeded**, with magnitudes calibrated to those benchmarks.

| Risk | I&W P(event) | E[Impact] | EMV | P95 exposure | ML ROC-AUC | Dominant early-warning signal | Treatment | Residual EMV |
|------|-------------|-----------|-----|--------------|------------|-------------------------------|-----------|--------------|
| **PR1** | 0.65 | $567M | −$368M | $890M downside | 0.87 (GBM) | sales-engineering vacancy gap (2–3 mo lead) | Mitigate | −$239M (−35%) |
| **PR2** | 0.47 | $492M | −$231M | $701M downside | 0.89 (GBM) | anomalous geolocation-API traffic (15–45 day lead) | Mitigate + Transfer | −$104M (−55%) |
| **PR3** | 0.62 | +$733M | +$453M | +$991M upside | 1.00 (Logistic) | driver adoption of AI routes | Exploit + Enhance | +$534M (+18%) |

**Net portfolio expected value after treatment: +$191M** (−$239M PR1, −$104M PR2, +$534M PR3), before the strategic option value of owning the platform.

**I&W indicator panel:**

| Risk | Leading indicators (weights) | Mean warning | Blended P(event) |
|------|------------------------------|-------------|-----------------|
| PR1 | win-rate gap (.40), competitor releases (.20), sales-eng vacancy (.20), benchmark deficit (.20); red at ≥0.55 | 0.61 | 0.7×0.61 + 0.3×0.743 ≈ 0.65 |
| PR2 | critical vulns past 15-day SLA (.35), anomalous geo-API (.25), zero-trust gap (.25), MTTR days (.15) | 0.44 | 0.7×0.44 + 0.3×0.540 ≈ 0.47 |
| PR3 | per-package cost reduction (.40), driver adoption (.25), OTDPI (.20), pilot on-target (.15) | 0.44 | (1−warn) blended w/ anchor 0.748 ≈ 0.62 |

![Monte Carlo simulation of risk exposure]
<img width="2223" height="582" alt="figure2_monte_carlo" src="https://github.com/user-attachments/assets/c3c948a6-a063-43d6-92d0-ed9e44fdb3c0" />
> Monte Carlo simulation of risk exposure (50,000 trials). Gold line = expected impact; dashed line = P95 (downside for PR1/PR2, upside for PR3).

---

## Risk response strategy

| Risk | Strategy | Residual EMV | KRI red trigger |
|------|----------|-------------|-----------------|
| PR1 | Mitigate | −$239M (−35%) | Win-rate <40% for 2 consecutive quarters; sales-eng headcount <75% |
| PR2 | Mitigate + Transfer | −$104M (−55%) | Any confirmed unauthorized geo/address API access; any critical vuln >15 days; zero-trust coverage <90% |
| PR3 | Exploit + Enhance | +$534M (+18%) | Per-package reduction <5%; driver adoption <60% (or <80% after 6 months); OTDPI <97 for 2 months |

**PR1 — Mitigate:** Pre-launch benchmarking vs ORION/Surround; hire 15–20 enterprise sales engineers before first RFP; tiered introductory pricing within FTC conduct limits; pause external commercialization if win-rate <40% for 2 quarters.

**PR2 — Mitigate + Transfer:** Zero-trust as a hard launch gate before any live customer data flows; API gateway with anomaly detection and CISO escalation within 15 min; logistics-specific cyber insurance up to $50M/incident; tested delivery-data incident-response playbook meeting 72-hour CCPA notification requirement.

**PR3 — Exploit + Enhance:** Scale from 3-city pilot to 50+ stations in 18 months; driver-adoption program targeting 80% per market within 6 months; pre-comply with California Clean Miles Standard; public CO₂ KPI benchmarked against ORION's 100M-miles reduction.

---

## KRI monitoring framework (CRISP-DM aligned)

Every KRI provides 30–90 days of advance warning, drawing on the dominant ML signal for its risk.

| Risk | KRI metric | Green | Amber | Red — trigger & response | Freq. |
|------|-----------|-------|-------|--------------------------|-------|
| PR1 | Enterprise win-rate vs ORION/Surround | ≥50% | 40–49% | <40% for 2 quarters → pause commercialization + VP review | Qtrly |
| PR1 | Sales-engineering headcount vs target | ≥90% | 75–89% | <75% → emergency recruiting + CEO escalation | Monthly |
| PR2 | Critical vulns past 15-day SLA | Zero | 1–2 near limit | Any vuln >15 days → patch sprint + board notice | Weekly |
| PR2 | Anomalous geo-API / unauthorized access | Zero | Elevated volume | Any confirmed access → API lockdown + CCPA 72h clock | Continuous |
| PR3 | Per-package cost reduction vs baseline | ≥15% | 5–14% | <5% → suspend expansion + model audit | Monthly |
| PR3 | Driver adoption of AI routes | ≥80% | 60–79% | <60% (or <80% after 6 mo) → DSP review + incentives | Monthly |

---

## Recommendation

**Proceed — under an active ERM program — with three non-negotiable conditions:**

1. **Zero-trust** before any live customer-data integration (PR2 carries the highest tail at $701M P95 despite moderate probability — zero-trust is a launch gate, not an IT project)
2. **Pre-launch sales-engineering team of ≥15 FTEs** before first RFP (PR1's $368M EMV is addressable by closing this gap before launch)
3. **80% driver-adoption target per market**, monitored monthly with authority to pause expansion if not met (PR3's +$453M to +$991M upside erodes by ~$400M for every year of delay against ORION)

Regulatory inputs (EU AI Act, CCPA, Clean Miles) are model inputs, not background — they calibrate the distributions directly.

---

## Methodology

1. **Risk identification (Modules 1–2).** SWOT analysis plus five brainstorming techniques produced 60 candidate risks, consolidated to 32 distinct risks across 7 categories.
2. **Qualitative assessment (Module 3).** Probability × Impact heat map (likelihood 1/3/5/7/9 × impact 1/2/4/6/8/9, max 81) with four severity tiers, refined through Scenario Analytics and Industry Fusion Analytics (Fleisher & Bensoussan, 2015, Ch. 22 and 17).
3. **Quantitative assessment (Module 4 + Signature Assignment).** I&W analysis converts leading indicators into calibrated probabilities; Beta/PERT distributions produce EMV, variance, and P95 exposure; a 50,000-trial Monte Carlo simulation models the full exposure distribution; Gradient-Boosting and Logistic-Regression classifiers (5-fold stratified cross-validation) confirm each warning state is detectable in advance.
4. **Response and monitoring.** Four standard ISO 31000 treatments (Mitigate, Transfer, Exploit/Enhance, Accept) with residual EMV, plus a CRISP-DM-aligned KRI framework with green/amber/red trigger points.

---

## How to reproduce

```bash
# 1. Clone
git clone https://github.com/truclinh1303-glitch/Aly6130_Group6_2026.git
cd Aly6130_Group6_2026

# 2. Install dependencies
pip install numpy pandas scipy scikit-learn matplotlib jupyter openpyxl

# 3. Run the analysis
#    Open the notebook below and run all cells. This regenerates the EMV / P95
#    results, ROC-AUC scores, and the Monte Carlo figure.
jupyter notebook "Signature Assignment/notebooks/IW_Quantitative_Risk_Assessmen.ipynb"
```

---

## Frameworks and key references

- International Organization for Standardization. (2018). *ISO 31000:2018 Risk management — Guidelines.*
- Committee of Sponsoring Organizations of the Treadway Commission. (2017). *Enterprise risk management — Integrating with strategy and performance.*
- National Institute of Standards and Technology. (2023). *Artificial intelligence risk management framework (AI RMF 1.0).*
- Fleisher, C. S., & Bensoussan, B. E. (2015). *Business and competitive analysis* (2nd ed.). FT Press.
- BCG. (2026). Last-mile delivery accounts for 50–60% of total parcel costs.
- IBM Security. (2025). *Cost of a data breach report 2025.*
- INFORMS. (2016). *UPS ORION — Franz Edelman Award.*
- CCJ Digital. (2026). Supply chain cyber threats: How malicious AI puts logistics data at risk.
- Deep Tech Nation Switzerland. (2026). Amazon acquires RIVR: An ETH Zurich robotics spinout.
- Shuaibu, A. S., Mahmoud, A. S., & Sheltami, T. R. (2025). A review of last-mile delivery optimization. *Drones, 9*(3), 158.
- Skadden. (2025). M&A in the AI era: Antitrust and national-security considerations.

A full reference list appears in `Signature Assignment/report/Group6_Final_Report 1.pdf`.

---

## Team — Group 6

| Member |
|--------|
| Sandra Amponsah |
| Truc Linh Hoang |
| Victoria Kpetigo |

**Course:** ALY 6130 — Risk Management Analytics · Northeastern University
**Instructor:** Abeba Nigussie Turi
**Term:** June 2026

---

## Academic integrity & use

This repository is coursework submitted for ALY 6130 at Northeastern University. The acquisition scenario is a course case study; figures use a synthetic, benchmark-calibrated dataset and do not represent actual Amazon internal data. Please do not copy or submit this work as your own.
