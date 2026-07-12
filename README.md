# Global Healthy Diet Cost Analysis

An exploratory data-analysis and machine-learning project investigating how
the cost of a healthy diet varies across countries, regions and time.

The analysis covers **1,379 observations**, representing **175 countries**
between **2017 and 2024**.

## Project overview

Access to an affordable healthy diet is an important indicator of global
food security and economic wellbeing.

This project explores:

- How healthy-diet costs are distributed globally
- How costs differ across geographic regions
- How prices changed between 2017 and 2024
- Which variables are associated with higher diet costs
- How effectively regression models can estimate healthy-diet cost

## Dataset

The dataset contains country-level healthy-diet cost estimates expressed in
purchasing-power-parity-adjusted US dollars.

Main variables include:

| Variable | Description |
|---|---|
| `country` | Country name |
| `region` | Geographic region |
| `year` | Observation year |
| `cost_healthy_diet_ppp_usd` | Daily cost of a healthy diet in PPP USD |
| `annual_cost_healthy_diet_usd` | Estimated annual healthy-diet cost |
| `cost_vegetables_ppp_usd` | Estimated vegetable component cost |
| `cost_fruits_ppp_usd` | Estimated fruit component cost |
| `cost_category` | Assigned cost category |

Dataset source: [Cost of Healthy Diet by Country, 2017–2024](INSERT_DATASET_URL)

## Analysis workflow

1. Data loading and quality auditing
2. Missing-value and duplicate inspection
3. Exploratory data analysis
4. Regional and temporal comparisons
5. Feature engineering
6. Regression-model training
7. Model evaluation and interpretation

## Exploratory findings

Initial analysis found:

- The mean daily cost of a healthy diet was approximately **$3.68 PPP**
- Recorded values ranged from approximately **$1.70 to $8.39**
- The dataset contains observations from Africa, Asia, Europe and the Americas
- Diet costs vary substantially across both countries and regions
- Several component-cost variables contain substantial missing data and
  therefore require careful treatment

## Machine-learning models

The following regression approaches are compared:

- Linear Regression
- Ridge Regression
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM

Models are evaluated using:

- Coefficient of determination, R²
- Root mean squared error, RMSE
- Mean absolute error, MAE
- Cross-validation performance

> Model results are interpreted cautiously because country-level and
> time-dependent data require leakage-safe validation.

## Repository structure

```text
.
├── assets/          # Figures used in this README
├── data/            # Dataset and data documentation
├── notebooks/       # Complete Jupyter analysis
├── README.md
└── requirements.txt
