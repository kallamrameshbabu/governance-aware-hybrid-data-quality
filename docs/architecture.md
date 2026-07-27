# Governance-Aware Hybrid Decision Architecture

## Overview

The proposed framework integrates deterministic business rules, unsupervised anomaly detection, AI consensus, and uncertainty estimation into a governance-aware decision engine for enterprise data quality management.

Unlike conventional anomaly detection systems that rely on a single predictive model, the framework combines multiple complementary evidence sources to produce transparent and auditable operational decisions.

---

## Architecture

```
Public Dataset
        │
        ▼
Data Preparation
        │
        ▼
Business Rule Engine
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
Governance-Aware Hybrid Policy
        │
        ▼
Accept
Repair
Quarantine
Escalate
```

---

## Hybrid Policy

The final policy selected during nested experiment-level cross-validation uses:

| Component | Weight |
|-----------|-------:|
| Rule Risk | 0.20 |
| AI Consensus | 0.55 |
| AI Prediction Vote | 0.20 |
| Uncertainty | 0.05 |

Decision threshold:

```
0.45
```

This configuration (W08) was independently selected in every outer cross-validation fold, indicating stable policy selection.

---

## Design Principles

The framework emphasizes:

- deterministic decision policies
- auditability
- reproducibility
- governance
- operational transparency

rather than maximizing predictive accuracy alone.
