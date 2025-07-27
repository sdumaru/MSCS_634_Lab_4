# Lab 4: Regression Analysis with Regularization Techniques
**Course**: MSCS 634 – Advanced Big Data and Data Mining

## Purpose
The goal of this lab was to investigate a wide variety of regression models including regularized models implemented on the Diabetes dataset. The lab was focused on seeing how various regression methods work on real world data, and what regularization can do to control model complexity.

## Models Implemented
- **Simple Linear Regression** (using BMI as the predictor)
- **Multiple Linear Regression** (using all features)
- **Polynomial Regression** (degree = 2)
- **Ridge Regression** (L2 regularization)
- **Lasso Regression** (L1 regularization)

## Key Insights

- **Simple Linear Regression** underfit the data with a low R² of 0.233, showing limited predictive power using only BMI.
- **Multiple Linear Regression** significantly improved performance (R² = 0.453), demonstrating that most features contribute meaningfully to predicting disease progression.
- **Polynomial Regression** captured non-linearity but underperformed slightly compared to linear and regularized models (R² = 0.416).
- **Ridge Regression** offered coefficient stability and improved generalization (R² = 0.419), though it didn't outperform simpler models.
- **Lasso Regression** was the best-performing model (R² = 0.472, RMSE = 52.90), showing that feature selection via L1 regularization enhanced both accuracy and interpretability.

## Visualization Summary
Actual vs. predicted plots were constructed for all models. These showed that:
- The two techniques closest to actual values are Lasso and Multiple Linear Regression.
- Polynomial Regression was able to capture some non-linear trend but also have some spread.
- Predictions of simple linear were scattered as the model was not well-fitted.

## Hyperparameter Tuning
For Ridge and Lasso regression, an alpha-R² plot was produced with a log scale. This assisted in the visualization of how regularization strength ultimately impacts performance and it reaffirmed that Lasso works at its best at mid-range alpha values.

## Challenges Faced
- First multiple regression was incorrectly run with a single predictor (BMI). Fixing this revealed a major performance improvement.
- Deciding on the optimal polynomial degree and alpha values required experimentation and tuning.
- A close monitoring of outputs was necessary to maintain consistency between insights, visualizations and metrics.

## Conclusion
 This lab showed the importance of using features and regularization in real-world data. As a result, Lasso Regression was not only a more intuitive model in theory, it was also the best model in practice, giving evidence to the power of sparsity and feature selection when doing regressions.

## Files Included
- `lab4_notebook.ipynb`: Full Jupyter Notebook with code, evaluation, and visualizations
- `README.md`: Summary of lab purpose, insights, and outcomes
