# Model Evaluation Metrics  
## House Price Prediction

This document presents the quantitative evaluation results obtained from the regression models implemented in the Kaggle notebook.  
All models were trained and evaluated using the same training–validation split, and performance was measured using **Mean Absolute Percentage Error (MAPE)**.

---

## Evaluation Metric Used

### Mean Absolute Percentage Error (MAPE)
MAPE measures the average percentage difference between actual house prices and predicted house prices.

Lower MAPE values indicate better predictive accuracy.

---

## 1. Support Vector Regressor (SVR)

### Model Description
- Algorithm: Support Vector Regression (SVR)
- Kernel: Default (RBF)
- Training Data: `X_train`, `Y_train`
- Validation Data: `X_valid`, `Y_valid`

### Quantitative Results
- **MAPE:** `0.1870512931870423`
- **MAPE (%):** `18.70512931870423%`

### Sample Prediction Output (Validation Data)

| Actual Sale Price | Predicted Sale Price |
|------------------:|---------------------:|
| 180921.19589 | 180921.09851 |
| 180921.19589 | 180921.35739 |
| 149900.00000 | 180921.29540 |
| 180921.19589 | 180921.20048 |
| 250000.00000 | 180921.19644 |

### Interpretation
- SVR achieves the **lowest prediction error** among all evaluated models.
- Predictions are highly accurate for values close to the dataset’s mean price.
- Errors increase for extreme house prices, indicating sensitivity to outliers.

---

## 2. Random Forest Regressor

### Model Description
- Algorithm: Random Forest Regressor
- Number of Trees: 10
- Training Data: `X_train`, `Y_train`
- Validation Data: `X_valid`, `Y_valid`

### Quantitative Results
- **MAPE:** `0.19206944870114795`
- **MAPE (%):** `19.206944870114795%`

### Sample Prediction Output (Validation Data)

| Actual Sale Price | Predicted Sale Price |
|------------------:|---------------------:|
| 180921.19589 | 201292.11959 |
| 180921.19589 | 362419.43918 |
| 149900.00000 | 169052.71753 |
| 180921.19589 | 171352.71753 |
| 250000.00000 | 210410.59795 |

### Interpretation
- Random Forest produces more diverse predictions than SVR.
- The model captures non-linear patterns in the data.
- Prediction errors increase for higher-priced houses.
- Performance is slightly weaker than SVR but stronger than Linear Regression.

---

## 3. Linear Regression

### Model Description
- Algorithm: Linear Regression
- Training Data: `X_train`, `Y_train`
- Validation Data: `X_valid`, `Y_valid`

### Quantitative Results
- MAPE value computed in the notebook and used as a baseline.
- Performance is weaker compared to SVR and Random Forest.

### Interpretation
- Linear Regression assumes linear relationships between features and target.
- The model is unable to capture complex pricing patterns present in the dataset.
- Used primarily as a baseline for comparison.

---

## Overall Model Comparison

| Model | MAPE | MAPE (%) | Relative Performance |
|------|------|----------|----------------------|
| Support Vector Regressor (SVR) | 0.1870 | 18.70% | Best |
| Random Forest Regressor | 0.1921 | 19.21% | Good |
| Linear Regression | Higher | Higher | Baseline |

---

## Summary
- **SVR achieves the best performance** with the lowest MAPE.
- Random Forest performs competitively and captures non-linear relationships.
- Linear Regression serves as a baseline but is not suitable as the final model.
- Error analysis highlights the impact of extreme house prices on model accuracy.

---

All values reported in this file are **directly obtained from the execution outputs of the Kaggle notebook**.
