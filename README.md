# SCT_ML_2: House Price Prediction (Linear Regression)

Task 2 of the SkillCraft Technology Machine Learning internship.

**Goal:** predict house sale prices from living area, bedrooms and bathrooms.

**Dataset:** House Prices (Ames housing), `train.csv`. The columns used are `GrLivArea` (square footage), `BedroomAbvGr` (bedrooms), `FullBath` (bathrooms) and `SalePrice` (target). Only full bathrooms are used, since the dataset has no half-bath count.

## Method
1. Select and rename the four columns.
2. Drop rows with missing values.
3. Split 80% train / 20% test (`random_state=42`).
4. Fit `LinearRegression` on the three features.
5. Evaluate with MAE, RMSE and R².

## Results
| Metric | Value |
|---|---|
| MAE | [35,788.06] |
| RMSE | [ 52,975.72] |
| R² | [0.6341] |

Coefficients are in `outputs/metrics.txt`. `outputs/actual_vs_predicted.png` plots predicted against actual prices.

## How to run
1. Open `SCT_ML_2.ipynb` in Google Colab (File → Upload notebook, or open it from GitHub).
2. Upload `train.csv` to the Colab Files panel, renamed `house_prices.csv` if you used that name.
3. Run all cells (Runtime → Run all).

## Files
- `SCT_ML_2.ipynb`: Colab notebook with the full run and outputs
- `linear_regression.py`: the same code as a script
- `outputs/`: metrics, plot and saved model
