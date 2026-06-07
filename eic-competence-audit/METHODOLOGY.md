# Methodology

## PubMed Search Strategy

### Narrow Search
```
"machine learning"[Title/Abstract] AND "[Journal Name]"[Journal]
```
Captures papers that specifically use the term "machine learning" in title or abstract.

### Broad Search
```
("machine learning"[Title/Abstract] OR "deep learning"[Title/Abstract] OR 
 "artificial intelligence"[Title/Abstract] OR "neural network"[Title/Abstract] OR 
 "natural language processing"[Title/Abstract]) AND "[Journal Name]"[Journal]
```
Captures the full spectrum of AI/ML terminology.

### Baselines
Same search terms without the `[Journal]` restriction, yielding PubMed-wide counts.

### Critical Methodological Note
The `[Journal]` field tag restricts results to the specific journal's PubMed abbreviation. This is essential — without it, searching for `"Clin Infect Dis"` in full text would match any paper mentioning clinical infectious diseases, not papers published in CID. Initial searches without `[Journal]` tags yielded inflated counts (e.g., CID: 681 vs. corrected 7 for narrow search).

### Time Frame
- **Analysis window**: 2023–2025 (3 full years)
- **Extracted**: 2021–2026 (for trajectory analysis)
- **2026 data**: Partial year, excluded from 3-year totals
- **Search date**: February 27, 2026

## EIC Credential Assessment

### Criteria for "ML Training"
- Formal degree in CS, data science, informatics, or computational biology
- Graduate-level coursework in machine learning (as evidenced by transcript/program)
- Professional certificate in ML/AI from accredited institution

### Criteria for "ML Publications"
- First-author or corresponding-author publication applying ML methodology
- Not: co-authorship on a paper where ML was done by a collaborator
- Not: editorial or commentary about AI/ML

### Sources Consulted (per EIC)
1. Institutional faculty profile
2. Google Scholar publication list
3. PubMed author search
4. Journal editorial board page
5. LinkedIn (when available)
6. NIH Reporter (for funded ML-related grants)

### Exclusions
- **Isaac Kohane** (NEJM AI): Excluded as purpose-built outlier — appointed specifically because of ML credentials
- **Non-US journals**: Lancet family, BMJ, CMI, IJID excluded per scope
- **Professional editors**: Editors without academic appointments excluded

## Predictive Model

### Narrow Model Parameters
| Component | Weight | Rationale |
|-----------|--------|-----------|
| ML Training (0/1) | 0.50 | Core competency; without it, everything else is partial |
| ML Publications (0–1, normalized to 5) | 0.25 | Demonstrated applied ability |
| Quantitative PhD (0/1) | 0.15 | Transferable analytical skills (partial) |
| AI Engagement (0–1) | 0.10 | Awareness and policy engagement |

**Ceiling**: 0.25 without ML Training = 1. Rationale: statistical sophistication (Bayesian inference, survival analysis, causal inference) does not transfer to ML-specific concepts (gradient descent, regularization, cross-validation schemes, neural architecture design, feature engineering, hyperparameter tuning).

### Broad Model Base Rates
| Parameter | Value | Rationale |
|-----------|-------|-----------|
| Desk ML base | 0.30 | Pattern recognition catches obvious methodological nonsense |
| Desk clinical base | 0.90 | EICs are experts at clinical relevance |
| Reviewer ML base | 0.40 | Can find "someone who does AI" but not subfield match |
| Reviewer clinical base | 0.92 | Strong domain networks |
| Adjudication ML base | 0.50 | Coin flip when reviews conflict on technical points |
| Adjudication clinical base | 0.88 | Strong clinical judgment |
| Deputy boost | 0.35 | Substantial but not complete substitution |
| Board boost max | 0.15 | Journal's ML volume as proxy for board capacity |

### Paper Type Complexity Spectrum
| Type | ML Depth | Clinical Depth | Example |
|------|----------|----------------|---------|
| Editorial/commentary | 0.1 | 0.8 | JAMA editorial on AI regulation |
| Clinical ML application | 0.5 | 0.7 | Random forest for sepsis prediction |
| NLP/clinical text | 0.7 | 0.5 | LLM extraction from consult notes |
| Deep learning/imaging | 0.8 | 0.4 | CNN for chest X-ray TB detection |
| Novel ML methods | 0.9 | 0.3 | Transformer for AMR from WGS |

## Reproducibility

All raw PubMed CSV exports are included in `data/raw/`. Searches can be reproduced at [PubMed](https://pubmed.ncbi.nlm.nih.gov/) using the query strings embedded in each CSV file's first row. Note that counts may change slightly as PubMed indexes new publications.
