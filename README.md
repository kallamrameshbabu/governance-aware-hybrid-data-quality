# Governance-Aware Evidence Fusion for Data-Quality Decisions

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
![Python](https://img.shields.io/badge/Python-3.11+-blue)
![Status](https://img.shields.io/badge/Research-Reproducible-success)
![Domain](https://img.shields.io/badge/Data%20Quality-Governance-orange)

## Research overview

This repository contains the implementation and reproducibility materials accompanying the manuscript:

> **Governance-Aware Evidence Fusion for Data-Quality Decisions: An Implemented Multi-Domain Evaluation of Anomaly Coverage and Review-Burden Trade-offs**

The study implements one calibrated governance policy with two operating points:

- a **detection component** based on the calibrated fused risk score; and
- a **full governed router** that applies lexicographic precedence to deterministic violations, evidence conflict, and the calibrated fused score.

The policy routes records to `ACCEPT`, `REPAIR`, `QUARANTINE`, or `ESCALATE` while retaining the evidence and policy version required for audit and replay.

## Main contributions

1. **Unified governed decision policy** combining deterministic rule risk, detector consensus, detector voting, and evidence uncertainty.
2. **Multi-domain controlled evaluation** across finance, healthcare, and retail.
3. **Operational burden analysis** reporting anomaly coverage, flagged-record rate, false-positive rate, and false reviews per true positive.
4. **Nested experiment-level calibration** with out-of-fold evaluation and false-positive constraints.
5. **Executable verification** of prevalence, class balance, rule coverage, evidence joins, policy labels, and artifact freshness.

## Evaluation design

| Domain | Dataset | Experiments | Evaluations |
|---|---|---:|---:|
| Finance | Bank Marketing | 21 | 210,000 |
| Healthcare | Diabetes 130-US Hospitals | 21 | 210,000 |
| Retail | Online Retail II | 21 | 210,000 |
| **Total** | Three public corpora | **63** | **630,000** |

Seven controlled anomaly classes are evaluated at exact realized prevalence levels of 1%, 5%, and 10%.

## Key findings

- The calibrated detection component achieved higher precision and lower false-positive rate than detector consensus, while the observed macro-F1 difference was not statistically significant.
- The full governed router captured **71.3%** of injected anomalies compared with **48.5%** for detector consensus.
- The router required **3.50 false reviews per true positive**, compared with **4.29** for detector consensus.
- The marginal cost of moving from consensus to governed routing was **1.82 additional false reviews per additional anomaly recovered**.
- Macro-F1 was not significantly separated across the principal methods (`Friedman p = 0.197`); the contribution is framed in coverage and review burden rather than F1 superiority.
- Governed actions formed operationally distinct populations, with strong domain dependence in the `ESCALATE` branch.

## Repository structure

```text
governance-aware-hybrid-data-quality/
├── notebooks/
│   ├── 01_Baseline_Prototype.ipynb
│   └── 02_Hybrid_Decision_Engine.ipynb
├── configs/
├── docs/
├── figures/
├── results/
├── tables/
├── CITATION.cff
├── CHANGELOG.md
├── LICENSE
├── requirements.txt
└── VERSION
```

## Execution order

1. Download the public source datasets listed in `docs/data_sources.md`.
2. Place them in the documented `data/raw/` location.
3. Run `notebooks/01_Baseline_Prototype.ipynb`.
4. Run `notebooks/02_Hybrid_Decision_Engine.ipynb`.

Google Colab is the primary execution environment. The notebooks also support local Jupyter execution with repository-relative paths.

## Data availability

The repository does **not** redistribute the three source datasets. They are publicly available from the UCI Machine Learning Repository.

## Reproducibility notes

The notebooks generate versioned experiment registries, sampling manifests, rule evidence, detector outputs, policy decisions, statistical tests, tables, figures, audit records, and a checksummed publication manifest. Large record-level outputs are excluded from GitHub and are intended for archival deposit with a persistent identifier.

## Citation

Use the repository citation provided in [`CITATION.cff`](CITATION.cff).

## License

Released under the [Apache License 2.0](LICENSE).

## Author

Ramesh Babu Kallam  
ORCID: https://orcid.org/0009-0008-5220-1775
