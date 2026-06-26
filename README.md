# Enterprise Risk Assessment — Amazon's Proposed Acquisition of an AI-Powered Last-Mile Delivery Optimization Platform (RIVR)

> **ALY 6130 — Risk Management Analytics · Northeastern University · Group 6**
> A term-long enterprise risk management (ERM) analytics project that assesses the risks and opportunities of Amazon's proposed acquisition of an AI-powered last-mile delivery optimization platform, moving from qualitative identification to a fully reproducible quantitative model.

![Course](https://img.shields.io/badge/Course-ALY%206130-232F3E)
![Frameworks](https://img.shields.io/badge/Frameworks-ISO%2031000%20%C2%B7%20COSO%20ERM%20%C2%B7%20NIST%20AI%20RMF-FF9900)
![Made with](https://img.shields.io/badge/Made%20with-Python%20%C2%B7%20Jupyter-146EB4)

---

## Overview

Amazon moves roughly **8 million packages per day** at an estimated **$14–$17 per residential package**, and the last mile accounts for **50–60% of total parcel cost**. To close its optimization gap against incumbents such as UPS ORION and FedEx Surround, Amazon proposed acquiring RIVR, an AI-powered last-mile route-optimization platform (an ETH Zurich spin-out).

This repository documents a complete ERM analysis of that acquisition. The analysis was built across six course modules and is grounded in **ISO 31000:2018**, **COSO ERM (2017)**, and the **NIST AI RMF 1.0 (2023)**. It progresses from a SWOT analysis and a 32-risk register, through qualitative scenario and industry-fusion analytics, to a quantitative model combining Indicators & Warning (I&W) analysis, a 50,000-trial Monte Carlo simulation, and machine-learning early-warning detection — and closes with response strategies and a monitoring framework of Key Risk Indicators (KRIs).

---

## The three priority risks

From a consolidated register of 32 negative risks (7 categories) and a separate register of 4 opportunities, three priority risks were carried into deep quantitative analysis. They are labeled **PR1–PR3** to avoid clashing with the register's own R1–R3 numbering.

| ID  | Risk | Type | Register cross-reference | Qualitative score |
|-----|------|------|--------------------------|-------------------|
| **PR1** | Commercial market-entry / enterprise win-rate failure | Threat | R26 + opportunities O2/O3 | 7 × 6 = 42 (High) |
| **PR2** | Cybersecurity breach of geolocation & address data | Threat | R10 + R11 | 5 × 9 = 45 (High) |
| **PR3** | Cost-reduction & sustainability leadership | Opportunity | Opportunity O1 | 9 × 8 = 72 (High upside) |

---

## Key quantitative results

Reproduced from `notebooks/IW_Quantitative_Risk_Assessment.ipynb` (`SEED = 42`, 50,000 Monte Carlo trials).

| Risk | I&W P(event) | E[Impact] | EMV | P95 exposure | ML ROC-AUC | Dominant early-warning signal | Treatment | Residual EMV |
|------|-------------|-----------|-----|--------------|------------|-------------------------------|-----------|--------------|
| **PR1** | 0.65 | $567M | −$368M | $890M downside | 0.87 | sales-engineering vacancy gap | Mitigate | −$239M (−35%) |
| **PR2** | 0.47 | $492M | −$231M | $701M downside | 0.89 | anomalous geolocation-API traffic | Mitigate + Transfer | −$104M (−55%) |
| **PR3** | 0.62 | +$733M | +$453M | +$991M upside | 1.00 | driver adoption of AI routes | Exploit + Enhance | +$534M (+18%) |

**Net portfolio expected value after treatment: +$191M**, before the strategic option value of owning the platform.

![Monte Carlo simulation of risk exposure](figures/fig1_monte_carlo.png)

---

## Repository structure

```
.
├── README.md
├── requirements.txt
├── reports/
│   ├── 01_SWOT_Analysis_Module1.pdf                  # Module 1 — SWOT, brainstorming, preliminary controls
│   ├── 02_Problem_Statement_and_KRIs_Module2.md      # Module 2 — problem statements + KRIs
│   ├── 02_Risk_Register_Module2.md                   # Module 2 — initial risk register + scoring scales
│   ├── 03_Risk_HeatMap_Report_Module3.docx           # Module 3 — qualitative heat-map assessment
│   ├── 04_Risk_Response_and_Mitigation_Module4.docx  # Module 4 — I&W, response strategies, residual EMV
│   └── 05_Final_Report_Signature_Assessment.docx     # Signature Assessment — full aggregated report
├── register/
│   └── Risk_Register_HeatMap.xlsx                    # Canonical 32-risk register + 4-opportunity register
├── notebooks/
│   └── IW_Quantitative_Risk_Assessment.ipynb        # Reproducible quant model (I&W, Monte Carlo, ML)
├── data/
│   ├── benchmark_parameters.csv                      # Officially-sourced benchmark parameters
│   └── iw_indicator_dataset.csv                      # Synthetic indicator panel (3 risks × 4 indicators × 156 weeks)
├── figures/
│   ├── fig1_monte_carlo.png                          # Monte Carlo exposure distributions
│   └── fig2_heatmap.png                              # Probability × impact heat map
└── presentation/
    └── Group6_Presentation.pptx                     # Final presentation deck
```

> **Canonical source of truth.** `register/Risk_Register_HeatMap.xlsx` is authoritative for all risk names, numbering, scores, and severity. Where earlier deliverables differ, the revised register governs.

---

## Methodology

The project follows the ERM analytics lifecycle taught in ALY 6130:

1. **Risk identification (Module 1–2).** SWOT analysis plus five brainstorming techniques (stakeholder mapping, PESTLE scanning, pre-mortem, process mapping, KRI brainstorming) produced an initial 60 candidate risks, consolidated to 32 distinct risks across 7 categories.
2. **Qualitative assessment (Module 3).** A Probability × Impact heat map (likelihood 1/3/5/7/9 × impact 1/2/4/6/8/9, max 81) with four severity tiers, refined through Scenario Analytics and Industry Fusion Analytics (Fleisher & Bensoussan, 2015, Ch. 22 and 17).
3. **Quantitative assessment (Module 4).** Indicators & Warning analysis converts leading indicators into calibrated probabilities; Beta/PERT distributions produce EMV, variance, and P95 exposure; a 50,000-trial Monte Carlo simulation models the full exposure distribution; and Gradient-Boosting and Logistic-Regression classifiers (5-fold stratified cross-validation) confirm each warning state is detectable in advance.
4. **Response and monitoring.** Four standard ISO 31000 treatments (Mitigate, Transfer, Exploit/Enhance, Accept) with residual EMV, plus a CRISP-DM-aligned KRI framework with green/amber/red trigger points.

### Data and reproducibility

All real-world dollar figures are anchored to official sources documented in `data/benchmark_parameters.csv` (e.g., IBM Cost of a Data Breach 2025, INFORMS/UPS ORION 2016, Statista 2024). Because the target's internal KPIs are not public, the indicator panel in `data/iw_indicator_dataset.csv` is **synthetic and seeded**, with magnitudes calibrated to those benchmarks. Every reported figure regenerates exactly from the notebook's fixed random seeds — consistent with the project's no-hallucination, full-reproducibility standard.

---

## How to reproduce

```bash
# 1. Clone
git clone https://github.com/truclinh1303-glitch/Aly6130_Group6_2026.git
cd Aly6130_Group6_2026

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the analysis
jupyter notebook notebooks/IW_Quantitative_Risk_Assessment.ipynb
#    Run all cells — this regenerates the EMV/P95 figures, ROC-AUC scores,
#    and the figures in /figures.
```

---

## Frameworks and key references

- International Organization for Standardization. (2018). *ISO 31000:2018 Risk management — Guidelines.*
- Committee of Sponsoring Organizations of the Treadway Commission. (2017). *Enterprise risk management — Integrating with strategy and performance.*
- National Institute of Standards and Technology. (2023). *Artificial intelligence risk management framework (AI RMF 1.0).*
- Fleisher, C. S., & Bensoussan, B. E. (2015). *Business and competitive analysis* (2nd ed.). FT Press.
- IBM Security. (2025). *Cost of a data breach report 2025.*
- INFORMS. (2016). *UPS ORION — Franz Edelman Award.*
- Shuaibu, A. S., Mahmoud, A. S., & Sheltami, T. R. (2025). A review of last-mile delivery optimization. *Drones, 9*(3), 158.

A full reference list appears in `reports/05_Final_Report_Signature_Assessment.docx`.

---

## Team — Group 6

| Member | |
|--------|---|
| Sandra Amponsah | |
| Truc Linh Hoang | |
| Victoria Kpetigo | |

---

## Academic integrity & use

This repository is coursework submitted for ALY 6130 at Northeastern University. The acquisition scenario is a course case study; figures use a synthetic, benchmark-calibrated dataset and do not represent actual Amazon internal data. Please do not copy or submit this work as your own.
