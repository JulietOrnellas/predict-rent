# NYC Rental Price Regression 📊🏙️

This repository contains two end-to-end regression analyses of New York City apartment rents using a simple **linear-regression** model:  
1. **Version 1 (predict-rent_v1.ipynb)**  
2. **Version 2 (predict-rent_v2.ipynb)** 
---

## Project Overview

We have two separate notebooks, each demonstrating a complete “load → wrangle → model → evaluate” pipeline on the same raw dataset:

1. **Version 1 (`predict-rent_v1.ipynb`)**  
   - **Load** the raw NYC rental dataset from a public URL.  
   - **Wrangle** by removing extreme outliers in price and geographic coordinates (basic trimming).  
   - **Visualize** how rent varies with the number of bedrooms via scatter plots.  
   - **Establish a baseline** MAE by always predicting the average rent.  
   - **Build** an OLS (ordinary least squares) regression model on the cleaned data.  
   - **Evaluate** performance using MAE and RMSE.  
   - **Interpret** model coefficients and predict rent for a 2-bedroom apartment.

2. **Version 2 (`predict-rent_v2.ipynb`)**  
   - **Load** the same raw dataset as v1.  
   - **Wrangle** with a revised approach:  
     1. Drop nulls.  
     2. Create an `expensive` flag (`price > 3000 ? 'yes' : 'no'`).  
     3. Create a `total` feature (`bedrooms + bathrooms`).  
     4. Trim price to its 0.5th–99.5th percentile (removes the top/bottom 0.5%).  
     5. Trim latitude/longitude to their 0.05th–99.95th percentiles (removes the outer 0.1% of GPS outliers).  
   - **Visualize** updated feature relationships (e.g., new `total` or `expensive` segments).  
   - **Establish a new baseline** MAE on the revised training set.  
   - **Build** a fresh OLS regression model using the new feature set.  
   - **Evaluate** updated performance (MAE, RMSE, R² on train/test split).  
   - **Interpret** the new coefficients (e.g., how `bedrooms`, `bathrooms`, `total`, and `expensive` influence rent).

---

## How to Run

1. **Clone the repository**  
   ```bash
   git clone https://github.com/JulietOrnellas/predict-rent.git
   cd predict-rent

