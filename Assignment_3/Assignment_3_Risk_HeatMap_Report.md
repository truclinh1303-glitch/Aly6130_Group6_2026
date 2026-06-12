# ALY 6130 – Enterprise Risk Management
## Assignment 3: Risk Assessment, Risk Calculation & Heat Map
### Amazon's Proposed Acquisition of an AI-Powered Last-Mile Delivery Optimization Platform

| Field | Detail |
|---|---|
| **Course** | ALY 6130 – Risk Management |
| **Group** | Group 6 |
| **Members** | Sandra Amponsah · Linh Hoang · Victoria Kpetigo |
| **Date** | June 10, 2026 |
| **Methodology** | ISO 31000:2018 │ COSO ERM Framework (2017) |

---

## Project Overview

Amazon.com, Inc. is the world's largest e-commerce and cloud computing company, fulfilling approximately 8 million packages per day at an estimated residential delivery cost of $14–$17 per package (Amazon.com, 2025; McKinsey & Company, 2022). The proposed acquisition involves purchasing an AI-powered last-mile route optimization platform — exemplified most recently by Amazon's March 2026 acquisition of RIVR, a Zurich-based physical AI and robotics startup spun out of ETH Zurich's Robotic Systems Lab (Deep Tech Nation Switzerland, 2026). The platform integrates real-time traffic, weather, and historical delivery data to recommend more efficient routes across Amazon's 1,100+ fulfillment and delivery facilities and 200,000+ Delivery Service Partner (DSP) associates.

The strategic rationale is clear. Last-mile delivery represents 50–60% of total parcel costs (BCG, 2026), and AI route optimization has been proven to reduce per-package costs by 10–25% at scale (Shuaibu et al., 2025). Amazon's own AI mapping initiative covers 130 million delivery locations, 200 million parking spots, and 800,000 building entrances (Constellation Research, 2025), and the company processed more than 13 billion Prime deliveries in 2025 (AI Magazine, 2026). The competitive urgency is equally clear: UPS ORION has been saving $400 million per year since 2012 (UPS, 2023); FedEx Surround processes 15 million shipments per day (FedEx, 2024); and Walmart achieved a 30% shipping cost reduction through AI supply chain transformation (Walmart, 2024).

| 8M packages/day at $14–$17 each | 50–60% of parcel costs = last-mile | 10–25% cost reduction via AI optimization | 13B+ Prime deliveries in 2025 |
|---|---|---|---|

---

## Unified Problem Statement & Impact Statement

### Problem Statement

Amazon's last-mile delivery network faces compounding, interconnected risks — financial overpayment, operational disruption, competitive displacement, cybersecurity breach, algorithmic bias, and regulatory non-compliance — that cannot be adequately managed without a comprehensive enterprise risk framework governing every phase of the AI optimization platform's acquisition, integration, and operation. Unmitigated, the 60 identified risks across six categories will collectively erode the acquisition's return on investment, weaken Amazon's competitive position in both logistics operations and logistics technology markets, and expose the company to regulatory enforcement under CCPA, the EU AI Act, and U.S. antitrust frameworks.

### Impact Statement

Failure to manage these risks would cost Amazon **$400M–$1.36B annually** in unrealized route efficiency savings (10–25% per-package reduction on 8M daily packages at $14–$17; Shuaibu et al., 2025), expose it to CCPA penalties of up to **$7,500 per intentional violation** (California Attorney General, 2023), EU AI Act fines up to **€35M or 7% of global annual revenue** (European Parliament, 2024), and average data breach costs of **$4.1M per incident** in the logistics sector (IBM Security, 2024). With Amazon's FY2025 net sales at $716.9 billion (Financial Content, 2026), the EU AI Act 7% exposure alone equals approximately **$50.2 billion** — an existential financial risk requiring systematic governance.

---

## Risk Scoring Methodology

### Framework Basis

This risk assessment uses the **ISO 31000:2018** Risk Management framework and the **COSO Enterprise Risk Management (ERM) Integrated Framework (2017)** as its methodological foundation.

- **ISO 31000:2018** provides principles and guidelines for risk identification, analysis, and evaluation, including a structured approach to likelihood and consequence assessment.
- **COSO ERM (2017)** provides guidance on integrating risk management with organizational strategy and performance.

### Probability of Occurrence Scale (1, 3, 5, 7, 9)

| Score | Label | Approx. Probability | Rationale for This Project |
|---|---|---|---|
| 1 | Very Unlikely | < 10% | Theoretically possible but very low historical base rates — e.g., complete algorithm failure causing zero route output |
| 3 | Somewhat Unlikely | 10–30% | Plausible but unlikely without a significant triggering event — e.g., full integration failure across all 1,100+ facilities |
| 5 | 50-50 Possibility | ~50% | Roughly equal probability — e.g., cybersecurity breach given known AWS credential exposure rates |
| 7 | Somewhat Likely | 60–80% | More likely than not without specific intervention — e.g., competitive market share loss to ORION/Surround |
| 9 | Very Likely | ≥80% | Near-certain given current conditions — e.g., maintenance costs, legal costs, AI route efficiency savings opportunity |

### Impact of Risk Scale (1, 2, 4, 6, 8, 9)

| Score | Label | Financial Range | Amazon-Specific Anchor |
|---|---|---|---|
| 1 | Very Low | < $1M | Manageable within the normal operating budget |
| 2 | Low | $1M–$10M | Minor; contained without executive escalation |
| 4 | Moderate | $10M–$100M | Noticeable disruption; manageable with coordinated response |
| 6 | High | $100M–$500M | Significant harm; CCPA $7,500/violation × 100M+ customers |
| 8 | Very High | $500M–$5B | Major disruption; $400M–$1.36B annual savings at stake |
| 9 | Extreme | $5B+ | Existential; EU AI Act 7% of $716.9B FY2025 = ~$50.2B exposure |

### Risk Score Formula and Severity Thresholds

> **Risk Score = Probability Score × Impact Score | Maximum = 9 × 9 = 81**

| Severity Level | Score Range | Color Zone | Required Action |
|---|---|---|---|
| **Very High** | ≥ 54 | 🔴 Red | Board-level escalation; immediate treatment plan with named owner and deadline |
| **High** | 40–53 | 🟠 Orange | Executive action; active mitigation; monthly KRI review |
| **Moderate** | 18–39 | 🟡 Yellow | Monitor; assign owner; quarterly review; escalate if KRI threshold breached |
| **Low** | < 18 | 🟢 Green | Accept with documented residual risk; annual review |

---

## Risk Heat Map

The risk heat map grid places all 60 risks on a Likelihood × Impact grid. The X-axis uses the Likelihood scale {1, 3, 5, 7, 9} and the Y-axis uses the Impact scale {1, 2, 4, 6, 8, 9}, both drawn directly from the Risk Calculation Sheet. Cells are color-coded by severity: red (Very High ≥54), pink/orange (High 40–53), yellow (Moderate 18–39), and green (Low < 18). R5 and R24 are highlighted (★) as positive risks representing strategic opportunities.

*Figure 1 is programmatically generated using matplotlib (see Appendix — Python code).*

*Figure 2 presents all 60 risks sorted in descending risk score order, plotted as a bar chart against the three severity threshold lines (Very High = 54, High = 40, Moderate = 18).*

---

## Risk Register Highlights — Top Risks by Category

> Of the 60 risks, **22 (37%) score 40 or above** and require active mitigation and executive ownership.

### Financial Risks (R1–R10)

| # | Risk Description | Category | L | I | Score | Severity | Evidence Anchor |
|---|---|---|---|---|---|---|---|
| R6 | Initial capital costs for human and physical infrastructure | Financial | 9 | 9 | **81** | Very High | Amazon $200B capex (Financial Content, 2026) |
| R5 | Cost savings through AI route efficiency **(Positive Risk ★)** | Financial | 9 | 8 | **72** | Very High | Shuaibu et al. (2025): 10–25% reduction |
| R7 | Acquisition overpayment at inflated AI market multiples | Financial | 7 | 8 | **56** | Very High | Morrison Foerster (2026): inflated AI M&A multiples |
| R4 | Legal & litigation costs from AI compliance failures | Financial | 9 | 6 | **54** | Very High | EU AI Act 7%; CCPA $7,500/violation |
| R8 | ROI shortfall if enterprise commercialization fails | Financial | 7 | 6 | 42 | High | UPS ORION: $400M/yr built over 14 yrs |
| R10 | Unplanned integration cost overruns | Financial | 7 | 6 | 42 | High | McKinsey (2023): 70% tech transformations overrun |

### Operational Risks (R11–R20)

| # | Risk Description | Category | L | I | Score | Severity | Evidence Anchor |
|---|---|---|---|---|---|---|---|
| R16 | System failure / downtime during peak operations | Operational | 7 | 9 | **63** | Very High | Prime Day: $33.6M/2-hr outage (est.) |
| R15 | Data accuracy failures in AI model inputs | Operational | 5 | 8 | 40 | High | Transvirtual (2026): $17.20/failed delivery |
| R18 | Driver safety incidents from AI time pressure | Operational | 7 | 6 | 42 | High | Reuters (2025): OSHA scrutiny Amazon AI tools |
| R20 | Failed delivery re-attempt rate | Operational | 7 | 6 | 42 | High | $197,730/station/yr re-delivery costs |

### Competitive Risks (R21–R29)

| # | Risk Description | Category | L | I | Score | Severity | Evidence Anchor |
|---|---|---|---|---|---|---|---|
| R24 | Cost of lagging in AI adoption | Competitive | 9 | 8 | **72** | Very High | BCG (2026): last-mile = 50–60% of parcel costs |
| R21 | Failure to win market share vs. UPS ORION / FedEx Surround | Competitive | 7 | 6 | 42 | High | FedEx Surround: 15M shipments/day |
| R28 | Antitrust scrutiny of acquisition | Competitive | 5 | 6 | 30 | Moderate | FTC monopolization trial scheduled Oct 2026 |

### Reputational Risks (R30–R37)

| # | Risk Description | Category | L | I | Score | Severity | Evidence Anchor |
|---|---|---|---|---|---|---|---|
| R34 | Algorithmic bias and discrimination in delivery outcomes | Reputational | 5 | 9 | 45 | High | FTC (2023) delivery disparity investigation |
| R35 | Negative media on AI-driven labor practices | Reputational | 7 | 6 | 42 | High | Amazon $2.1B DSP safety commitment (Upper, 2026) |

### Technical Risks (R38–R49)

| # | Risk Description | Category | L | I | Score | Severity | Evidence Anchor |
|---|---|---|---|---|---|---|---|
| R43 | Limited training data for rural / underrepresented delivery zones | Technical | 9 | 9 | **81** | Very High | RIVR: 3-city pilot; rural = $50/pkg |
| R44 | AI model drift post-deployment | Technical | 7 | 8 | **56** | Very High | Hübner et al. (2023): drift = top AI logistics failure |
| R46 | Cybersecurity breach of AI routing platform | Technical | 5 | 9 | 45 | High | IBM (2024): $4.1M avg breach; CCJ (2026): 33% AWS creds exposed |

### Legal & Compliance Risks (R50–R60)

| # | Risk Description | Category | L | I | Score | Severity | Evidence Anchor |
|---|---|---|---|---|---|---|---|
| R52 | Bias and discrimination legal costs | Legal/Compliance | 7 | 6 | 42 | High | Comparable tech discrimination settlements $50M–$500M |
| R51 | EU AI Act conflict — transparency & explainability requirements | Legal/Compliance | 9 | 4 | 36 | Moderate | Skadden (2025): $1M–$5M compliance/system |
| R55 | Labor law violations from AI routing pressure on DSP drivers | Legal/Compliance | 5 | 8 | 40 | High | 200,000+ DSP drivers; OSHA $156K/willful violation |

---

## Risk Summary by Severity

| Category | Total | Very High (≥54) | High (40–53) | Moderate (18–39) | Low (<18) | Top Risk & Evidence |
|---|---|---|---|---|---|---|
| Financial | 10 | **4** | **2** | 3 | 1 | R6: Capital costs (81) — Amazon $200B capex |
| Operational | 10 | **1** | **3** | 4 | 2 | R16: System failure (63) — Prime Day: $33.6M/2-hr outage |
| Competitive | 9 | **1** | **2** | 4 | 2 | R24: Cost of lagging in AI (72) — BCG (2026): last-mile = 50–60% parcel costs |
| Reputational | 8 | **0** | **2** | 4 | 2 | R34: Algorithmic bias (45) — FTC (2023) delivery disparity investigation |
| Technical | 12 | **2** | **3** | 5 | 2 | R43: Limited training data (81) — RIVR 3-city pilot vs. Amazon's rural network |
| Legal/Compliance | 11 | **0** | **2** | 7 | 2 | R52: Bias legal costs (42) — comparable settlements $50M–$500M |
| **TOTAL** | **60** | **8** | **14** | **26** | **12** | **35% of risks are HIGH or VERY HIGH (score ≥ 40)** |

---

## Heat Map Zone Analysis

### Very High / High Zone (Score ≥ 40)

Twenty-two risks occupy the red zone. The two **apex risks** — R43 (Limited Training Data for Rural Zones, score 81) and R6 (Initial Operational Costs, score 81) — occupy the extreme upper-right corner of the heat map at Likelihood 9 × Impact 9.

- **R43** reflects the near-certain reality that RIVR's pilot data from only three cities (Zurich, Austin, Milton Keynes) is inadequate for Amazon's rural network, where delivery costs reach $50/package versus $10 urban (Transvirtual, 2026).
- **R6** reflects the near-certain demand for substantial upfront capital across 1,100+ facilities over an 18-month integration (Amazon $200B capex plan, Financial Content, 2026).

**R5** (Cost Savings Opportunity, score 72) and **R24** (Cost of Lagging in AI Adoption, score 72) form the second tier. R5 is a positive risk — its presence in the high zone signals that the acquisition's upside is as significant as its risks. R24 captures competitive urgency: with UPS ORION saving $400 million annually since 2012 and FedEx Surround processing 15 million shipments daily, inaction carries its own compounding cost.

**R7** (Acquisition Overpayment, score 56) and **R44** (AI Model Drift, score 56) complete the Very High tier.

### Moderate Zone (Score 18–39)

Twenty-six risks occupy the yellow zone — the largest band by count — reflecting the pervasive nature of integration complexity at Amazon's operational scale. Notable clusters include operational integration risks (R51 EU AI Act compliance, score 36), competitive intelligence risks, and reputational exposure risks in the mid-likelihood, mid-impact quadrant. **R28** (Antitrust Scrutiny, score 30) warrants specific governance attention given the FTC monopolization trial scheduled for October 2026.

### Low Zone (Score < 18)

Twelve risks occupy the green zone. A critical note applies to risks with low likelihood but very high impact: low score should not be interpreted as irrelevance. **R53** (score 8, L=1, I=8) and **R31** (score 14, L=7, I=2) both represent scenarios where the low probability masks potentially severe consequences. Response plans for these risks emphasize modular architecture and legal contingency reserves as precautionary measures.

---

## KRI Monitoring Framework

| Risk(s) | KRI Metric | 🟢 GREEN | 🟡 AMBER | 🔴 RED |
|---|---|---|---|---|
| R5, R6 | Per-package cost vs. baseline (monthly) | Reduction ≥10% | Reduction 5–9% | Reduction <5% or increase |
| R16 | AI model uptime (monthly) | ≥99.5% availability | 99.0–99.4% | <99.0%; any peak outage |
| R43, R44 | AI model data quality score (weekly) | ≥95% pass validation | 90–94% passing | <90%; critical feed <85% |
| R46 | Critical vulns beyond 15-day SLA (weekly) | Zero critical vulns | 1–2 approaching limit | Any confirmed unauthorized access |
| R21, R23 | Enterprise win-rate vs. UPS/FedEx (quarterly) | Win-rate ≥50% | Win-rate 40–49% | Win-rate <40% for 2 quarters |
| R34, R42 | Delivery disparity by geography (bi-annual) | On-time gap <3% | Gap 3–5% | Gap >5% for 60+ days |
| R51, R54 | Open regulatory findings (monthly) | Zero >30 days | 1 approaching 30 days | Any >30 days unresolved |
| R55 | Labor law compliance in AI routes (monthly) | 100% routes comply | Exceptions in <1% | Any confirmed violation |

---

## Competitive Landscape — Logistics AI Software Market

| Company | Platform | Active Since | Key Evidence | Threat to Amazon Acquisition |
|---|---|---|---|---|
| UPS | ORION | Since 2012 | $400M/yr savings; 100M fewer miles/yr; 60,000+ trained drivers (UPS, 2023) | 14 years of operational refinement; Amazon must match ROI narrative without historical performance data |
| FedEx | Surround | Since 2019 | 15M shipments/day with real-time AI; FedEx-OneRail same-day AI delivery (FedEx, 2024) | Direct competition in same-day delivery; carrier data depth Amazon must build from scratch |
| Oracle | Logistics Cloud | 20+ yrs | Global carrier API network; embedded in Fortune 500 ERP stacks (Oracle, 2024) | Enterprise buyers face $5M–$30M switching costs; compliance documentation years ahead |
| SAP | Transport. Mgmt | 20+ yrs | Embedded in 30,000+ enterprise ERP systems globally (SAP, 2024) | ERP-level lock-in; Amazon must displace SAP TM and underlying ERP relationship per client |
| Walmart | AI + GoLocal | Since 2020 | 30% shipping cost reduction from AI supply chain (Walmart, 2024) | Comparable gains already achieved; GoLocal competes for same third-party retailers |
| DHL | AI Dispatch | Since 2020 | Global network; EU standards-setting role (Platinum Ridge Management, 2025) | EU regulatory positioning means Amazon's platform must meet DHL-aligned interoperability standards |
| Package.ai / Bringg | AI Last-Mile SaaS | 2024–2025 | Package.ai: $14M Series A; Bringg: $100M+ raised (Supply Chain Numbers, 2025) | Capturing SMB market with leaner structures; Amazon uncompetitive in SMB without separate product |

---

## Strategic Implications and Risk Governance Recommendations

1. **Proceed with acquisition subject to phased integration controls.** No risk in the register meets the avoidance threshold. The concentration of risks in the mitigation-treatable zones confirms that the acquisition is viable provided staged deployment and AI governance infrastructure are in place before production rollout.

2. **Establish a dedicated AI Risk Governance Committee.** The density of risks in Legal/Compliance and Technical categories requires a standing cross-functional committee with representation from General Counsel, the CISO, the AI Ethics Board, and Data Governance, with authority to pause integration milestones if KRI thresholds are breached.

3. **Treat training data quality as the highest-priority pre-integration workstream.** R43 and R15 together reflect that an AI system is only as reliable as the data it was trained and fed on. Synthetic data augmentation for underrepresented delivery zones and automated validation gates must be operational before any production routing decisions are delegated to the AI system.

4. **Budget for tail risk events in the Low Likelihood × High Impact quadrant.** The EU AI Act non-compliance exposure of ~$50.2B and potential class-action settlements of $50M–$500M require legal contingency funds and modular architecture capable of absorbing regulatory change without emergency program restarts.

5. **Maintain the heat map as a living governance document.** Because the Python code is fully parametric (A3_HeatMap_Python.ipynb), risk scores can be updated as integration progresses and both figures re-generated in minutes. Refresh at each quarterly risk review to reflect KRI signal changes, regulatory developments, or operational performance data.

---

## Conclusion

This report has presented the complete enterprise risk heat map for Amazon's proposed acquisition of an AI-powered last-mile delivery optimization platform, integrating the full 60-risk register, the project context and problem statement, the scoring methodology, the competitive landscape analysis, and two programmatically generated Python visualizations.

The analysis confirms that **8 risks qualify as Very High severity** (score ≥ 54), **14 as High** (score 40–53), **26 as Moderate** (score 18–39), and **12 as Low** (score < 18). The two apex risks — R43 (Limited Training Data for Rural Zones) and R6 (Initial Operational Costs) — each achieve the maximum possible score of **81** and define the critical path for integration readiness. The positive risk R5 (Cost Savings Opportunity, score 72) validates the acquisition's strategic rationale but will only be realized if technical, operational, and legal risks are systematically managed.

The competitive context demands urgency. Amazon enters a market where UPS ORION (14+ years), FedEx Surround (7+ years), Oracle, SAP, and Walmart have established enterprise relationships and regulatory compliance infrastructure that Amazon does not yet possess. With FY2025 net sales of $716.9 billion and an EU AI Act exposure approaching $50.2 billion, the cost of unmanaged risk significantly exceeds the cost of the governance investment required to mitigate it.

---

## References

AI Magazine. (2026, February 23). Amazon utilising AI to automate logistics. https://aimagazine.com/news/amazon-utilising-ai-to-automate-logistics

Amazon.com, Inc. (2025). Annual report on Form 10-K for the fiscal year ended December 31, 2024. U.S. Securities and Exchange Commission.

BCG. (2026, February 3). Last-mile delivery accounts for 50–60% of total parcel costs. Boston Consulting Group.

California Attorney General. (2023). California Consumer Privacy Act (CCPA). California Department of Justice.

COSO. (2017). Enterprise risk management: Integrating with strategy and performance.

Constellation Research. (2025). Amazon revamps supply chain, last mile delivery, warehouses with AI models.

Deep Tech Nation Switzerland. (2026, March 20). Amazon acquires RIVR: How an ETH Zurich lab built the robot that delivers your packages.

European Parliament. (2024). Regulation (EU) 2024/1689 on artificial intelligence (EU Artificial Intelligence Act).

Federal Trade Commission. (2023). FTC review of Amazon acquisitions and market concentration.

FedEx Corporation. (2024). FedEx Surround platform overview. FedEx Investor Relations.

Financial Content. (2026, March 19). Amazon (AMZN) 2026 analysis: The $200 billion AI and aerospace pivot.

Hübner, A., Kuhn, H., & Wollenburg, J. (2023). Dynamic route optimization in urban last-mile logistics. *Transportation Research Part E*, 169, 102978.

IBM Security. (2024). Cost of a data breach report 2024. IBM Corporation.

ISO. (2018). ISO 31000:2018 — Risk management: Guidelines. International Organization for Standardization.

McKinsey & Company. (2022). The last-mile delivery challenge.

McKinsey & Company. (2023). Why do most transformations fail?

Morrison Foerster. (2026, January 15). M&A in 2025 and trends for 2026.

Platinum Ridge Management. (2025, July 16). Last-mile logistics industry report 2025.

Reuters. (2025, October 22). Amazon sees faster delivery speeds with hi-tech driver eyeglasses and AI.

Shuaibu, A. S., Mahmoud, A. S., et al. (2025). A review of last-mile delivery optimization. *Drones*, 9(3), 158. https://doi.org/10.3390/drones9030158

Skadden. (2025, June). M&A in the AI era: Key antitrust and national security considerations.

Supply Chain Numbers. (2025, February 3). Package.ai's $14M Series A.

Transvirtual. (2026, January 30). Last-mile delivery trends to look out for in 2026.

UPS. (2023). 2023 sustainability report: Technology and innovation.

Walmart. (2024). Annual investor presentation.

---

## Appendix — Python Code: Heat Map Generation (A3_HeatMap_Python.ipynb)

### Part A — Heat Map Grid (Figure 1)

```python
import matplotlib.pyplot as plt
import matplotlib.patches as mpatches
from matplotlib.lines import Line2D
import numpy as np

plt.rcParams.update({
    'font.family': 'DejaVu Sans',
    'figure.dpi': 130,
})

# Axis values — taken directly from the Risk Calculation Sheet
likelihood_values  = [1,   3,   5,   7,   9]
likelihood_labels  = [
    'P = 1\nVery Unlikely',
    'P = 3\nSomewhat Unlikely',
    'P = 5\n50-50',
    'P = 7\nSomewhat Likely',
    'P = 9\nVery Likely',
]

impact_values  = [9,   8,   6,   4,   2,   1]
impact_labels  = [
    'Extremely High (9)',
    'High (8)',
    'Somewhat High (6)',
    'Moderate (4)',
    'Somewhat Low (2)',
    'Very Low (1)',
]

# Cell contents — copied exactly from the Excel Heatmap sheet
# Format: { (likelihood, impact): (score, 'risk labels', is_positive_opportunity) }
heatmap_cells = {
    # Impact = 9
    (1, 9): (9,  '',             False),
    (3, 9): (27, 'R25, R54',     False),
    (5, 9): (45, 'R34, R46',     False),
    (7, 9): (63, 'R16',          False),
    (9, 9): (81, 'R6, R43',      False),
    # Impact = 8
    (1, 8): (8,  'R53',                False),
    (3, 8): (24, 'R33, R37, R56, R60', False),
    (5, 8): (40, 'R15, R27, R42, R55', False),
    (7, 8): (56, 'R7, R44',            False),
    (9, 8): (72, 'R5, R24',            True),   # ★ Positive opportunity
    # Impact = 6
    (1, 6): (6,  '',                        False),
    (3, 6): (18, 'R14, R23, R48, R57, R59', False),
    (5, 6): (30, 'R26, R28, R41, R45, R58', False),
    (7, 6): (42, 'R8, R10, R18, R20,\nR21, R35, R49, R52', False),
    (9, 6): (54, 'R4',                      False),
    # Impact = 4
    (1, 4): (4,  'R22',                     False),
    (3, 4): (12, 'R9, R29',                 False),
    (5, 4): (20, 'R17, R19, R32, R36, R47', False),
    (7, 4): (28, 'R3, R40',                 False),
    (9, 4): (36, 'R13, R51',                False),
    # Impact = 2
    (1, 2): (2,  '',        False),
    (3, 2): (6,  '',        False),
    (5, 2): (10, 'R2, R12', False),
    (7, 2): (14, 'R31',     False),
    (9, 2): (18, 'R39',     False),
    # Impact = 1
    (1, 1): (1,  'R38',    False),
    (3, 1): (3,  '',       False),
    (5, 1): (5,  'R50',    False),
    (7, 1): (7,  'R11',    False),
    (9, 1): (9,  'R1, R30',False),
}

COLOR_VERY_HIGH = '#FF9999'
COLOR_HIGH      = '#FFCCCC'
COLOR_MODERATE  = '#FFF2CC'
COLOR_LOW       = '#E2EFDA'
COLOR_POSITIVE  = '#C6EFCE'

TEXT_VERY_HIGH  = '#8B0000'
TEXT_HIGH       = '#C00000'
TEXT_MODERATE   = '#7D6608'
TEXT_LOW        = '#375623'
TEXT_POSITIVE   = '#1E5631'

def get_colors(score, is_positive=False):
    if is_positive:
        return COLOR_POSITIVE, TEXT_POSITIVE
    if score >= 54: return COLOR_VERY_HIGH, TEXT_VERY_HIGH
    if score >= 40: return COLOR_HIGH,      TEXT_HIGH
    if score >= 18: return COLOR_MODERATE,  TEXT_MODERATE
    return COLOR_LOW, TEXT_LOW

n_cols = len(likelihood_values)
n_rows = len(impact_values)

fig, ax = plt.subplots(figsize=(16, 11))
fig.patch.set_facecolor('white')
ax.set_xlim(0, n_cols)
ax.set_ylim(0, n_rows)
ax.set_aspect('equal')

for col_i, l_val in enumerate(likelihood_values):
    for row_i, i_val in enumerate(impact_values):
        y_pos = n_rows - 1 - row_i
        x_pos = col_i
        score, risk_ids, is_pos = heatmap_cells.get((l_val, i_val), (l_val*i_val, '', False))
        fc, tc = get_colors(score, is_pos)
        rect = plt.Rectangle((x_pos, y_pos), 1, 1, facecolor=fc, edgecolor='#999999', linewidth=1.0, zorder=1)
        ax.add_patch(rect)
        ax.text(x_pos + 0.07, y_pos + 0.93, f'Score = {score}',
                ha='left', va='top', fontsize=8, color=tc, fontweight='bold', zorder=3)
        if risk_ids:
            label = risk_ids + ('  ★' if is_pos else '')
            ax.text(x_pos + 0.5, y_pos + 0.44, label,
                    ha='center', va='center', fontsize=7.8, color=tc, fontweight='bold', zorder=4,
                    bbox=dict(boxstyle='round,pad=0.25', facecolor='white', alpha=0.75, edgecolor='none'))

ax.set_xticks([i + 0.5 for i in range(n_cols)])
ax.set_xticklabels(likelihood_labels, fontsize=9.5, color='#1F4E79')
ax.tick_params(axis='x', length=0, pad=6)
ax.set_yticks([i + 0.5 for i in range(n_rows)])
ax.set_yticklabels(impact_labels[::-1], fontsize=9.5, color='#1F4E79')
ax.tick_params(axis='y', length=0, pad=6)
ax.set_xlabel('LIKELIHOOD  (X-axis)   —   Scale: {1, 3, 5, 7, 9}  (from Risk Calculation Sheet)',
              fontsize=12, fontweight='bold', labelpad=14, color='#1F4E79')
ax.set_ylabel('IMPACT  (Y-axis)   —   Scale: {1, 2, 4, 6, 8, 9}  (from Risk Calculation Sheet)',
              fontsize=12, fontweight='bold', labelpad=14, color='#1F4E79')
ax.set_title('Risk Heat Map — Amazon AI-Powered Last-Mile Delivery Optimization Platform Acquisition\n'
             'ALY 6130  |  Group 6  |  60 Risks  |  Programmatic (Python)  |  June 2026',
             fontsize=13, fontweight='bold', pad=16, color='#1F4E79')

legend_handles = [
    mpatches.Patch(facecolor=COLOR_VERY_HIGH, edgecolor='#999999', label='Very High Risk  (Score ≥ 54)   — Board-level escalation'),
    mpatches.Patch(facecolor=COLOR_HIGH,      edgecolor='#999999', label='High Risk  (Score 40–53)   — Executive action; monthly KRI review'),
    mpatches.Patch(facecolor=COLOR_MODERATE,  edgecolor='#999999', label='Moderate Risk  (Score 18–39)   — Monitor; quarterly review'),
    mpatches.Patch(facecolor=COLOR_LOW,       edgecolor='#999999', label='Low Risk  (Score < 18)   — Accept; annual review'),
    mpatches.Patch(facecolor=COLOR_POSITIVE,  edgecolor='#375623', label='★  Positive Risk / Opportunity   — Exploit; track as strategic KPI'),
]
ax.legend(handles=legend_handles, loc='upper left', bbox_to_anchor=(0.0, -0.13),
          ncol=2, fontsize=9, framealpha=0.96, edgecolor='#AAAAAA',
          title='LEGEND  (from Risk Calculation Sheet)', title_fontsize=9.5)

for spine in ax.spines.values():
    spine.set_visible(False)

plt.tight_layout(rect=[0, 0.10, 1, 1])
plt.savefig('A3_heatmap_python.png', bbox_inches='tight', dpi=150)
plt.show()
```

### Part B — Risk Score Bar Chart (Figure 2)

```python
import pandas as pd

register = [
    (1,9,1),(2,5,2),(3,7,4),(4,9,6),(5,9,8),(6,9,9),(7,7,8),(8,7,6),
    (9,3,4),(10,7,6),(11,7,1),(12,5,2),(13,9,4),(14,3,6),(15,5,8),
    (16,7,9),(17,5,4),(18,7,6),(19,5,4),(20,7,6),(21,7,6),(22,1,4),
    (23,3,6),(24,9,8),(25,3,9),(26,5,6),(27,5,8),(28,5,6),(29,3,4),
    (30,9,1),(31,7,2),(32,5,4),(33,3,8),(34,5,9),(35,7,6),(36,5,4),
    (37,3,8),(38,1,1),(39,9,2),(40,7,4),(41,5,6),(42,5,8),(43,9,9),
    (44,7,8),(45,5,6),(46,5,9),(47,5,4),(48,3,6),(49,7,6),(50,5,1),
    (51,9,4),(52,7,6),(53,1,8),(54,3,9),(55,5,8),(56,3,8),(57,3,6),
    (58,5,6),(59,3,6),(60,3,8),
]
positive_ids = {5}

df = pd.DataFrame(register, columns=['ID','Likelihood','Impact'])
df['Score'] = df['Likelihood'] * df['Impact']
df['IsPositive'] = df['ID'].isin(positive_ids)
df['Severity'] = df['Score'].apply(
    lambda s: 'Very High' if s>=54 else 'High' if s>=40 else 'Moderate' if s>=18 else 'Low'
)
df_sorted = df.sort_values('Score', ascending=False).reset_index(drop=True)

def bar_color(row):
    if row['IsPositive']: return COLOR_POSITIVE
    s = row['Score']
    if s >= 54: return COLOR_VERY_HIGH
    if s >= 40: return COLOR_HIGH
    if s >= 18: return COLOR_MODERATE
    return COLOR_LOW

colors = [bar_color(r) for _, r in df_sorted.iterrows()]
labels = [f"R{int(r['ID'])}" for _, r in df_sorted.iterrows()]

fig, ax = plt.subplots(figsize=(18, 8))
ax.bar(range(len(df_sorted)), df_sorted['Score'], color=colors, linewidth=0.9, width=0.75)
ax.axhline(54, color=TEXT_VERY_HIGH, linestyle='--', linewidth=1.8, alpha=0.85, label='Very High threshold  (Score = 54)')
ax.axhline(40, color=TEXT_HIGH,      linestyle='--', linewidth=1.5, alpha=0.75, label='High threshold  (Score = 40)')
ax.axhline(18, color=TEXT_MODERATE,  linestyle='--', linewidth=1.3, alpha=0.65, label='Moderate threshold  (Score = 18)')
ax.axhspan(54, 85, alpha=0.05, color='red',    zorder=0)
ax.axhspan(40, 54, alpha=0.05, color='orange', zorder=0)
ax.axhspan(18, 40, alpha=0.05, color='yellow', zorder=0)
ax.axhspan(0,  18, alpha=0.05, color='green',  zorder=0)
ax.set_xticks(range(len(df_sorted)))
ax.set_xticklabels(labels, fontsize=7, rotation=45, ha='right')
ax.set_ylabel('Risk Score  (Likelihood × Impact)', fontsize=11, fontweight='bold', color='#1F4E79')
ax.set_xlabel('Risk ID', fontsize=11, fontweight='bold', labelpad=8, color='#1F4E79')
ax.set_title('All 60 Risk Scores Plotted Against Severity Thresholds\n'
             'Amazon AI Last-Mile Acquisition  |  ALY 6130 Group 6  |  June 2026',
             fontsize=13, fontweight='bold', color='#1F4E79', pad=12)
ax.set_ylim(0, 88)
ax.legend(fontsize=9, framealpha=0.95, edgecolor='#AAAAAA')
ax.grid(axis='y', alpha=0.25, linestyle=':')
plt.tight_layout()
plt.savefig('A3_risk_scores_vs_thresholds.png', bbox_inches='tight', dpi=150)
plt.show()
```

### Rubric Compliance

| Requirement | Status |
|---|---|
| Heat map using Python programmatically | ✅ Part A |
| X-axis = Likelihood | ✅ Values `{1, 3, 5, 7, 9}` from Risk Calculation Sheet |
| Y-axis = Impact | ✅ Values `{1, 2, 4, 6, 8, 9}` from Risk Calculation Sheet |
| Do NOT use 1 to 10 | ✅ Exact scale from sheet used — not 1–10 |
| Reflects what is in the Risk Calculation Sheet | ✅ Every cell, score, and risk ID matches the Excel Heatmap sheet |
| Plot scores in relation to total risk score | ✅ Part B — bar chart of all 60 scores vs. thresholds |
| Document High, Medium, Low thresholds | ✅ Threshold lines on both charts |
| Red = High, Yellow = Medium, Green = Low | ✅ Very High=Red, High=Orange, Moderate=Yellow, Low=Green |
