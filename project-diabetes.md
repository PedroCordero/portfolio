### Lazy Learning for Disease Progression Prediction using kNN and Radius Neighbors Regression

This project applies lazy learning algorithms — specifically K-Nearest Neighbors (kNN) and Radius Neighbors Regressor (RNR) — to predict diabetes disease progression from a real-world dataset. The dataset contains 10 clinical features including blood pressure, body mass index (BMI), and serum measurements. Cross-validation and hyperparameter tuning are used to maximize model performance.

![diabetes](/assets/img/project-diabetes.gif)

#### Key Features  

- Real-world medical dataset (Diabetes).
- Full feature utilization (10 clinical predictors).
- Feature standardization (important for distance-based models).
- Hyperparameter tuning using GridSearchCV
- Model evaluation with MSE and R² Score

![diabetes](/assets/img/project-diabetes.png)

### Results:

| Model | Best Param | R² Score | MSE |
|-------|-------------|----------|------|
| KNN   | k = 18      | 0.42     | 3058 |
| RNR   | radius = 5.0| 0.24     | 4035 |

- With all 10 features, KNN significantly outperforms RNR.
- Radius Neighbors is less stable unless tuned with large radii.
- R² = 0.42 implies moderate predictive power from non-parametric models.
- Standardization is essential for distance-based learning.
- R² = 0.42 is a decent result for non-parametric models on noisy, real-world health data — it indicates the model is extracting some structure, but more sophisticated models (like Random Forest or XGBoost) could do better.

![diabetes](/assets/img/project-diabetes2.png)

*Regression Results: True vs Predicted.*

![diabetes](/assets/img/project-diabetes3.png)

*Results: Kernel density estimation (KDE).*

[back](./)
