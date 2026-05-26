# 🔍 Data-Driven Disentanglement of Confounding Factors in Sjögren's Syndrome

> Lacasta K., Gandara-Alvarez A., Rus M.J., Cantiga-Silva C., Moreira Navarrete V., Lopez-Martin C., Perez Venegas J.J., Ortega J.A., Simon-Soro A.  
> *[Computers in Biology and Medicine]*, 2025. DOI: [DOI pending]

---

## Overview

This repository contains the code and results associated with the paper. We propose a confounding-aware multi-stage computational framework to disentangle the effects of aging and polypharmacy from intrinsic disease-related signals in Sjögren's Syndrome (SS). The framework integrates PCA, Random Forest with SHAP, and multivariable regression, applied to an observational cohort of 196 women.

**Main finding:** Standard classifiers (AUC 0.92) exploited confounding comorbidities rather than disease-specific signals. After systematic deconfounding, an interpretable oral model retained substantial diagnostic performance (AUC 0.82), driven primarily by cumulative dental damage and stimulated salivary flow.

---

## Repository structure

```
sjogrens-confounding/
│
├── data/
│   ├── processed/          # Anonymized data used for analysis (see Data Availability)
│   └── README_data.md      # Variable descriptions and codebook
│
├── code/
│   ├── 01_preprocessing.py # Data loading, cleaning, feature engineering
│   └── 02_analysis.py      # PCA, Random Forest + SHAP, regression models
│
├── results/
│   ├── figures/            # All figures included in the paper
│   └── tables/             # Supplementary tables
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Requirements

Python **3.10.x** is required. All dependencies are pinned to the exact versions used in the study.

Key libraries (full list in `requirements.txt`):

| Library | Version | Purpose |
|---|---|---|
| pandas | X.X.X | Data handling |
| numpy | X.X.X | Numerical operations |
| scikit-learn | X.X.X | PCA, Random Forest, metrics |
| shap | X.X.X | SHAP explainability |
| scipy | X.X.X | Statistical tests |
| matplotlib | X.X.X | Figures |
| seaborn | X.X.X | Figures |
| statsmodels | X.X.X | Multivariable regression |


## Data availability

The clinical dataset includes records from 196 women collected at Virgen Macarena and Virgen de Valme University Hospitals (Seville, Spain). Due to strict institutional patient privacy regulations (GDPR) and ethical requirements, raw clinical data cannot be publicly shared.

For access to additional data or further information, please contact the corresponding author:  
**Aurea Simon-Soro** — [asimon@us.es] — Department of Stomatology, University of Seville / CABIMER.
HormoBiome - https://www.hormobiome.com/

---

## Citation

If you use this code or data in your work, please cite:

```bibtex
@article{lacastas2025sjogrens,
  title     = {Data-Driven Disentanglement of Confounding Factors in Sjögren's Syndrome},
  author    = {Lacastas, Kristina and Gandara-Álvarez, Ángela and Rus, Maria J. and
               Cantiga-Silva, Cristiane and Moreira Navarrete, Virginia and
               Lopez-Martin, Carmen and Perez Venegas, Jose Javier and
               Ortega, Juan Antonio and Simon-Soro, Aurea},
  journal   = {[Journal Name]},
  year      = {2026},
  doi       = {[DOI]}
}
```
