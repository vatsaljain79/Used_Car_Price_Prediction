# Used Car Price Prediction

This project aims to predict the price of used cars in the automotive market using machine learning techniques. The pipeline was developed to handle data preprocessing, feature engineering, model training, and evaluation to provide accurate price predictions.

---

## Table of Contents

- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Proposed Solution](#proposed-solution)
- [Dataset Description](#dataset-description)
- [Preprocessing and Feature Engineering](#preprocessing-and-feature-engineering)
- [Models and Training](#models-and-training)
- [Results and Performance](#results-and-performance)
- [Key Findings](#key-findings)
- [References](#references)

---

## Introduction

Predicting the price of used cars is essential for both buyers and sellers to assess fair market value. This project explores data-driven approaches to address this challenge.

---

## Problem Statement

The used car market's dynamic nature creates difficulty in determining fair prices due to factors such as:
- Mileage
- Fuel type
- Accident history
- Year of manufacture

This project builds a predictive model using these attributes to enhance decision-making.

---

## Proposed Solution

The solution includes:
1. **Dataset Preparation**: Handling missing values, encoding categorical variables, and scaling features.
2. **Feature Engineering**: Transforming attributes like mileage and engine specifications for better model interpretability.
3. **Model Training**: Testing Linear Regression, Random Forest, XGBoost, Neural Networks, and Stacking methods.
4. **Evaluation**: Using RMSE and R² for comparison.

---

## Dataset Description

The dataset contains 50,000 car listings with features like:
- Brand
- Model year
- Mileage
- Fuel type
- Transmission
- Engine specifications
- Accident history
- Price (target variable)

---

## Preprocessing and Feature Engineering

### Key Steps:
- **Handling Missing Values**: Filling numeric values with the mean and categorical values with the mode.
- **Feature Extraction**:
  - Engine specifications parsed to derive horsepower, displacement, and configuration.
  - Car age calculated using the model year.
- **Encoding**:
  - Target encoding for categorical features like brand and transmission.
  - One-hot encoding for fuel types.
- **Scaling**: StandardScaler applied to numeric features for uniformity.

---

## Models and Training

### Models Tested:
1. **Linear Regression** (Baseline)
2. **Ensemble Models**:
   - Random Forest
   - Gradient Boosting
   - XGBoost
3. **Neural Networks**: Three-layer architecture with ReLU activation and dropout.
4. **Stacking Models**: Combining predictions from multiple models like Neural Networks, Random Forest, and ElasticNet.

---

## Results and Performance

### Model Performance Summary:
| Model                       | RMSE      | R²     |
|-----------------------------|-----------|--------|
| Linear Regression           | 47,934.80 | 0.6282 |
| Gradient Boosting           | 48,068.26 | 0.6594 |
| Neural Network              | 48,521.12 | 0.6526 |
| **Stacking Model** (NN+RF+ElasticNet) | **48,787.41** | **0.6744** |

**Best RMSE**: Neural Network + RF + ElasticNet (48,787.41)  
**Best R²**: LightGBM + Extra Trees + Linear (0.6801)

---

## Key Findings

1. Ensemble methods like Gradient Boosting and XGBoost outperformed simpler models.
2. Stacking models showed the highest accuracy with RMSE and R² trade-offs.
3. Preprocessing steps such as logarithmic transformation and feature extraction enhanced model performance.

---

## References

1. Breiman, L. (2001). *Random Forests*. Machine Learning, 45(1), 5-32.
2. Pedregosa, F., et al. (2011). *Scikit-learn: Machine Learning in Python*. Journal of Machine Learning Research, 12, 2825-2830.
3. Chen, T., Guestrin, C. (2016). *XGBoost: A Scalable Tree Boosting System*. ACM SIGKDD.

---

## Contributors

- Madhav Gupta (2022EE11737)
- Arunim Garg (2022EE32002)
- Vatsal Jain (2022EE11672)  
Department of Electrical Engineering, IIT Delhi
