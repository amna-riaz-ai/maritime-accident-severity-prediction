# Maritime Accident Severity Prediction

**Author:** Amna Riaz | Dalian Maritime University | MSc Artificial Intelligence

## Overview
This project predicts whether a maritime accident will result in fatalities using 
real UK government accident data. When an accident is reported, authorities manually 
assess its severity — a process taking days or weeks. This model provides instant 
prediction to support faster emergency response decisions.

## Dataset
UK Marine Accident Investigation Branch (MAIB) — 1,840 real accident records from 
2010 to 2024. Source: UK Government official maritime safety database.

## Problem
Only 82 out of 1,840 accidents resulted in fatalities (4.5%) — a severe class 
imbalance problem. A naive model would predict no fatality every time and still 
achieve 95% accuracy while catching zero fatal cases.

## Solution
SMOTE oversampling to handle class imbalance, followed by training and comparing 
three models: Logistic Regression, Random Forest, and XGBoost. SHAP explainability 
was applied to make predictions interpretable for real maritime safety operators.

## Results
| Model | Accuracy | F1 Score | AUC-ROC |
|---|---|---|---|
| Logistic Regression | 75.4% | 0.754 | 0.835 |
| Random Forest | 97.7% | 0.977 | 0.994 |
| XGBoost | 97.0% | 0.970 | 0.994 |

Random Forest correctly identified 322 out of 324 fatal accidents.

## Key Finding
Injury Type is the strongest predictor of fatality, followed by vessel size 
(Length and Gross Tonnage), Damage level, and Vessel Type.

## Technologies
Python, Scikit-learn, XGBoost, SHAP, SMOTE, Pandas, Matplotlib, Seaborn

## Real World Impact
Coast Guard teams can prioritize emergency response instantly. Port authorities 
can target safety inspections on high risk vessel types. Policy makers gain 14 
years of pattern insights to shape maritime safety regulations.
