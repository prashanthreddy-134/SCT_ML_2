# SCT_ML_3– House Price Prediction (Linear Regression)

**Task:** Implement a linear regression model to predict house prices from square footage, number of bedrooms and number of bathrooms.
**Dataset:** House Price Dataset (link in the internship brief).

## Setup
```bash
pip install -r requirements.txt
```
Place the CSV at `data/house_prices.csv`. The script detects common column names (for example `sqft_living` or `Square_Footage`, `Bedrooms`, `Bathrooms`, `Price`) and reports clearly if one is missing.

## Run
```bash
python linear_regression.py --data data/house_prices.csv
python linear_regression.py --predict 2000 3 2     # predict price for 2000 sq ft, 3 beds, 2 baths
```

## Method
1. Load the data, keep the four required columns and drop rows with missing values.
2. Split 80% train / 20% test (`random_state=42`).
3. Fit `LinearRegression` on the three features.
4. Evaluate with MAE, RMSE and R².

## Outputs (`outputs/`)
- `metrics.txt`: MAE, RMSE, R² and model coefficients
- `actual_vs_predicted.png`: scatter plot of actual against predicted prices
- `linear_regression_model.joblib`: saved model

## Results
Fill in after running: MAE ____  RMSE ____  R² ____
