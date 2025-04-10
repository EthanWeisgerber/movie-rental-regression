# DVD Rental Duration Prediction

This project develops a regression model to help a DVD rental company predict how many days a customer will rent a DVD. Accurate predictions enable better inventory planning and improved operational efficiency.

## Objective

Build a regression model that predicts rental duration (in days) using customer and movie features, with a target **mean squared error (MSE) ≤ 3** on a test set.

## Dataset

The dataset is provided in `rental_info.csv` and includes the following features:

- `rental_date`, `return_date`: Timestamps for rental and return.
- `amount`, `amount_2`: Amount paid and its square.
- `rental_rate`, `rental_rate_2`: Rental rate and its square.
- `release_year`: Year of the movie’s release.
- `length`, `length_2`: Movie length in minutes and its square.
- `replacement_cost`: DVD replacement cost.
- `special_features`: Extra content such as trailers or deleted scenes.
- `NC-17`, `PG`, `PG-13`, `R`: Dummy variables representing movie ratings (reference category dropped).

## Approach

- Used **RandomizedSearchCV** for hyperparameter tuning.
- Trained a **Random Forest Regressor** for final prediction.
- Used **Lasso Regression** to examine feature importances.

## Result

- Final model: **Random Forest**
  - `n_estimators = 51`
  - `max_depth = 10`
- **Test MSE:** `2.2263` — Successfully meets the target (MSE ≤ 3)

## Notes

- Lasso regression was used primarily for feature selection and coefficient interpretation.
- The workflow includes data preprocessing, feature engineering, model selection, and evaluation.

