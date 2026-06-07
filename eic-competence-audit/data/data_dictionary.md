# Data Dictionary

## eic_credentials.csv

| Variable | Type | Description |
|----------|------|-------------|
| journal | string | Full journal name |
| journal_abbrev | string | Standard abbreviation |
| category | string | GenMed or ID |
| impact_factor | float | 2024 Journal Impact Factor |
| eic_name | string | Editor-in-chief full name |
| eic_degree | string | Degrees held |
| institution | string | Primary institutional affiliation |
| domain | string | Research domain/specialty |
| ml_training | binary | Formal ML/AI/CS graduate training (0/1) |
| ml_publications | binary | First/corresponding author ML publication (0/1) |
| quantitative_phd | binary | PhD in quantitative discipline (0/1) |
| ai_deputy | binary | Journal has AI/ML deputy editor (0/1) |
| editorial_ai_engagement | binary | Journal has formal AI review initiatives (0/1) |
| narrow_score | float | Narrow model competence score [0,1] |
| notes | string | Additional context |

### Credential Assessment Sources

Credentials assessed February 2026 via:
- Institutional faculty profiles
- Google Scholar author pages
- PubMed author searches
- Journal editorial board pages
- LinkedIn professional profiles
- NIH Reporter (grant history)

### Scoring Definitions

**ml_training:** Formal graduate-level coursework or degree in machine learning, computer science, data science, or computational methods. Biostatistics/statistics training alone does not qualify.

**ml_publications:** First or corresponding authorship on a peer-reviewed publication employing ML/AI as a primary method. Co-authorship on collaborative studies does not qualify.

**quantitative_phd:** Doctoral degree in mathematics, statistics, computer science, physics, engineering, or operations research. MD/PhD in biomedical sciences does not qualify unless the PhD is in a qualifying field.

**ai_deputy:** Deputy or associate editor with documented ML/AI expertise formally appointed to assist with triage of quantitative manuscripts.

**editorial_ai_engagement:** Dedicated journal AI/ML sections, specialized reviewer databases for computational manuscripts, or formal editorial policies for AI/ML review.

## journal_ml_counts.csv

| Variable | Type | Description |
|----------|------|-------------|
| journal | string | Full journal name |
| journal_abbrev | string | Standard abbreviation |
| category | string | GenMed or ID |
| narrow_YYYY | int | Papers matching narrow ML search in year YYYY |
| narrow_3yr | int | Sum of narrow counts 2023-2025 |
| broad_YYYY | int | Papers matching broad AI/ML search in year YYYY |
| broad_3yr | int | Sum of broad counts 2023-2025 |

### PubMed Baseline Totals (2023-2025)

| Search | Total |
|--------|-------|
| Narrow (ML only) | 139,206 |
| Broad (ML+DL+AI+NN+NLP) | 227,731 |
