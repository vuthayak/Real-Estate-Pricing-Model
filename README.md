# 🏡 Real Estate Pricing Model with Machine Learning
## Team Members:
- Vishvah Uthayakumar
- Shayaan Kazi
- Dhruv Chopra
- Anuraj Shah
- Curtis Sinopoli

## 📌 Project Overview
This project explores the use of machine learning to predict housing prices based on historical real estate data. The goal is to support homeowners, investors, and realtors in making informed decisions through accurate price estimations derived from property characteristics.

## 🎯 Objectives
1. Develop predictive models using real estate data to estimate future housing prices.

3. Compare multiple machine learning models (e.g., Linear Regression, Random Forest, SVM) and fine-tune them for improved performance.

5. Provide insights into market trends and property valuations to assist a variety of stakeholders.

## 📂 Dataset
Source: [USA Real Estate Dataset on Kaggle](https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset)

Size: 2,226,382 rows, 12 columns

Final Cleaned Size: ~1.08M rows

### Features Used:
bed — Number of bedrooms

bath — Number of bathrooms

acre_lot — Lot size (acres)

house_size — Size (sq. ft.)

city — Location (target encoded)

state — Location (one-hot encoded)

prev_sold_date — Split into year, month, day

### Target Variable:
price — Sale price of the property

## 🧠 Machine Learning Approach
### Preprocessing Steps:
Removed irrelevant features (brokered_by, status, street, zip_code)

Handled missing values and outliers

Extracted and encoded temporal and location-based features

### Models Evaluated:

| Model	| Key Strengths |	Hyperparameters |
| ------| --------------| ----------------|
| Linear Regression	| Simplicity |	Default |
|Random Forest	| Non-linearity handling	| `max_depth=10, n_estimators=200` |
|Boosted Tree Regressor |	Improved accuracy	| `max_depth=10, n_estimators=200` |
| Support Vector Machine	| High-dimensional data	| Linear kernel | 

### Validation:
10x10 Repeated K-Fold Cross-Validation

## 📊 Evaluation Metrics
R²: Goodness of fit

MAE: Mean Absolute Error

MAPE: Mean Absolute Percentage Error

RMSE: Root Mean Squared Error

## 🏆 Results
Best Model: Boosted Tree Regressor

Weakest Model: Support Vector Machine (struggled with accuracy)

Key Takeaways:
- The boosted tree regressor achieved the highest R² and lowest error rates.

- Emotion-based and highly unique property features remain a limitation of all models.

- Future trends and outlier property types may reduce generalization.

## ⚠️ Limitations & Risks
- Emotion and design factors not captured by the dataset

- Market shifts may affect model relevance

- Generalization challenges for properties unlike the training data
