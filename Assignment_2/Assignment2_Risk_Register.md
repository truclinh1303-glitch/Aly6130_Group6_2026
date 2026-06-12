# Risk Register
## ALY 6130 – Risk Management for Analytics | Module 2
### Amazon's Proposed Acquisition of an AI-Powered Last-Mile Delivery Optimization Platform

**Group 6:** Sandra Amponsah · Linh Hoang · Victoria Kpetigo | **Date:** June 2026

---

## Risk Register

| Risk # | Date | The Risk of / That… | Caused by… | Resulting in… | Consequence / Impact | Likelihood (P) | Impact (I) | Risk Score (P×I) | Priority | Risk Owner | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **R1** | June 2026 | Amazon's acquired AI optimization platform will fail to win market share against established logistics software competitors (UPS ORION, FedEx Surround, Oracle, SAP TM) | Amazon entering a commercial logistics software market without prior sales engineering, SLA-based support infrastructure, or competitive pricing strategy against vendors with decades of enterprise software investment | Loss of expected ROI on the acquisition; inability to commercialize the platform externally; competitors accelerating feature development to neutralize Amazon's routing advantage; reputational harm in the enterprise logistics software segment | Financial: lost revenue opportunity; Competitive: market share erosion; Strategic: ROI shortfall on acquisition thesis | 7 | 6 | **42** | 🟠 HIGH | VP, Logistics Technology | Open |
| **R2** | June 2026 | A cybersecurity breach, ransomware attack, or unauthorized API access event targeting the AI optimization platform will expose customer home addresses, driver geolocation data, and delivery confirmation photographs | The acquired platform introducing a materially new attack surface — real-time geolocation feeds, customer address APIs, proof-of-delivery photographs — for which Amazon's existing cybersecurity program was not designed, prior to zero-trust controls being deployed | CCPA multi-state consumer notification obligations; regulatory enforcement penalties; disruption to last-mile delivery operations at scale; reputational damage in logistics data security | Legal/Compliance: CCPA enforcement (score 9); Reputational: data privacy breach (score 8); Operational: delivery disruption | 5 | 9 | **45** | 🔴 VERY HIGH | CISO / VP, Information Security | Open |
| **R3** ★ | June 2026 | AI-powered route optimization will deliver 15–25% per-stop delivery cost reduction and measurable carbon emission decreases, positioning Amazon ahead of California Clean Miles and EU Urban Vehicle Access regulatory mandates | Amazon's acquisition of an AI optimization platform enabling dynamic route sequencing, fuel reduction, idle time elimination, and electric vehicle deployment planning at scale across 8M+ daily packages | Hundreds of millions in annual operating savings; first-mover ESG reporting advantage with institutional investors; pre-compliance with emerging carrier emissions regulations; strengthened competitive position | Financial: cost savings (score 8); Competitive: sustainability leadership; Regulatory: pre-compliance advantage | 7 | 8 | **56** | 🟢 VERY HIGH (Upside) | VP, Last-Mile Operations | Open |

### Mitigation Strategies

**R1 — Entry into Logistics Technology Software Market**
1. Pre-launch competitive benchmarking against UPS ORION and FedEx Surround feature sets
2. Hire sales engineering and enterprise SLA support talent before commercialization
3. Monitor quarterly win-rate KRI: trigger review if win-rate < 40% for two consecutive cycles

**R2 — Cybersecurity & Data Breach Exposure**
1. Deploy zero-trust network access controls across all AI platform integrations pre-launch
2. Enforce encryption in transit and at rest; apply least-privilege RBAC
3. Implement API security gateway with anomaly detection
4. Resolve all critical vulnerabilities within 15-day SLA; any confirmed unauthorized access triggers immediate incident response

**R3 — Cost Reduction & Sustainability Leadership (Positive Risk ★)**
1. Pilot AI routing in 3–5 delivery regions and measure per-package cost vs. baseline
2. Track CO₂ per 1,000 deliveries monthly
3. Positive trigger: ≥10% cost reduction for two consecutive months → accelerate rollout investment
4. Align EV charging infrastructure planning with AI route length outputs

---

## KRI Summary — Traffic Light Threshold Reference

| Risk # | KRI Metric | 🟢 Green (Acceptable) | 🟡 Amber (Elevated — Review) | 🔴 Red (Critical — Escalate) |
|---|---|---|---|---|
| **R1** | Quarterly win-rate of acquired platform vs. UPS ORION / FedEx Surround in enterprise deals | Win-rate ≥ 50%; platform rated competitive in ≥3 feature benchmark reviews | Win-rate 40–49% for one quarter; competitor releases major feature update | Win-rate < 40% for two consecutive quarters; independent benchmark rates platform inferior |
| **R2** | High-severity vulnerabilities unresolved beyond 15-day SLA; confirmed unauthorized API access events | Zero critical vulnerabilities > 15 days; zero unauthorized access events | 1–2 critical vulnerabilities approaching 15-day SLA; anomalous API traffic detected | Any critical vulnerability > 15 days unresolved; any confirmed unauthorized access event |
| **R3** ★ | Per-package delivery cost vs. pre-integration baseline (AI-optimized routes) | Cost reduction ≥ 10% vs. baseline for two consecutive months | Cost reduction 5–9% — opportunity materializing but below target | Cost reduction < 5% or cost increase — platform not delivering expected efficiency gains |

---

## Risk Score Calculation

> **Risk Score = Probability × Impact**

| Risk # | Risk Name | Type | SWOT Source | Probability Rationale | P Score | Impact Category | Impact Rationale | I Score | Risk Score | Risk Level |
|---|---|---|---|---|---|---|---|---|---|---|
| **R1** | Entry into Logistics Technology Software Market | Competitive / Strategic | THREAT — Amazon's logistics division was designed as an internal operational capability, not a commercial software business. Rivals (UPS ORION, FedEx Surround, Oracle, SAP TM) have decades of enterprise software investment and deep carrier integration relationships | Somewhat Likely (7): acquisition will almost certainly trigger competitive responses from UPS, FedEx, and Oracle within 12 months. Amazon has zero sales-engineering or SLA-support infrastructure for the enterprise software market. Underperformance in head-to-head evaluations is a probable near-term outcome | 7 | Competitive | Somewhat High (6): Decision accuracy by rivals in US, UK, EU, and Australia is already benchmarked as competitive. Financial impact is deferred but strategic ROI impairment is material if Amazon cannot win enterprise clients. Win-rate below 40% triggers Priority classification | 6 | **42** | 🟠 HIGH |
| **R2** | Cybersecurity & Data Breach Exposure | Information Security / Legal | THREAT — The AI optimization service processes customer home addresses, real-time driver geolocation data, delivery confirmation photographs, route intelligence benchmarks, and carrier API feeds. A cybersecurity breach would expose Amazon to multi-state consumer privacy liability, CCPA enforcement actions, and reputational damage | 50-50 Possibility (5): Amazon has mature cybersecurity capabilities for e-commerce, but the acquired platform introduces entirely new data flows not covered by current architecture. Zero-trust controls, API security gateways, and incident response playbooks must be built from scratch during the 18–24 month integration window | 5 | Legal / Compliance | Extremely High (9): A confirmed breach triggers CCPA multi-state enforcement, EU AI Act high-risk system sanctions, and reputational damage in logistics data security — a domain where Amazon has no prior regulatory track record | 9 | **45** | 🔴 VERY HIGH |
| **R3** ★ | Cost Reduction & Sustainability Leadership | Financial / Strategic Opportunity | OPPORTUNITY — Dynamic AI routing can reduce miles driven 15–25% per-stop vs. static systems. Optimized routing reduces total miles and carbon emissions. Emerging regulations (California Clean Miles Standard, EU Urban Vehicle Access) create first-mover compliance advantage | Somewhat Likely (7): Amazon's SWOT Strengths confirm structural advantages — proprietary delivery data at a depth no competitor can replicate; AWS cloud integration enabling sub-second route re-optimization; 200M+ Prime subscribers providing immediate at-scale validation | 7 | Financial | High (8): At 8M daily packages and $14–$17 per-package last-mile cost, a 10% reduction generates $400M–$500M+ in annual operating savings. Sustainability pre-compliance also protects against future regulatory cost exposure from California Clean Miles and EU Urban Access mandates | 8 | **56** | 🟢 VERY HIGH (Upside) |

---

## Risk Level Legend

| Symbol | Level | Score Range | Management Action Required |
|---|---|---|---|
| 🟢 | LOW | 1–15 | Acceptable — monitor routinely via quarterly KRI dashboard review |
| 🟡 | MODERATE | 16–35 | Elevated — assign named risk owner; escalate to Director level; review monthly |
| 🟠 | HIGH | 36–54 | Significant — active treatment plan required within 30 days; VP-level oversight; monthly KRI review |
| 🔴 | VERY HIGH | 55–81 | Critical — immediate escalation to C-suite and Board Risk Committee; treatment plan within 72 hours |

---

## Scoring Scales

### Probability of Occurrence

| Level | Description | Score | Definition |
|---|---|---|---|
| 1 | Very Unlikely | 1 | Remote chance; would be a surprise if it occurred |
| 2 | Somewhat Unlikely | 3 | Could occur but is not expected under normal conditions |
| 3 | 50-50 Possibility | 5 | Equal chance of occurring or not occurring |
| 4 | Somewhat Likely | 7 | More likely than not to occur within the risk horizon |
| 5 | Very Likely | 9 | Expected to occur; high confidence based on evidence |

### Impact Scale by Category

| Score | Label | Financial | Operational | Competitive | Reputational | Technical / AI | Legal / Compliance |
|---|---|---|---|---|---|---|---|
| **1** | Very Low | Negligible: routine AI vendor maintenance fees < $1M; immaterial vs. $638B revenue | Minor: small subset of dispatchers require supplemental AI training; no impact on delivery metrics | Negligible: no competitive response from UPS, FedEx, or Oracle | None: issue contained internally; no customer awareness or media coverage | Isolated algorithm anomaly: < 0.1% of routes require manual override; resolved in next model update | Minor vendor SLA documentation gap; remediated in 30-day cycle; no regulatory exposure |
| **2** | Somewhat Low | Tech obsolescence risk: $5M–$20M incremental cost to remain competitive with UPS ORION | Limited human capital gap: 10–20 additional ML/data quality roles required; addressable in 6 months | Competitor releases minor feature update that narrows but does not eliminate Amazon's AI advantage | Isolated DSP complaints in trade forums; no mainstream media coverage | AI accuracy drops 3–5% on edge-case addresses; retraining resolves without delivery disruption | Minor AI decision log gap; low-risk finding; documentation remediated before regulatory deadline |
| **4** | Moderate | Vendor lock-in: switching to alternative AI provider costs $50M–$150M due to deep API dependencies | Third-party data dependency failure disrupts AI routing in 1–2 regions for up to 24 hours; manual dispatch activated | Acquired platform driver adoption falls below 70% in pilot regions; 30–40% of AI routes manually overridden | DSP dissatisfaction with algorithmic routing pressure reported in trade press; no direct customer-facing impact | Route processing latency exceeds 2-second threshold for 5% of dispatches under Prime Day load | AI explainability gap: route logic insufficient for EU AI Act Article 13 auditability; legal advisory issued |
| **6** | Somewhat High | Legal exposure: regulatory settlement for AI delivery discrimination claims estimated $100M–$500M | TMS integration failure delays full deployment by 12–18 months; $200M+ in unrealized efficiency savings | UPS ORION and FedEx Surround outperform Amazon in head-to-head benchmarks in US, UK, EU, Australia; win-rate < 40% for two consecutive quarters | AI routing perceived as unsafe or discriminatory; covered in national media (WSJ, Bloomberg); Congressional staffers request briefing | Training data quality issue confirmed post-deployment: 5–8% on-time delivery decline in suburban and rural markets | Bias and discrimination complaint filed; FTC opens preliminary inquiry into delivery time windows by zip code |
| **8** | High | Opportunity cost: failure to achieve AI efficiency gains foregoes $400M–$1.5B in annual savings; acquisition impairment flagged in 10-K | Data accuracy failure causes 10–15% surge in failed first-attempt deliveries across multiple markets; $100M+ in re-delivery costs | UPS and FedEx achieve AI-driven last-mile cost leadership 12–18 months ahead of Amazon; Amazon loses pricing competitiveness in same-day delivery | Data privacy breach: customer addresses and driver geolocation exposed; Prime NPS declines; Senate Commerce Committee hearing announced | Algorithmic bias confirmed by third-party audit: DOJ Civil Rights Division and FTC open formal investigations | CCPA enforcement: California AG imposes $250M+ penalty; class action filed in multiple states; EU opens concurrent GDPR investigation |
| **9** | Extremely High | Catastrophic: total acquisition cost, integration overruns, and legal settlements exceed $2B–$3B; goodwill impairment recognized; analyst downgrades trigger share price decline | System failure during Prime Day or Q4: AI routing collapses across 200+ delivery stations; 2M–5M packages undelivered; $1B+ in SLA penalties and emergency logistics costs | Competitive standard reset: UPS, FedEx, DHL, and logistics-tech startups adopt superior AI platforms; Amazon required to initiate a second acquisition cycle within 3 years at significantly higher cost | Ethical crisis: confirmed evidence of systemic surveillance, fairness violations, or unsafe driver conditions at scale; Congressional hearing; #DeleteAmazon campaign; brand damage equivalent to a major consumer safety recall | Dangerous route recommendations discovered post-deployment: AI produces routes violating school zone restrictions, bridge weight limits, or hazmat corridors; personal injury liability and criminal negligence exposure | Systemic multi-regulator failure: simultaneous CCPA enforcement, EU AI Act suspension order, and NLRB labor investigation; Amazon forced to suspend AI routing across all markets; recovery measured in years |
