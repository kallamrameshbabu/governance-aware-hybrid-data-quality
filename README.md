
# Governance-Aware Hybrid Decision Fusion for Data Quality Anomaly Detection in Cloud Lakehouses

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
![Python](https://img.shields.io/badge/Python-3.11+-blue)
![Status](https://img.shields.io/badge/Research-Reproducible-success)
![Domain](https://img.shields.io/badge/Data%20Quality-Governance-orange)

---

## Research Overview

This repository contains the complete implementation, experimental workflow, and reproducible research artifacts accompanying the manuscript:

> **Governance-Aware Hybrid Decision Fusion for Data Quality Anomaly Detection in Cloud Lakehouses: A Multi-Domain Evaluation**

The proposed framework integrates deterministic business rules, unsupervised anomaly detection, AI consensus, and uncertainty estimation into a governance-aware decision engine for enterprise data quality management.

Unlike traditional anomaly detection systems that focus solely on predictive accuracy, this work emphasizes:

- transparent evidence fusion
- deterministic decision policies
- reproducible experimentation
- operational governance
- statistical validation

The framework is evaluated using **63 controlled experiments** across **Finance**, **Healthcare**, and **Retail** datasets using nested experiment-level cross-validation and rigorous statistical inference.

## Quick Start

```bash
git clone https://github.com/kallamrameshbabu/governance-aware-hybrid-data-quality.git
cd governance-aware-hybrid-data-quality

python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

jupyter notebook

```

# Research Contributions

This research makes four primary contributions.

### 1. Governance-Aware Hybrid Decision Fusion

A deterministic policy combines heterogeneous evidence sources:

- Business-rule violations
- Isolation Forest
- Local Outlier Factor
- AI detector consensus
- Prediction uncertainty

to produce auditable operational decisions.

---

### 2. Leakage-Free Experimental Design

The evaluation employs

- experiment-level nested cross-validation
- out-of-fold prediction generation
- reproducible policy selection

preventing information leakage during model evaluation.

---

### 3. Rigorous Statistical Validation

The study evaluates performance using

- Bootstrap confidence intervals (10,000 resamples)
- Wilcoxon signed-rank tests
- Holm multiple-comparison correction
- Friedman omnibus tests

rather than relying solely on average metrics.

---

### 4. Reproducible Research Artifacts

This repository contains

- implementation notebooks
- publication-ready figures
- statistical outputs
- configuration files
- reproducibility documentation

allowing the complete experimental pipeline to be reproduced.

---

# Repository Structure

```
governance-aware-hybrid-data-quality/

├── notebooks/
├── configs/
├── docs/
├── manuscript/
├── figures/
├── results/
├── tables/
├── src/
└── tests/
```

---

# Research Workflow

```
Public Dataset

        │

        ▼

Data Quality Rules

        │

        ▼

Isolation Forest
        +
Local Outlier Factor

        │

        ▼

AI Consensus

        │

        ▼

Uncertainty Estimation

        │

        ▼

Governance-Aware Evidence Fusion

        │

        ▼

Accept
Repair
Quarantine
Escalate
```

---

# Experimental Evaluation

The framework was evaluated on three independent application domains.

| Domain | Dataset | Experiments |
|---------|----------|------------:|
| Finance | Bank Marketing | 21 |
| Healthcare | Diabetes 130-US Hospitals | 21 |
| Retail | Online Retail II | 21 |

Total:

- **63 experiments**

Nested Evaluation:

- 3 outer folds
- 3 inner folds

---

# Key Findings

The evaluation demonstrates that:

- AI consensus achieved the highest numerical macro-F1 score.
- The Hybrid V3 policy achieved statistically comparable performance while significantly reducing false positives relative to the initial hybrid policy.
- Performance varied across domains, highlighting the importance of governance-aware decision policies.
- The nested optimization consistently selected the same policy configuration (W08), demonstrating stable policy selection.

---

# Reproducibility

The repository includes:

- experiment notebooks
- hybrid policy configuration
- statistical analysis pipeline
- publication-ready figures
- manuscript artifacts

Users can reproduce the experimental workflow after downloading the source datasets and placing them in the documented local paths.

---

# Data Availability

This repository **does not redistribute** the datasets used in the experiments.

All datasets are publicly available from their original sources.

Instructions for obtaining the datasets are provided in:

```
docs/data_sources.md
```

---

# Citation

If you use this repository in academic work, please cite:

```
Ramesh Babu Kallam.

Governance-Aware Hybrid Decision Fusion for Data Quality
Anomaly Detection in Cloud Lakehouses:
A Multi-Domain Evaluation.

(Data & Knowledge Engineering, under review)
```

A `CITATION.cff` file is included to support GitHub citation features.

---

# License

Released under the Apache License 2.0.

See:

```
LICENSE
```

---

# Acknowledgements

This work was developed as part of an ongoing research program investigating governance-aware artificial intelligence for enterprise data quality management, explainable AI, adaptive decision systems, and trusted data engineering.

---

## Contact

**Ramesh Babu Kallam**

GitHub:

https://github.com/kallamrameshbabu

ORCID:

https://orcid.org/0009-0008-5220-1775

## Notebooks

1. [Baseline Prototype](notebooks/01_Baseline_Prototype.ipynb)
2. [Hybrid Decision Engine](notebooks/02_Hybrid_Decision_Engine.ipynb)

Run them in numerical order.
