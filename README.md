# h1n1-vaccine-prediction-Project

Author: Andrew Nyakiba

## Table of Contents

- [Overview](#overview)
- [Business and Data Understanding](#business-and-data-understanding)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Conclusion](#conclusion)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [Presentation](#presentation)
---

## Overview
This project builds a machine learning classification model to predict whether an individual received the H1N1 vaccine. The goal is to support public health organizations in understanding vaccination behavior and improving targeted interventions.

---

## Business and Data Understanding

### Business Problem
Vaccination uptake is critical for public health, yet many individuals do not get vaccinated. Public health organizations need data-driven insights to identify and target individuals who are less likely to receive vaccines.

### Stakeholder
Public health organizations and policymakers aiming to improve vaccination rates.

### Dataset
The dataset contains survey responses including:
- Demographic information (age, education, gender)
- Behavioral patterns (hygiene, social habits)
- Health conditions and access to healthcare
- Opinions and perceptions about vaccines

The target variable is binary:
- `1` → Received H1N1 vaccine  
- `0` → Did not receive H1N1 vaccine  

---

## Modeling

An iterative modeling approach was used:

1. **Baseline Model**
   - Logistic Regression
   - Provided a simple and interpretable starting point

2. **Decision Tree Model**
   - Captured non-linear relationships in the data

3. **Handling Class Imbalance**
   - Applied class weighting to improve minority class prediction
   - Balanced Logistic Regression showed the best improvement

4. **Model Comparison**
   - Logistic Regression improved recall by around ~30%
   - Decision Tree improved recall by ~22%
   - Logistic Regression achieved better overall performance (higher AUC)

---

## Evaluation

The primary evaluation metric was **recall** for the vaccinated class, as correctly identifying vaccinated individuals is critical for this problem.

### Key Results:
- Baseline model struggled with minority class prediction
- Class imbalance significantly affected performance
- Balanced Logistic Regression:
  - Improved recall for vaccinated individuals
  - Provided better generalization (higher ROC-AUC)
  - Maintained interpretability

The ROC curve further confirmed that Logistic Regression outperformed the Decision Tree in distinguishing between classes.

---

## Conclusion

The **Balanced Logistic Regression model** was selected as the final model due to its superior performance in identifying vaccinated individuals and its overall classification ability.

### Key Insights:
- Doctor recommendation is a major driver of vaccination
- Belief in vaccine effectiveness strongly influences behavior
- Behavioral and perception-based features are more predictive than demographic factors

---

## Recommendations

Based on the findings:

- Increase doctor-led vaccination campaigns
- Improve public trust in vaccine effectiveness
- Target specific groups with lower vaccination likelihood
- Use data-driven approaches for public health outreach

---


## Limitations

- Data is self-reported and may contain bias
- Some relevant variables may not be included

---
## Presentation

- [View PDF](presentation/h1n1_vaccine_presentation.pdf)
- [Download PPT](presentation/h1n1_vaccine_presentation.pptx)
