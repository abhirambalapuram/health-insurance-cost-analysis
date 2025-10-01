# **Health Insurance Cost Analysis (Linear Regression)**

Analyze the classic insurance.csv dataset and build a Linear Regression model to predict medical insurance charges from demographic and lifestyle factors.

## Objective

Explore relationships between age, sex, BMI, children, smoker, region and charges

Train a reproducible regression pipeline with preprocessing

Report metrics (R², RMSE, MAE) and interpret coefficients

## Dataset

Source: Kaggle “Medical Cost Personal Dataset” (mirichoi0218)

Public raw mirror used in notebook: stedy/Machine-Learning-with-R-datasets/insurance.csv

Columns: age, sex, bmi, children, smoker, region, charges

Note: All data are public and contain no PHI/PII.

## Methods

Train/validation split, 80/20

ColumnTransformer: StandardScaler for numeric features and OneHotEncoder for categorical features

Model: LinearRegression (plus optional Lasso baseline)

RMSE calculated manually using np.sqrt(mean_squared_error(...)) for compatibility across scikit-learn versions

## Results (example from one run)

Linear Regression: R² around 0.75–0.80, RMSE around 6000–8000, MAE around 4000–5000

Key signal: smoker=yes is the strongest driver of higher charges; BMI and age also increase costs

Exact numbers may vary depending on environment and random split.

## Outputs

Predicted vs Actual scatter plot and residuals plot

Coefficient table with feature names (after encoding)

Group summaries (e.g., average charges for smokers vs non-smokers)

## Tech Stack

Python, pandas, NumPy, scikit-learn, matplotlib
