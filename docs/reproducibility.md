# Reproducibility Guide

## Environment

Python 3.11

Dependencies are listed in:

```
requirements.txt
```

or

```
environment.yml
```

---

## Running the Experiments

Run the notebooks in order.

```
01_Baseline_Prototype.ipynb

↓

02_Hybrid_Decision_Engine.ipynb
```

The second notebook performs:

- hybrid policy optimization
- nested cross-validation
- statistical testing
- publication artifact generation

---

## Generated Outputs

The notebook automatically produces:

- publication figures
- publication tables
- JSON summaries
- audit reports

No manual post-processing is required.

---

## Random Seeds

All experiments use fixed random seeds where applicable to improve reproducibility.

---

## Reproducibility Goal

The repository is intended to reproduce every experiment reported in the accompanying manuscript.
