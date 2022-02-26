# Airbnb Price Prediction

Current Progress:
- Preprocessing: 
   1) Removed listings with invalid names, 
   2) Removed 'id', and 'host_name' columns for ethical considerations, 
   3) Removed observations with NaN values in last_review (date value) since listings with no reviews will have no last_review.
- EDA: 
   1) Created a Correlogram of the 14 remaining variables. Identified number of reviews and reviews per month to be highly correlated. No other pair of variables was highly correlated with high correlation defined at $|r_ij| \ge 0.5$. Shown in preprocessing&eda.ipynb
   2) Created a Word cloud from listing names. Shown in preprocessing&eda.ipynb

- Modelling Procedure:
  1) Ridge Regression
  2) Linear Regression (OLS)
  3) Lasso
  4) ...

- Evaluation: (accuracy and time complexity
  - Metric: MSE? 

Contributors: Mikaela Lim, Gianni Spiga, Sharon Vien, Kevin Xu
