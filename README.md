# Age Prediction Modeling — NHANES

Predicting age and age group (Adult vs. Senior) from health and metabolic indicators using the NHANES 2013–2014 dataset.

**Authors:** Caly Nguyen, Dana Neuman, Ramon Gonzalez

---

## Dataset

National Center for Health Statistics. (2014). *National Health and Nutrition Examination Survey 2013–2014 (NHANES) age prediction subset* [Data set]. UC Irvine Machine Learning Repository.

[https://archive.ics.uci.edu/dataset/887/national+health+and+nutrition+health+survey+2013-2014+(nhanes)+age+prediction+subset](https://archive.ics.uci.edu/dataset/887/national+health+and+nutrition+health+survey+2013-2014+(nhanes)+age+prediction+subset)

---

## Project Overview

This project applies both regression and classification models to predict age-related outcomes from metabolic and lifestyle variables including BMI, fasting glucose, insulin levels, oral glucose tolerance, diabetes status, physical activity, and gender.

**Regression task:** Predict continuous age (`RIDAGEYR`) using Linear Regression, Elastic Net, and MARS.

**Classification task:** Predict age group (`Adult` vs `Senior`) using Logistic Regression, Decision Tree, and Random Forest — with and without class balancing via upsampling.

---


## Key Findings

- MARS outperformed Linear Regression and Elastic Net on the regression task but showed higher error at the age extremes (10–20 and 70–80), a classic tail-regression pattern
- All three classifiers performed similarly after balancing, with AUC values clustered around 0.73 — suggesting the available features have moderate but not strong discriminatory power for age group
- Oral glucose tolerance (LBXGLT) and insulin (LBXIN) were the most important predictors across all classification models
