# DVD Rental Duration Prediction

This project aims to help a DVD rental company predict how many days a customer will rent a DVD, using regression modeling. Accurate rental duration predictions can improve inventory planning and overall efficiency.

## Objective

Develop a regression model that predicts rental duration (in days) with a **mean squared error (MSE) of 3 or less** on a test set.

## Tools & Technologies

- **Python**
- **Jupyter Notebooks**
- **scikit-learn**: For model building, evaluation, and hyperparameter tuning

## Dataset

The dataset is provided in `rental_info.csv` and includes the following features:

- `rental_date`, `return_date`: Timestamps for when the DVD was rented and returned
- `amount`, `amount_2`: Rental amount paid and its square
- `rental_rate`, `rental_rate_2`: Rate of rental and its square
- `release_year`: Year the movie was released
- `length`, `length_2`: Movie length (in minutes) and its square
- `replacement_cost`: Cost to replace the DVD
- `special_features`: Special features like trailers or deleted scenes
- `NC-17`, `PG`, `PG-13`, `R`: Dummy variables representing movie ratings (reference category dropped)

## Approach

- Performed **data cleaning and feature engineering** using pandas
- Tuned models using **RandomizedSearchCV**
- Trained two models:
  - **Random Forest Regressor**: Final predictive model
  - **Lasso Regression**: Used for analyzing feature importance

## Results

- **Final model**: Random Forest Regressor
  - `n_estimators = 51`
  - `max_depth = 10`
- **Achieved Test MSE**: `2.2263` — meets the performance requirement

## Notes

- Lasso regression was used to explore which features most influenced rental duration
- The modeling workflow includes preprocessing, feature engineering, model training, and evaluation, all within a Jupyter Notebook environment



## Notes

- Lasso regression was used primarily for feature selection and coefficient interpretation.
- The workflow includes data preprocessing, feature engineering, model selection, and evaluation.

