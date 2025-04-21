# house-price-regression
Complete machine learning pipeline for predicting house prices: data cleaning, encoding, outlier removal, and regression model comparison using the Ames Housing dataset from Kaggle.


## Project Overview
1. Library Imports & Versions
2. Dataset Overview
3. Data Cleaning & Preprocessing
4. Visualization 
5. Checking Outliers
6. Checking Correlation
7. Preparing the data
8. Model Training & Evaluation
9. Final Model Selection

## Model Choice Justification
Why XGBoost with Threshold = 0.001 Was Chosen

After experimenting with different feature importance thresholds, we found that using a threshold of 0.001 produced the best balance between model performance and feature count. This threshold retained 59 important features, which allowed the model to learn effectively while still maintaining a manageable level of complexity.

Among all evaluated models (including Ridge, Lasso, ElasticNet, Decision Trees, Random Forests, and Extra Trees), XGBoost consistently outperformed others in terms of:

- Lowest RMSE (19,278)
- Lowest MAE (13,267)
- Highest R² (0.92)
- Lowest MAPE (8.24%)

These metrics indicate that the model has a strong predictive capability, generalizes well to unseen data, and makes relatively low-error predictions even in percentage terms (as shown by MAPE).

Moreover, XGBoost offers several benefits, such as regularization to prevent overfitting, built-in feature importance metrics, and fast training times. These characteristics make it a robust and reliable choice for this regression task.

In conclusion, XGBoost with threshold = 0.001 was selected as the final model because it delivered the best overall performance, balancing accuracy, stability, and computational efficiency.
