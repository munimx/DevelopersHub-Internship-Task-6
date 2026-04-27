Munim Ahmad -- DHC-3052 -- DeveloperHub Corporation Internship

# Task 6: House Price Prediction

This project predicts house prices from property features (such as area,
bedrooms, bathrooms, and related attributes) using regression models.

## Project Files

- `task_6_house_price_prediction.ipynb` — Main notebook with data loading,
  preprocessing, model training, visualizations, and evaluation.
- `Housing.csv` — Dataset used for training/testing.

## Dataset Information

- **Source (Kaggle):**
  [Housing Prices Dataset by yasserh](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset?resource=download)
- **Dataset title:** Housing Prices Dataset
- **File used in this project:** `Housing.csv`
- **Size/shape:** 1 CSV file, `545` samples (rows), `13` columns (Kaggle lists
  this as 13 features/samples summary)
- **Kaggle metadata:** Usability `10.0`, expected update frequency: `Annually`,
  tag: `Real Estate`
- **License:**
  [CC0 1.0 (Public Domain)](https://creativecommons.org/publicdomain/zero/1.0/)

### Columns in `Housing.csv`

- `price` (target)
- `area`
- `bedrooms`
- `bathrooms`
- `stories`
- `mainroad`
- `guestroom`
- `basement`
- `hotwaterheating`
- `airconditioning`
- `parking`
- `prefarea`
- `furnishingstatus`

### Dataset Context

Per the Kaggle description, this is a house-price regression dataset intended
for predictive modeling with variables like area, bedroom count, furnishing, and
location-related amenities. The challenge includes potential multicollinearity
across predictors.

### License Note (CC0)

CC0 indicates the dataset is dedicated to the public domain: it can be copied,
modified, and used (including commercially) without requesting permission. As
with most open datasets, it is provided **as-is** without warranty.

## Objective

Build and evaluate a house-price regression pipeline that:

1. Loads the dataset
2. Preprocesses numeric and categorical features
3. Trains regression models (Linear Regression and Gradient Boosting)
4. Visualizes predicted vs actual prices
5. Reports Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE)

## What the Notebook Does

- Loads `Housing.csv`
- Automatically identifies the target column (`price`)
- Splits data into train/test sets
- Applies preprocessing using a `ColumnTransformer`:
  - Numeric: median imputation + standard scaling
  - Categorical: most-frequent imputation + one-hot encoding
- Trains and compares:
  - Linear Regression
  - Gradient Boosting Regressor
- Evaluates with MAE and RMSE
- Generates:
  - Predicted vs Actual scatter plot
  - Residual plot

## Last Verified Run (in this workspace)

- Dataset shape: `545 x 13`
- Train/Test split: `436 / 109`
- Best model (by RMSE): **Gradient Boosting**
- Metrics:
  - Gradient Boosting: MAE ≈ `969,687.93`, RMSE ≈ `1,302,052.72`
  - Linear Regression: MAE ≈ `970,043.40`, RMSE ≈ `1,324,507.00`

## How to Run

1. Open `task_6_house_price_prediction.ipynb` in VS Code/Jupyter.
2. Ensure `Housing.csv` is in the same folder.
3. Run all notebook cells from top to bottom.

## Notes for Reviewers

- The notebook is written to be readable and modular, with clear sectioning for
  each task requirement.
- Model comparison and visual diagnostics are included to make evaluation
  transparent.
