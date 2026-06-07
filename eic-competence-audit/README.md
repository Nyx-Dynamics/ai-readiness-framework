# EIC ML Competence Audit

**Editorial Competence in Medical AI: A Cross-Sectional Credential Audit of Nine Major US Medical Journals**

*A.C. Demidont, DO, AAHIVS — Nyx Dynamics LLC*

---

## Overview

A cross-sectional audit of 9 major US medical journals finds that **0 of 14 editors-in-chief** hold formal ML/AI training, first-author ML publications, or quantitative doctoral degrees. These journals collectively publish **0.115% of global PubMed-indexed ML/AI biomedical output** (263 of 227,731 papers, 2023–2025). Predictive models estimate triage error rates of **45–78%** for quantitatively intensive manuscripts submitted to these venues.

This data directly motivates the Nemesis peer review service and provides the empirical foundation for the AI Readiness Framework's application to editorial gatekeeping.

---

## Journals Audited

| Journal | Category | Impact Factor |
|---------|----------|--------------|
| New England Journal of Medicine | General Medicine | 78.5 |
| JAMA | General Medicine | 63.1 |
| Annals of Internal Medicine | General Medicine | 16.1 |
| Circulation | General Medicine | 35.5 |
| Clinical Infectious Diseases | ID | 8.8 |
| Journal of Infectious Diseases | ID | 5.0 |
| Open Forum Infectious Diseases | ID | 3.8 |
| Clinical Microbiology Reviews | ID | 40.1 |
| Emerging Infectious Diseases | ID | 7.4 |

---

## Key Findings

- **0/14** editors-in-chief with formal ML/AI/CS graduate training
- **0/14** with first- or corresponding-author ML publications
- **0/14** with quantitative doctoral degrees
- **45–78%** estimated triage error rate for quantitatively intensive submissions
- **0.115%** of global PubMed ML/AI output published in these 9 journals combined

---

## Repository Contents

### `data/`
| File | Description |
|------|-------------|
| `eic_credentials.csv` | Core dataset — EIC credentials, competence scores, and journal metrics for all 14 editors-in-chief |
| `journal_ml_counts.csv` | PubMed-indexed ML/AI paper counts by journal and year (2023–2025) |
| `model_results.json` | Predictive model outputs — triage error rate estimates and confidence intervals |
| `consolidated_data.json` | Full merged dataset combining credentials, publication counts, and model results |
| `data_dictionary.md` | Variable definitions and data collection methodology |

### `visualizations/`
| File | Description |
|------|-------------|
| `us_eic_ml_audit.html` | Interactive map and credential dashboard |
| `ml_papers_audit.html` | ML/AI publication volume by journal |
| `ai_ml_papers_definitive.html` | Definitive ML/AI paper count analysis |
| `predictive_model_viz.html` | Triage error rate model visualization |

### `METHODOLOGY.md`
Full data collection, credential assessment, and modeling methodology.

---

## Citation

Manuscript in preparation. Data archived at Zenodo: [10.5281/zenodo.18826439](https://doi.org/10.5281/zenodo.18826439)

---

## Relevance to the AI Readiness Framework

This audit operationalizes **Question 6 (Readiness)** of the AI Readiness Framework at the level of the editorial system itself: if journals cannot evaluate computational validity, the gatekeeping function that determines what reaches clinical practitioners is compromised. Nemesis was built to supply the missing competence.
