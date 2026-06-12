# proj-Kagglethon-Food-Waste-Prediction# Food Waste Prediction using LightGBM

## Overview

This project was developed as part of Kagglethon 1.0 conducted by Aivis, B.N.M Institute of Technology.

The objective was to predict daily food waste in buffet-style restaurants using restaurant operational data, ingredient pricing information, holiday indicators, and event-based features.

The solution was built using Machine Learning and secured 🥇 1st Place in the competition.

---

## Problem Statement

Food waste is a major challenge in buffet restaurants due to over-preparation and fluctuating customer demand.

The goal was to predict the total daily food waste using:

- Food preparation quantities
- Food sales quantities
- Ingredient pricing trends
- Weekend and holiday information
- Sports event phases

---

## Dataset

The competition dataset consisted of:

1. Restaurant Operations Dataset
   - Daily food prepared
   - Daily food sold
   - Holiday indicators
   - Sports event information

2. Grocery Prices Dataset
   - Daily ingredient prices
   - Market trends

3. Dish-Ingredient Matrix
   - Mapping between dishes and ingredients

---

## Approach

### Baseline Estimation

A baseline waste estimate was calculated using:

Waste = Total Prepared - Total Sold

### Feature Engineering

Created additional features such as:

- Total Prepared Quantity
- Total Sold Quantity
- Imbalance Ratio
- Preparation-to-Sales Ratio
- Over-preparation Indicator
- Weekend Flag
- Religious Holiday Flag
- Sports Event Phase

### Residual Learning

Instead of directly predicting food waste, the model learned the residual error between actual waste and baseline waste estimates.

---

## Machine Learning Model

Model Used:

- LightGBM Regressor

Parameters:

- n_estimators = 900
- learning_rate = 0.03
- num_leaves = 31
- subsample = 0.8
- colsample_bytree = 0.8

---

## Evaluation Metric

Normalized Root Mean Squared Error (NRMSE)

Baseline NRMSE:
0.0468

Final NRMSE:
0.0359

---

## Technologies Used

- Python
- Pandas
- NumPy
- LightGBM
- Scikit-Learn

---

## Result

🥇 Secured 1st Place in Kagglethon 1.0

The final solution improved prediction accuracy through feature engineering and residual learning techniques.

---

## Repository Structure

├── Food_Waste_Prediction.ipynb
├── requirements.txt
├── README.md
└── certificate.jpg

---

## Future Improvements

- Time-series forecasting features
- Ensemble models
- Advanced demand prediction techniques
- Explainable AI for waste analysis
