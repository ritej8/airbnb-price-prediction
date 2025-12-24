# airbnb-price-prediction
Predicting Airbnb prices using data analysis and machine learning
Results
Model Performance Summary

Several models were evaluated to predict Airbnb listing prices using a subset of numerical and categorical features.

| Model                   | Target                | R² Score | MAE      |
| ----------------------- | --------------------- | -------- | -------- |
| Linear Regression       | Raw Price             | ~0.04    | High     |
| Linear Regression       | Log-Transformed Price | ~0.16    | Improved |
| Random Forest Regressor | Log-Transformed Price | **0.22** | **0.91** |


The baseline Linear Regression model performed poorly due to the highly skewed price distribution and sensitivity to outliers. Applying a logarithmic transformation to the target variable significantly improved model stability and predictive performance.

The Random Forest model achieved the best overall results, confirming that the relationship between listing features and price is non-linear.

Key Insights

Bedrooms is the strongest predictor of price.

Accommodates (listing capacity) has a strong positive impact on pricing.

Review scores contribute to price variation but with weaker influence.

Linear models struggle to capture Airbnb pricing behavior without transformations.

Interpretation of Results

An 
𝑅
2
R
2
 score of 0.22 indicates that the model explains approximately 22% of the variance in listing prices using a limited feature set. While this may seem modest, it is expected for real-world pricing data influenced by many unobserved factors such as exact location, seasonality, and host behavior.

The Mean Absolute Error (MAE) of 0.91 on the log-transformed scale reflects reasonable predictive accuracy for a first end-to-end machine learning project.

Limitations

Limited feature engineering

No temporal or seasonal effects included

Location granularity simplified

No hyperparameter tuning applied

Future Improvements

Add geospatial features (distance to city center, clustering)

Apply advanced preprocessing pipelines

Tune models using GridSearchCV

Incorporate additional features such as availability and amenities
