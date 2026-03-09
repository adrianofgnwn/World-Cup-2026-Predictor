# What Makes a World Cup Champion?

![Python](https://img.shields.io/badge/Python-3.14-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## Overview

This project analyzes **FIFA World Cup matches from 1974–2022** to identify the statistical DNA of tournament champions. Using classification models, we examine how factors such as shot accuracy, xG performance, defensive solidity, possession, and match dominance contribute to whether a team performs like a **World Cup winner**.

> **Note:** The dataset is a curated selection of 43 notable matches across 13 World Cups, not every match played.

## Research Questions

1. *What statistical profile separates World Cup champions from every other team in the tournament?*
2. *Which match-level features are most predictive of champion performance?*

## Dataset

* **Name:** FIFA World Cup Enhanced (1974–2022)
* **Source:** [Kaggle](https://www.kaggle.com/datasets/samyakrajbayar/fifa-world-cup)
* **Size:** 43 matches, 38 features → reshaped to 86 team-match rows
* **Target Variable:** `is_champion` (1 = World Cup winner that year, 0 = other)

## Project Pipeline

1. Data Loading & Preparation
2. Feature Engineering
3. Exploratory Data Analysis (EDA)
4. Model Training & Evaluation
5. Insights & Conclusions

## Results

| Model | Accuracy | F1 Score | ROC-AUC |
| --- | --- | --- | --- |
| **Logistic Regression** | **0.779** | **0.655** | **0.847** |
| Random Forest | 0.779 | 0.596 | 0.806 |
| Gradient Boosting | 0.767 | 0.524 | 0.750 |

## Key Findings

* **Clinical finishing is the #1 trait** — Champions convert 15.1% of shots vs 9.7%
* **Defensive solidity matters** — 93.5% save rate vs 87.0%, conceding only 0.79 goals per match
* **The clutch factor is real** — Champions overperform their xG by +0.19, others underperform by -0.13
* **Champions dominate matches** — +1.5 avg goal difference, 1.75x shot dominance ratio
* **Discipline doesn't matter** — Virtually identical card averages between champions and non-champions
* Logistic Regression outperformed all other models on F1-score and ROC-AUC

## Project Structure

```
World-Cup-Champion-Analysis/
│
├── data/
│   └── fifa_world_cup_enhanced_1974_2022.csv
├── notebooks/
│   └── world_cup_champion_analysis.ipynb
├── requirements.txt
└── README.md
```

## Requirements

Install dependencies using:

```
pip install -r requirements.txt
```

## Dependencies

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

## Author

Made as a portfolio project for a BSc Computer Science degree.

## License

This project is licensed under the MIT License.