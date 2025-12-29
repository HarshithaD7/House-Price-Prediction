# Model Observations and Analysis  
## House Price Prediction

---

## Models Evaluated
The following regression models were implemented and evaluated on the same training–validation split:
- Linear Regression
- Support Vector Regressor (SVR)
- Random Forest Regressor

Model performance was evaluated using **Mean Absolute Percentage Error (MAPE)**.

---

## Support Vector Regressor (SVR)
- The SVR model achieved the **lowest error**, with a **MAPE of 0.1870 (18.70%)**.
- Predictions are strongly centered around the mean house price (~180,921), indicating that the model has learned the overall pricing trend well.
- The model performs accurately for houses priced near the dataset’s average.
- However, SVR shows limited sensitivity to extreme values, such as significantly higher-priced houses (e.g., 250,000).

---

## Random Forest Regressor
- The Random Forest model achieved a **MAPE of 0.1921 (19.21%)**, slightly higher than SVR.
- The model generates more diverse predictions compared to SVR.
- It captures non-linear relationships better than Linear Regression.
- Some overestimation and underestimation are observed for higher-priced houses.

---

## Linear Regression
- Linear Regression was used as a **baseline model**.
- Its performance is weaker compared to SVR and Random Forest.
- The model is limited by its assumption of linear relationships and cannot fully capture complex housing price patterns.

---

## Comparative Insights
- SVR performs best among all evaluated models in terms of prediction accuracy.
- Random Forest performs competitively and offers better variability in predictions.
- Linear Regression serves as a reference model but is not suitable as the final predictive model.

---

## Conclusion
Based on observed prediction behavior and quantitative error values, the **Support Vector Regressor (SVR)** is the most suitable model for this house price prediction task.  
Further improvements can be achieved through feature engineering and advanced ensemble techniques.
