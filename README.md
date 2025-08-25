# Predictive Movie Rental Duration 🎬

## Overview
This project predicts the number of days a customer will rent a DVD based on features such as rental rate, movie length, release year, and special features.  
The goal is to provide a regression model with **Mean Squared Error (MSE) ≤ 3** on the test set, helping the company improve inventory planning and operational efficiency.

---

## Dataset
The dataset comes from `rental_info.csv` and includes the following features:

- **rental_date**: Date/time when the DVD was rented  
- **return_date**: Date/time when the DVD was returned  
- **amount / amount_2**: Rental fee and its square  
- **rental_rate / rental_rate_2**: Rental rate and its square  
- **release_year**: Year the movie was released  
- **length / length_2**: Movie length (minutes) and its square  
- **replacement_cost**: Cost to replace the DVD  
- **special_features**: Features like trailers, deleted scenes, etc.  
- **NC-17, PG, PG-13, R**: Dummy variables for movie ratings  

---

## Methods
Two regression approaches were tested:

1. **Lasso + OLS Regression**  
   - Feature selection using Lasso  
   - Followed by Ordinary Least Squares (OLS) regression

2. **Random Forest Regression**  
   - Hyperparameter tuning using `RandomizedSearchCV`

**Evaluation Metric:** Mean Squared Error (MSE)

---

## Results

| Model          | MSE    |
|----------------|--------|
| Lasso + OLS    | ~4.81  |
| Random Forest  | ~2.22 ✅ |

- ✅ **Best model:** Random Forest Regressor  
- ✅ **Best MSE:** 2.22 (requirement achieved: MSE ≤ 3)

---

## Conclusion
The **Random Forest Regressor** achieved the best performance with an MSE of 2.22, meeting the company’s requirement.  
This model can be used to optimize inventory management and rental planning for DVDs.
