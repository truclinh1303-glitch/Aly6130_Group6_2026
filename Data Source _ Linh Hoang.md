# Data Source Registry
## ALY 6130 — Quantitative Risk Analysis
### Amazon AI Last-Mile Acquisition | Group 6

---

## Master Data Sources

| # | Risk Category | Data Type | Source Name | Data Description | Key Variables for Risk Calc | Risk IDs Covered | Access | URL | Last Updated |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Financial | Structured | Amazon 10-K / Annual Report | Revenue, capex, shipping & fulfillment costs, operating margins, acquisition history | Capex baseline, cost structure, ROI assumptions | R1, R5, R6, R7, R8, R10 | Free | https://www.sec.gov/cgi-bin/browse-edgar | Annual — FY2024 |
| 2 | Financial | Structured | UPS Annual Report / 10-K | Package volume, ORION savings ($300–400M/yr), fuel reduction, route efficiency metrics | Competitor cost benchmarks, route efficiency KPIs | R21, R23, R24 | Free | https://investors.ups.com/financial-information | Annual — FY2024 |
| 3 | Financial | Structured | FedEx Annual Report / 10-K | Surround AI performance, last-mile cost structure, delivery speed benchmarks | Competitor feature baseline, delivery accuracy rates | R21, R22, R23 | Free | https://investors.fedex.com/financial-information | Annual — FY2024 |
| 4 | Financial | Structured | SEC EDGAR — Full-Text Search | 10-K, 10-Q, 8-K filings for Amazon, UPS, FedEx; earnings disclosures | Material risk disclosures, litigation costs, regulatory filings | R4, R52, R56, R60 | Free | https://efts.sec.gov/LATEST/search-index | Continuous |
| 5 | Financial | Structured | Finro AI Valuation Multiples (Q1 2026) | EV/Revenue multiples for 575 AI companies across 15 niches; M&A comps dataset | Acquisition price range, fair value benchmarks (10x–50x revenue) | R7 | Paid (report) | https://www.finrofca.com/research/ai-multiples | Q1 2026 |
| 6 | Financial | Structured | CB Insights — AI M&A Deals | AI deal count, deal values, funding round history, logistics AI startup landscape | Market entry frequency, startup valuation distribution | R7, R27 | Freemium | https://www.cbinsights.com/research/ai-ma-trends | Quarterly |
| 7 | Financial | Structured | Crunchbase — Logistics AI Startups | Funding rounds, investors, valuations, founding dates for logistics AI companies | Competitor entry history, disruption timeline inputs | R27, R7 | Freemium | https://www.crunchbase.com/search/organizations | Continuous |
| 8 | Macroeconomic | Structured | World Bank Open Data | GDP growth rates, inflation, trade metrics by country; historical time series | Macro scenario inputs for currency/budget risk simulation | R9 | Free | https://data.worldbank.org/indicator | Annual |
| 9 | Macroeconomic | Structured | World Bank LPI 2.0 (2023–2024) | Logistics Performance Index: shipment speed, reliability, customs efficiency by country | Cross-border risk baseline, supply chain performance benchmarks | R25, R59 | Free | https://lpi.worldbank.org/en/home | Biennial |
| 10 | Macroeconomic | Structured | FRED — St. Louis Federal Reserve | US CPI, Federal Funds Rate, PPI (transportation), fuel price index | Inflation inputs for cost escalation scenarios; interest rate for NPV/DCF | R9, R6 | Free | https://fred.stlouisfed.org/categories/32423 | Monthly |
| 11 | Macroeconomic | Structured | IMF World Economic Outlook Data | Multi-country GDP forecasts, exchange rate volatility, current account data | FX hedging inputs; international expansion risk scenarios | R9, R59 | Free | https://www.imf.org/en/Publications/WEO/weo-database | Biannual |
| 12 | Operational | Structured | Amazon Logistics Operations Data (10-K Notes) | Failed delivery rates, re-attempt costs, DSP network (275K+ drivers), peak volumes | Delivery failure rate baseline; re-attempt cost per unit | R15, R16, R20, R30 | Free | https://ir.aboutamazon.com/annual-reports-proxies-and-shareholder-letters | Annual |
| 13 | Operational | Structured | BLS — Occupational Employment (Transportation) | Driver wages, turnover rates, injury/fatality rates by sector | Labor cost inputs; change management resistance probability | R11, R18 | Free | https://www.bls.gov/ooh/transportation-and-material-moving | Annual |
| 14 | Operational | Structured | DOE — Alternative Fuels Data Center | EV charging station density, coverage gaps by ZIP/region, fleet electrification data | EV infrastructure readiness score; rural zone coverage gaps | R19, R29 | Free | https://afdc.energy.gov/stations#/analyze | Continuous |
| 15 | Operational | Structured | Flexport Supply Chain Index | Container shipping delays, port congestion, supplier lead time data | Third-party API reliability baseline; supply chain disruption frequency | R13, R45 | Free | https://www.flexport.com/research/ocean-timeliness | Weekly |
| 16 | Operational | Structured | Pitney Bowes Parcel Shipping Index | US/global parcel volumes by carrier, YoY growth rates, market share shifts | Market volume inputs for competitive risk scenarios | R24, R21 | Free | https://www.pitneybowes.com/us/shipping-index | Annual |
| 17 | Competitive | Structured | eMarketer — E-commerce Market Share | Amazon vs Walmart vs others: e-commerce share, Prime penetration, growth forecasts | Market share baseline; competitive displacement probability | R21, R24 | Paid | https://www.emarketer.com/topics/category/amazon | Quarterly |
| 18 | Competitive | Structured | UPS ORION Performance Benchmarks | 100M miles saved/yr, $400M cost reduction, 10–20% route efficiency gain, 25% OTD improvement | Competitor performance ceiling for accuracy benchmarks | R21, R22, R23 | Free (public disclosures) | https://investors.ups.com/financial-information | Annual |
| 19 | Competitive | Structured | Stanford AI Index 2025 | Global AI investment $252.3B (2024), private investment +44.5% YoY, M&A +12.1% | Market entry rate; AI adoption pace for competitive lag scenarios | R24, R7 | Free | https://aiindex.stanford.edu/report/ | Annual |
| 20 | Technical | Structured | NIST AI Risk Management Framework (AI RMF 1.0) | Structured framework for AI bias, drift, explainability, and security risk quantification | Bias audit criteria; model drift thresholds; explainability requirements | R38, R41, R42, R43, R44, R46 | Free | https://nvlpubs.nist.gov/nistpubs/ai/nist.ai.100-1.pdf | 2023 (v1.0) |
| 21 | Technical | Structured | MIT CSAIL / CTL Research Datasets | Academic papers on ML model drift rates, training data quality, routing algorithm benchmarks | Re-training frequency distributions; accuracy degradation curves | R41, R43, R44 | Free | https://ctl.mit.edu/research | Ongoing |
| 22 | Technical | Structured | Google Maps Platform / HERE API SLA Data | API uptime guarantees (99.9%), latency benchmarks, coverage reports by region | Third-party API reliability inputs; fallback routing probability | R13, R45 | Free (developer docs) | https://developers.google.com/maps/sla | Continuous |
| 23 | Legal/Compliance | Structured | EU AI Act — Official Text (2024) | Transparency, explainability, high-risk AI system requirements; enforcement timeline | Compliance gap probability; cost of modifications if non-compliant | R51, R53 | Free | https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689 | 2024 |
| 24 | Legal/Compliance | Structured | California AG — CCPA Enforcement Actions | CCPA enforcement cases, fines issued, sectors targeted | Fine probability distribution; breach cost baseline | R54, R33 | Free | https://oag.ca.gov/privacy/ccpa | Ongoing |
| 25 | Legal/Compliance | Structured | FTC — Amazon Antitrust Filings | FTC vs Amazon case history, scope of market definition used, settlement terms | Antitrust delay probability; deal close timeline inputs | R28, R56 | Free | https://www.ftc.gov/legal-library/browse/cases-proceedings | Ongoing |
| 26 | Legal/Compliance | Structured | California Clean Miles Standard | EV adoption requirements for TNCs/delivery fleets; compliance deadlines and penalties | Compliance cost estimates; penalty probability by year | R58, R19 | Free | https://ww2.arb.ca.gov/our-work/programs/clean-miles-standard | 2023 |
| 27 | Legal/Compliance | Structured | EEOC — Algorithmic Bias Guidance | AI hiring/routing discrimination guidelines; case precedents for algorithmic disparate impact | Bias litigation probability; settlement cost range | R34, R42, R52 | Free | https://www.eeoc.gov/laws/guidance/questions-and-answers-clarify-and-provide-common-interpretation | 2023 |
| 28 | Unstructured | Qualitative | Amazon Earnings Call Transcripts | CEO/CFO commentary on logistics AI, DSP program, delivery speed targets | Strategic intent signals; management risk appetite indicators | R5, R7, R24, R35 | Free | https://seekingalpha.com/symbol/AMZN/earnings | Quarterly |
| 29 | Unstructured | Qualitative | UPS / FedEx Earnings Transcripts | ORION/Surround competitive commentary, AI investment disclosures | Competitor investment pace; feature roadmap signals | R21, R22, R23 | Free | https://seekingalpha.com/symbol/UPS/earnings | Quarterly |
| 30 | Unstructured | Qualitative | Reuters / Bloomberg Logistics News | Amazon DSP labor disputes, AI deployment incidents, supply chain disruptions | Reputational event frequency; media sentiment baseline | R11, R30, R35, R37 | Freemium | https://www.reuters.com/business/retail-consumer | Continuous |
| 31 | Unstructured | Qualitative | TechCrunch / The Verge — AI Logistics | Logistics AI startup funding announcements, product launches, competitive moves | New entrant tracking; disruption timeline inputs | R27, R22 | Free | https://techcrunch.com/tag/logistics/ | Continuous |
| 32 | Unstructured | Qualitative | McKinsey Global Institute — AI in Logistics | Industry reports on AI route optimization ROI, adoption barriers, talent gaps | Expert probability estimates for integration failure scenarios | R12, R24, R44 | Free (registration) | https://www.mckinsey.com/industries/travel-logistics-and-infrastructure | Annual |
| 33 | Unstructured | Qualitative | Gartner Supply Chain Top 25 Report | Supply chain maturity benchmarks, technology adoption curves, vendor landscape | Vendor reliability scores; platform longevity estimates | R49, R27 | Paid | https://www.gartner.com/en/supply-chain/research | Annual |
| 34 | Unstructured | Qualitative | Wall Street Journal — Tech/Antitrust | Amazon antitrust coverage, AI regulation editorial, acquisition regulatory commentary | Regulatory sentiment indicators; deal risk narrative | R28, R56, R51 | Paid | https://www.wsj.com/tech/ai | Continuous |
| 35 | Unstructured | Qualitative | Morrison Foerster Tech M&A Survey 2025 | 57% of dealmakers expect AI M&A to increase; AI as top acquisition priority | Market timing signals; deal premium justification | R7, R24 | Free | https://www.mofo.com/resources/insights/tech-ma-survey | Annual |

---

## Risk-to-Data Source Mapping

| Risk ID | Risk Description | Category | Risk Score | Primary Data Sources | Key Metrics to Extract | Quant Method |
|---|---|---|---|---|---|---|
| **R6** | Initial capital costs — human & physical infrastructure | Financial | **81** | Amazon 10-K (capex), FRED (inflation), IMF (FX rates) | Capex history, infra cost per facility, inflation rate | Monte Carlo — PERT cost sim |
| **R43** | Limited training data for rural/underrepresented zones | Technical | **81** | DOE AFDC (coverage gaps), MIT CTL (ML papers), NIST AI RMF | Rural zone delivery density, data completeness % | Probability distribution — coverage gap |
| **R5** ★ | Cost savings via AI route efficiency (opportunity) | Financial | **72** | UPS ORION benchmarks, Amazon DeepFleet data, Flexport | Cost-per-stop reduction %, fuel savings baseline | Scenario analysis — upside range |
| **R24** | Cost of lagging in AI adoption vs competitors | Competitive | **72** | Stanford AI Index, eMarketer, UPS/FedEx 10-K | Market share shift rate, adoption timeline delta | Monte Carlo — market share loss sim |
| **R16** | System failure/downtime during peak operations | Operational | **63** | Amazon 10-K, Google Maps SLA, MIT CSAIL | Uptime benchmarks, downtime cost/hr, peak volume | Expected Value = P(failure) × Cost |
| **R7** | Acquisition overpayment at inflated AI market multiples | Financial | **56** | Finro Q1 2026, CB Insights, Morrison Foerster Survey | EV/Revenue multiples (10x–50x), comparable deal values | Sensitivity analysis — DCF scenarios |
| **R44** | AI model drift — accuracy degrades over time | Technical | **56** | NIST AI RMF, MIT CTL research, Amazon earnings transcripts | Drift rate (%/month), re-training cost, accuracy floor | Regression — drift curve modeling |
| **R4** | Legal/litigation costs from AI compliance failures | Financial | **54** | FTC filings, California AG CCPA, EU AI Act text | Historical fine amounts, enforcement frequency | Expected loss = P(violation) × Fine |
| **R34** | Ethical/bias concerns in delivery outcomes | Reputational | 45 | EEOC guidance, NIST AI RMF, academic bias audit studies | Disparate impact ratio, audit failure rate | Probability × reputational cost model |
| **R46** | Cybersecurity breach — customer & driver geolocation | Technical | 45 | NIST AI RMF, Amazon 10-K risk notes, CISA advisories | Breach probability, avg breach cost (IBM Cost of Breach) | Scenario tree — breach severity × P |
| **R8** | ROI shortfall if commercialization fails | Financial | 42 | Amazon 10-K, eMarketer, UPS ORION benchmarks | Platform adoption rate benchmarks, enterprise win-rate | Monte Carlo — revenue distribution |
| **R10** | Unplanned integration cost overruns | Financial | 42 | McKinsey M&A integration reports, Amazon 10-K | Historical IT integration overrun rates (avg 45%+) | PERT — cost range simulation |
| **R18** | Driver safety incidents from AI time pressure | Operational | 42 | BLS injury data, Amazon DSP incident reports, OSHA | Incident rate per 100 drivers, cost per incident | Expected cost = rate × unit cost |
| **R21** | Failure to win vs UPS ORION / FedEx Surround | Competitive | 42 | UPS/FedEx 10-K, Pitney Bowes Index, eMarketer | Market share delta, feature parity gap, enterprise win rate | Competitive gap scorecard |
| **R35** | Negative media — AI-driven driver labor practices | Reputational | 42 | Reuters, WSJ, BLS labor data, TechCrunch | Media sentiment index, union dispute frequency | Qualitative risk index → P×I |
| **R52** | Bias/discrimination legal costs from route disparities | Legal/Compliance | 42 | EEOC guidance, California AG, FTC enforcement | Disparate impact case settlement averages | Expected legal cost distribution |
| **R51** | Conflict with EU AI Act explainability requirements | Legal/Compliance | 36 | EU AI Act official text, McKinsey AI reports | Compliance timeline, modification cost estimates | Cost scenario — compliance vs rebuild |
| **R13** | Third-party data dependency — traffic/weather APIs | Operational | 36 | Google Maps SLA docs, Flexport, HERE API docs | API uptime SLA %, downtime frequency, fallback cost | Reliability block diagram model |
| **R25** | Global rivals setting AI logistics industry standards | Competitive | 27 | Stanford AI Index, Gartner SC Top 25, World Bank LPI | Standard-setting body participation, benchmark gaps | Qualitative index + Monte Carlo |
| **R9** | Currency & macroeconomic risk on integration budget | Financial | 12 | IMF WEO, World Bank, FRED | Exchange rate volatility (σ), inflation forecast range | VaR — currency exposure model |

---

## Coverage Summary by Risk Category

| Risk Category | # Risks in Register | # Data Sources Mapped | Top Source | Quant Methods Available | Data Completeness |
|---|---|---|---|---|---|
| Financial | 10 | 7 | Amazon 10-K + SEC EDGAR | Monte Carlo (PERT), DCF Sensitivity, Expected Value | ✅ High |
| Operational | 10 | 5 | BLS + DOE AFDC + Flexport | Expected Value (P×Cost), Reliability Block Diagram | ✅ High |
| Competitive | 9 | 5 | Stanford AI Index + eMarketer | Market Share Simulation, Competitive Gap Scorecard | 〜 Medium |
| Reputational | 8 | 4 | Reuters + EEOC Guidance | Qualitative Index → P×I, Sentiment Scoring | 〜 Medium |
| Technical | 12 | 5 | NIST AI RMF + MIT CTL | Drift Modeling, Reliability Analysis, Bias Audit Framework | ✅ High |
| Legal/Compliance | 11 | 5 | EU AI Act + FTC + California AG | Expected Loss (P×Fine), Compliance Cost Scenarios | ✅ High |
| Macroeconomic | 2 | 4 | World Bank + FRED + IMF | VaR (FX), Inflation Monte Carlo, Macro Scenario Analysis | ✅ High |
| Unstructured | — | 8 | Earnings Transcripts + McKinsey | Sentiment Analysis, Expert Elicitation, Qualitative Scoring | 〜 Medium |
| **TOTAL** | **60** | **43** | | | |

---

## Quick Reference: Sources by Access Type

### Free
- Amazon 10-K / Annual Report (SEC EDGAR)
- UPS Annual Report / 10-K
- FedEx Annual Report / 10-K
- SEC EDGAR Full-Text Search
- World Bank Open Data
- World Bank LPI 2.0
- FRED — St. Louis Federal Reserve
- IMF World Economic Outlook
- Amazon Logistics Operations Data (10-K Notes)
- BLS — Occupational Employment (Transportation)
- DOE — Alternative Fuels Data Center
- Flexport Supply Chain Index
- Pitney Bowes Parcel Shipping Index
- UPS ORION Performance Benchmarks
- Stanford AI Index 2025
- NIST AI Risk Management Framework (AI RMF 1.0)
- MIT CSAIL / CTL Research Datasets
- Google Maps Platform / HERE API SLA Data
- EU AI Act — Official Text (2024)
- California AG — CCPA Enforcement Actions
- FTC — Amazon Antitrust Filings
- California Clean Miles Standard
- EEOC — Algorithmic Bias Guidance
- Amazon Earnings Call Transcripts
- UPS / FedEx Earnings Transcripts
- TechCrunch / The Verge — AI Logistics
- Morrison Foerster Tech M&A Survey 2025

### Free (Registration Required)
- McKinsey Global Institute — AI in Logistics

### Freemium
- CB Insights — AI M&A Deals
- Crunchbase — Logistics AI Startups
- Reuters / Bloomberg Logistics News

### Paid
- Finro AI Valuation Multiples (Q1 2026)
- eMarketer — E-commerce Market Share
- Gartner Supply Chain Top 25 Report
- Wall Street Journal — Tech/Antitrust
