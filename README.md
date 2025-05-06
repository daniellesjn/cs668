# cs668

## Table of Contents
- [Abstract](#abstract)
- [Research Questions](#research-questions)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Limitations](#limitations)

# Injury Prediction in Professional Football Players

# Abstract
This project analyzes player injury data to investigate how player traits are associated with injury type and severity. It also explores the use of machine learning models to predict injury outcomes based on player characteristics.

---

## Research Questions

1. **Which player traits** (age, position, FIFA rating) are most associated with different **injury types or severities**?
2. **Can machine learning** models predict injury severity or type from basic player profile data?

---

## Dataset
📂 The dataset is available here: [player_injuries_impact.csv](./player_injuries_impact.csv)

- **Total Entries:** 656 injury records
- **Features:**  
  - Player Age  
  - Position  
  - FIFA Rating  
  - Injury Type  
  - Dates of Injury and Return
- **Target Variables:**
  - **Severity:** Low, Moderate, Severe (based on days missed)
  - **Injury Type:** e.g., Hamstring strain, ACL tear

---

## Methodology

- **Data Processing:**  
  - Cleaned and encoded variables (e.g., Label Encoding for Position and Injury Type)
  - Calculated days missed and created severity categories

- **Statistical Analysis:**  
  - ANOVA for Age and Rating vs. Injury Type/Severity  
  - Chi-square for Position vs. Injury Outcomes

- **Machine Learning Models:**
  - Random Forest  
  - Gradient Boosting  
  - Logistic Regression  
  - SVM  
  - KNN  

- **Evaluation Metrics:**
  - Accuracy  
  - F1 Score (weighted)  
  - Multi-Class ROC Curves and AUC scores

---

## Results

- **Age** was significantly associated with both injury severity and type (p < 0.05)
- **Position** was **not** significantly related to injury type
- **Best Models:**
  - Logistic Regression performed best for severity prediction
  - Gradient Boosting gave highest F1 scores for injury type
- ROC analysis showed models were most effective at predicting **low-severity injuries**

---

## Limitations

- Only includes injured players — no control group of uninjured players
- Injury type distribution is imbalanced
- Limited features — does not include training load, match intensity, or biomechanics

---