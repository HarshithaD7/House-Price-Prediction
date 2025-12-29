# House Price Prediction  
## Detailed Project Report

---

## 1. Introduction
Accurate house price prediction is an important problem in real estate analytics, as it helps buyers, sellers, and investors make informed decisions.  
This project focuses on predicting house sale prices using supervised machine learning regression techniques implemented in a **Kaggle Notebook environment**.

Multiple regression models are trained and evaluated to identify the most accurate approach for predicting house prices based on historical data.

---

## 2. Problem Statement
The objective of this project is to build a machine learning model that can **predict house sale prices** using available property-related features.

This is formulated as a **regression problem**, where the target variable is a continuous numerical value representing the sale price of a house.

---

## 3. Dataset Description
- The dataset contains structured housing data with numerical and categorical attributes.
- Each row represents a single house.
- The target variable is **SalePrice**.

### Key characteristics:
- Real-world housing dataset
- Presence of both low-priced and high-priced houses
- Variability in feature values affecting sale price

Due to GitHub file size constraints, only sample datasets are included in the repository.  
The full dataset is accessed and processed directly within the Kaggle Notebook.

---

## 4. Data Preprocessing
The following preprocessing steps were applied:

- Loading and inspecting the dataset using exploratory commands
- Separating input features (`X`) and target variable (`Y`)
- Splitting the dataset into **training** and **validation** sets
- Preparing the data for regression model training

These steps ensure consistency and fair comparison across all regression models.

---

## 5. Models Implemented
Three regression models were implemented and evaluated:

### 5.1 Linear Regression
- Used as a **baseline model**
- Assumes a linear relationship between input features and house prices
- Simple and interpretable but limited in capturing complex patterns

### 5.2 Support Vector Regressor (SVR)
- Non-linear regression model
- Effective in capturing general pricing trends
- Sensitive to feature distribution and extreme values

### 5.3 Random Forest Regressor
- Ensemble-based regression model
- Combines multiple decision trees
- Capable of modeling non-linear relationships and interactions between features

---

## 6. Evaluation Metric
### Mean Absolute Percentage Error (MAPE)

MAPE measures the average percentage difference between actual and predicted house prices.

- Lower MAPE values indicate better predictive performance
- MAPE is suitable for comparing regression models on price prediction tasks

---

## 7. Model Evaluation Results

### 7.1 Support Vector Regressor (SVR)
- **MAPE:** **0.1870512931870423**
- **MAPE (%):** **18.70%**

SVR achieved the **lowest error** among all evaluated models, indicating the highest predictive accuracy.

Predictions are highly consistent for houses priced near the dataset’s average value (~180,921).  
However, the model shows larger deviations for extreme values such as significantly higher-priced houses.

---

### 7.2 Random Forest Regressor
- **MAPE:** **0.19206944870114795**
- **MAPE (%):** **19.21%**

Random Forest performs competitively and produces more varied predictions than SVR.  
It captures non-linear patterns in the data but shows slightly higher error compared to SVR, particularly for high-priced houses.

---

### 7.3 Linear Regression
- Used as a baseline model
- Produces higher error compared to SVR and Random Forest
- Limited by its assumption of linearity

Linear Regression is useful for comparison but is not suitable as the final predictive model.

---

## 8. Comparative Analysis
- **SVR performs best** in terms of predictive accuracy
- Random Forest provides strong performance and better flexibility
- Linear Regression performs weakest among the three models

The comparison highlights the importance of using non-linear models for real-world house price prediction.

---

## 9. Observations
- Most prediction errors occur for houses with prices far from the mean
- SVR predictions are concentrated around the central price range
- Random Forest handles price variability better but with slightly higher error
- Model performance is influenced by data distribution and outliers

---

## 10. Conclusion
This project demonstrates the application of machine learning regression techniques for predicting house prices.

Among all evaluated models, **Support Vector Regressor (SVR)** achieved the **best performance** with the lowest Mean Absolute Percentage Error.  
Random Forest also performed well, while Linear Regression served as a baseline reference.

The results confirm that non-linear models are better suited for complex real-world pricing problems.

---

## 11. Future Improvements
- Feature engineering to better capture price-driving factors
- Hyperparameter tuning for SVR and Random Forest
- Handling outliers to improve performance on extreme prices
- Applying advanced ensemble methods such as Gradient Boosting or XGBoost
- Deploying the model as a web-based price prediction tool

---

## 12. References
- Scikit-learn Documentation
- Kaggle Housing Dataset
- Machine Learning Regression Techniques
