# NYC Rental Price Regression 📊🏙️

This repository contains an end-to-end regression analysis of New York City apartment rents using a simple **linear-regression** model. 

---

## Project Overview
The objectives of this analysis are to:

* **Load** the raw NYC rental dataset from a public URL.  
* **Wrangle** data by removing extreme outliers in price and geographic coordinates.  
* **Visualize** how rent varies with the number of bedrooms via scatter plots.  
* **Establish a baseline** MAE by always predicting the average rent.  
* **Build** an OLS regression model 
* **Evaluate** performance using MAE and RMSE.  
* **Interpret** model coefficients and predict rent for a 2-bedroom apartment.

---

## Requirements
Install the following libraries before running the notebook:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
