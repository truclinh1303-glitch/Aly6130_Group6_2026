Quantitative Risk Assessment Using the Indicators & Warning (I & W) Technique

Amazon’s Proposed Acquisition of an AI-Powered Last-Mile Delivery Optimization Platform

Group 6

Sandra Amponsah
Linh Hoang
Victoria Kpetigo

ALY 6130 – Risk Management

Module 4: Quantitative Risk Assessment (I & W)

Instructor: Abeba Nigussie Turi

Northeastern University

17th June 2026

Quantitative Risk Assessment Using the Indicators & Warning (I & W) Technique

Amazon’s Proposed Acquisition of an AI-Powered Last-Mile Delivery Optimization Platform

1.  Purpose and Approach

Module 3 established the qualitative prioritization of our risk register; this summary applies the quantitative layer to the three priority risks carried forward — R1 commercial market-entry, R2 cybersecurity breach, and R3 the cost-reduction opportunity (★). The Indicators & Warning (I & W) technique frames each risk as a set of observable leading indicators with calibrated warning thresholds. Each indicator is weighted by its diagnostic strength, normalized to a 0–1 warning contribution, and summed into a composite warning score. That score yields a data-derived probability of occurrence, which is paired with a three-point impact estimate to produce an Expected Monetary Value (EMV) and, through Monte Carlo simulation, a full distribution of exposure rather than a single point.

2.  Quantitative Steps Taken

Define indicators. For each risk we specified four leading indicators anchored to the existing KRIs (e.g., enterprise win-rate, critical vulnerabilities past the 15-day SLA, per-package cost reduction) and assigned diagnostic weights summing to 1.0.

Calibrate warnings. Each indicator was normalized to a 0–1 scale (inverting ‘lower-is-worse’ metrics) with green/amber/red bands; a composite ≥ 0.55 triggers the red warning state.

Derive probability. The composite warning score over a simulated 36-month integration window maps to P(event); for the positive risk R3, probability of realization equals 1 − mean warning.

Quantify impact & EMV. Three-point (optimistic / most-likely / pessimistic) dollar impacts were drawn from the register and combined via a PERT estimate; EMV = P × E[Impact].

Simulate & predict. A 50,000-trial Monte Carlo simulation propagated uncertainty in both probability (Beta) and impact (PERT); gradient-boosting and logistic models were trained on the indicator panel to test whether warning states are predictable from the indicators (early-warning detection).

3.  I & W Assessment of the Three Risks

The table below summarizes how each probability and impact figure was derived. Encouragingly, the I & W-derived probabilities reconcile closely with the qualitative register scores (R1 0.65 vs. 0.70; R2 0.47 vs. 0.50; R3 0.62 vs. 0.70), validating the earlier qualitative judgement while adding a defensible quantitative basis. The real-world parameters that anchor the model are drawn from published benchmarks: AI route-optimization at scale (UPS ORION) yields roughly US$300–400M in annual savings and 100M fewer miles driven (INFORMS, 2016); the global average cost of a data breach is US$4.44M, rising to US$10.22M in the United States (IBM, 2025); and last-mile delivery represents about 53% of total shipping cost — exceeding 50% per peer-reviewed review (Statista, 2024; Shuaibu et al., 2025).

4.  Monte Carlo and Machine-Learning Results

The Monte Carlo simulation converts each point estimate into a loss/gain distribution. R1 carries a most-likely exposure near $567M but a 95th-percentile downside of roughly $891M; R2’s breach exposure centers near $492M with a $701M tail; the R3 opportunity shows a most-likely upside of about $733M and a 95th-percentile best case near $991M. The gradient-boosting warning classifiers achieved strong discrimination (ROC-AUC 0.87 for R1, 0.89 for R2, and 1.00 for R3), and feature-importance analysis isolated the dominant early-warning signals: the sales-engineering vacancy gap for R1, anomalous geolocation-API traffic for R2, and driver adoption of AI routes for R3. These are the indicators the team should monitor most closely.

Figure 1. Monte Carlo simulation (50,000 trials) of conditional impact, with P(event) and EMV for each risk.

5.  Updated Risk Treatment & Response Plan (RT & RP)

The quantitative results feed back into the RT & RP. Treatment strategies follow the four standard responses; residual EMV reflects the modeled effect of each treatment (mitigation/transfer reduce downside exposure, while exploiting the positive risk increases expected upside).

Figure 2. Refreshed enterprise heat map on the non-linear P{1,3,5,7,9} × I{1,2,4,6,8,9} scale; bubble size ∝ Monte Carlo EMV.

6.  Conclusion

Quantitative I & W analysis confirmed the qualitative prioritization while sharpening it into actionable dollar figures and monitorable signals. R2 remains the highest-severity downside despite a moderate probability, warranting transfer of residual financial exposure through cyber insurance; R1 justifies active mitigation investment; and R3 should be deliberately exploited. The appended Jupyter notebook and indicator dataset reproduce every figure above. (Data provenance: the indicator-level panel is synthetic and illustrative, constructed solely to demonstrate the I & W methodology; the cost, probability-anchor, and competitive parameters are calibrated to the published benchmarks cited in Section 3. The R2 impact band reflects an enterprise-scale/mega-breach scenario across an entire delivery network, which is materially larger than the per-incident industry average reported by IBM, 2025.)

References

COSO. (2017). Enterprise risk management—Integrating with strategy and performance. Committee of Sponsoring Organizations of the Treadway Commission.

ISO. (2018). ISO 31000:2018 Risk management—Guidelines. International Organization for Standardization.

Project Management Institute. (2017). A guide to the project management body of knowledge (PMBOK guide) (6th ed.). PMI.

Shuaibu, A. S., Mahmoud, A. S., & Sheltami, T. R. (2025). A review of last-mile delivery optimization: Strategies, technologies, drone integration, and future trends. Drones, 9(3), 158. https://doi.org/10.3390/drones9030158

IBM. (2025). Cost of a data breach report 2025. IBM Security. https://www.ibm.com/reports/data-breach

INFORMS. (2016). UPS On-Road Integrated Optimization and Navigation (ORION) project. Institute for Operations Research and the Management Sciences. https://www.informs.org/Impact/O.R.-Analytics-Success-Stories/UPS

Statista. (2024). Last-mile delivery share of total shipping costs worldwide from 2018 to 2023. https://www.statista.com/statistics/1434298/last-mile-share-of-total-shipping-costs/

Appendix A.  Officially-Sourced Benchmark Parameters and Data Provenance

Every real-world dollar figure cited in this assessment is anchored to a citable, official source, summarized below. These benchmarks are also provided as a machine-readable file (iw_benchmark_parameters.csv) together with the reproducible Jupyter notebook (IW_Quantitative_Risk_Assessment.ipynb) and the synthetic indicator dataset (iw_indicator_dataset.csv). The indicator panel is synthetic and seeded (SEED = 42) because the target’s internal operating KPIs are not public; its magnitudes, however, are calibrated to the anchors listed here.

Note. Access labels indicate how each source can be obtained: INFORMS, MDPI (Shuaibu et al., 2025), and U.S. Census data are free to view or download; the IBM Cost of a Data Breach 2025 report is a free PDF after email registration; Statista and the ISO standard may require institutional or library access.