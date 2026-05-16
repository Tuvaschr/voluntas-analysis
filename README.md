[README.md](https://github.com/user-attachments/files/27851320/README.md)
# Voluntas — Analyst Test Dashboard
**Author:** Schroder  
**Date:** May 2026  
**File:** `Voluntas_Dashboard_Schroder.html`

---

## Overview

This is an interactive HTML dashboard built from the Voluntas Analyst Test Dataset (n = 300). It allows you to explore, filter, and analyse survey data on healthcare access, barriers, demographics, and expenditure — all within a single self-contained file that requires no installation or internet connection to run.

---

## How to Open

1. Download `Voluntas_Dashboard_Schroder.html`
2. Double-click the file — it will open directly in your browser (Chrome, Safari, Firefox, or Edge)
3. No server, no login, no software required

---

## What the Dashboard Contains

### Global Filters
Filter all charts and tables simultaneously by:
- Gender · Age Group · Region · Healthcare Access · Education Level · Income Source

### KPI Cards
Live summary statistics that update with every filter selection:
- Total respondents · % with healthcare access · % without · Avg monthly food expenditure · Total barriers reported

### Disaggregated Analysis (Tabbed)
| Tab | Content |
|-----|---------|
| **1a** | Distribution of education level by gender — counts, percentages, "Not answered" row. Valid n = 290. |
| **1b** | Distribution of healthcare access by region — counts, percentages, Not answered column. Valid n = 281. |
| **1c** | Distribution of income source by age group — counts, percentages, grouped bar chart. n = 300. |
| **2b** | Barriers to healthcare disaggregated by gender — selection rates, gender gap column, bar chart. n = 300. |

Each table includes:
- Toggle between column %, row %, and % of valid total
- Missing data clearly noted with counts shown but excluded from % calculations
- Key observations panel

### Charts
- Healthcare Access by Region
- Top Barriers to Healthcare
- Healthcare Access by Age Group
- Income Source Distribution
- Education Level vs Healthcare Access (stacked)
- Monthly Food Expenditure Distribution

### Respondent Data Table
- Full row-level data with column dropdown filters (Gender, Age Group, Region, Healthcare Access, Education, Income Source)
- Search box for free-text filtering by any field
- Expandable / collapsible

### Standalone Files
Clickable cards linking to individual standalone tables and visualisations:
- `1a_education_by_gender.html`
- `1b_healthcare_by_region.html`
- `1c_income_by_age.html`
- `1c_income_by_age_grouped.html`
- `1c_income_by_age_viz.html`
- `2b_barriers_by_gender.html`
- `2b_barriers_by_gender_viz.html`

### Codebook
Collapsible variable reference table documenting all 13 variables — name, label, type, values, and missing data notes.

---

## Dataset

| Variable | Description | Type | Missing |
|----------|-------------|------|---------|
| `resp_id` | Respondent ID | ID | None |
| `gender` | Gender | Categorical | None |
| `age_group` | Age group | Categorical | None |
| `region` | Region | Categorical | None |
| `healthcare_access` | Has access to healthcare | Binary | ~6.3% (n=19) |
| `education_level` | Highest education completed | Ordered categorical | ~3.3% (n=10) |
| `income_source` | Primary income source | Categorical | None |
| `monthly_food_exp` | Monthly food expenditure (USD) | Continuous | ~4.7% (n=14) |
| `barrier_cost` | Barrier: Cost | Binary (multi-select) | None |
| `barrier_distance` | Barrier: Distance | Binary (multi-select) | None |
| `barrier_language` | Barrier: Language | Binary (multi-select) | None |
| `barrier_long_wait_times` | Barrier: Long wait times | Binary (multi-select) | None |
| `barrier_lack_of_awareness` | Barrier: Lack of awareness | Binary (multi-select) | None |

---

## Key Analytical Notes

- All percentages for variables with missing data are calculated on **valid responses only** — missing cases are shown as "Not answered" with counts visible but excluded from % denominators
- Barrier variables are **multi-select** — percentages reflect the share of respondents selecting each barrier and do not sum to 100%
- A calculation error was identified in the source notes for Long wait times (listed as 100.4%); the correct figure is **41.0%** (123 ÷ 300 × 100)

---

## Files in This Repository

```
Voluntas_Dashboard_Schroder.html     ← Main dashboard (open this)
Analyst_Test_Dataset.xlsx            ← Source data
README.md                            ← This file
1a_education_by_gender.html
1b_healthcare_by_region.html
1c_income_by_age.html
1c_income_by_age_grouped.html
1c_income_by_age_viz.html
2b_barriers_by_gender.html
2b_barriers_by_gender_viz.html
```
