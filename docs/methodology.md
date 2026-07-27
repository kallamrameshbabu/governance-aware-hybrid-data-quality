# Experimental Methodology

## Evaluation Strategy

The framework was evaluated using nested experiment-level cross-validation.

The split unit is the experiment rather than individual records.

This prevents information leakage between training and testing folds.

---

## Datasets

Three domains were evaluated.

| Domain | Experiments |
|---------|------------:|
| Finance | 21 |
| Healthcare | 21 |
| Retail | 21 |

Total:

- 63 experiments

---

## Statistical Analysis

Performance was evaluated using:

- Macro Precision
- Macro Recall
- Macro F1
- False Positive Rate
- False Negative Rate
- Balanced Accuracy
- PR-AUC

Significance testing includes:

- Bootstrap confidence intervals (10,000 resamples)
- Wilcoxon signed-rank tests
- Holm correction
- Friedman omnibus tests

---

## Policy Selection

Hybrid policies were selected using constrained nested optimization.

The objective was to maximize macro-F1 while keeping the false-positive rate close to the AI-consensus baseline.

This reflects an operational governance objective rather than unconstrained predictive optimization.
