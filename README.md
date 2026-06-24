# Healthcare Operations Analysis

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/grazinga-grazille/healthcare-analytics/main?filepath=healthcare_analysis_demo.ipynb)

**Does who runs your hospital affect how well it performs?**

Launch the interactive notebook on [Binder](https://mybinder.org/v2/gh/grazinga-grazille/healthcare-analytics/main?filepath=healthcare_analysis_demo.ipynb) to explore Plotly charts in the browser (no local setup required).

An exploratory data analysis of U.S. hospital quality using CMS Care Compare data. This project investigates whether structural factors—ownership type, hospital classification, and geography—are associated with measurable differences in care quality across mortality, safety, and readmission domains.

## Dataset

| File | Description |
|------|-------------|
| `Hospital_General_Information.csv` | CMS Hospital General Information (January 2026 release) — 5,426 hospitals, 38 columns |
| `HOSPITAL_Data_Dictionary.pdf` | Official CMS field definitions and measure descriptions |

**Source:** [Centers for Medicare & Medicaid Services — Care Compare](https://data.cms.gov/provider-data/dataset/xubh-q36u)

Each hospital is rated on how many measures fall **Better**, **No Different**, or **Worse** than the national average within three clinical domains:

| Domain | What It Measures |
|--------|------------------|
| Mortality | 30-day death rates |
| Safety | Hospital-acquired infections and surgical complications |
| Readmission | Unplanned readmissions within 30 days |

## Custom KPIs

| KPI | Definition |
|-----|------------|
| **Domain Better Rate** | Proportion of measures rated Better within a domain |
| **Net Domain Score** | Better measure count − Worse measure count per domain |
| **Risk Score & Category** | Count of domains rated Worse; flagged At-Risk if ≥ 2 |
| **Composite Quality Score** | Sum of net scores across Mortality, Safety, and Readmission |

## Analysis Overview

The notebook (`healthcare_analysis_demo.ipynb`) walks through six sections:

1. **Understanding the data** — Coverage, distributions, and data quality
2. **Ownership & quality** — Comparing outcomes across hospital ownership types
3. **Readmission, mortality, and safety** — Domain-level performance patterns
4. **At-risk hospital identification** — Risk classification using the Risk Score KPI
5. **Top performers & hidden gems** — Ranking hospitals by composite quality
6. **Executive summary & recommendations** — Key findings and actionable insights