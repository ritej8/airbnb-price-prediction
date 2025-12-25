# Airbnb Price Prediction

Predicting Airbnb listing prices using exploratory data analysis and machine learning with scikit-learn pipelines.

 Project Overview

This project aims to predict Airbnb listing prices based on property characteristics such as room type, capacity, bedrooms, and review scores.
It demonstrates a complete machine learning workflow, from data exploration to preprocessing pipelines and model evaluation.
| Model                        | Target        | R² Score | RMSE / MAE      |
| ---------------------------- | ------------- | -------- | --------------- |
| Linear Regression            | Raw Price     | ~0.04    | High error      |
| Linear Regression            | Log-Price     | ~0.16    | Improved        |
| Random Forest (no pipeline)  | Log-Price     | ~0.22    | MAE ≈ 0.91      |
| **Random Forest (Pipeline)** | **Log-Price** | **0.82** | **RMSE ≈ 0.30** |

Final Model

Random Forest Regressor

Target variable transformed using log1p

Full preprocessing handled inside a scikit-learn Pipeline using ColumnTransformer

🔍 Key Insights

Bedrooms is the strongest predictor of price.

Accommodates (listing capacity) has a strong positive impact on pricing.

Room type significantly affects price (entire homes cost substantially more).

Review scores contribute to pricing but with weaker influence.

Linear models struggle due to skewed distributions and non-linear relationships.

📊 Interpretation of Results

An R² score of 0.82 indicates that the final pipeline-based model explains most of the variance in Airbnb prices using a limited but meaningful feature set.

The RMSE of ~0.30 on the log-transformed scale reflects strong predictive performance given the inherent noise in real-world pricing data, which is influenced by unobserved factors such as exact location, seasonality, and host behavior.

This improvement highlights:

The importance of log-transforming skewed targets

The effectiveness of tree-based models

The critical role of pipelines in preventing data leakage

⚙️ Tools & Techniques

Python, NumPy, pandas

Matplotlib, Seaborn

scikit-learn

Pipelines

ColumnTransformer

Random Forest Regressor

Cross-validation

# Limitations

Limited feature engineering

No temporal or seasonal effects

Simplified location representation

No advanced hyperparameter tuning

# Future Improvements

Add geospatial features (distance to city center, clustering)

Perform hyperparameter tuning with GridSearchCV

Include additional features such as availability and amenities

Experiment with Gradient Boosting models features such as availability and amenities
