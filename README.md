# Airbnb Price Prediction
------------------------------------------
Current Progress:
- Preprocessing: 
   1) Removed listings with invalid names, 
   2) Removed 'id', and 'host_name' columns for ethical considerations, 
   3) Removed observations with NaN values in last_review (date value) since listings with no reviews will have no last_review.

- EDA: [In Progress]
   1) Created a Correlogram of the 14 remaining variables. Identified number of reviews and reviews per month to be highly correlated. No other pair of variables was highly correlated with high correlation defined at $|r_ij| \ge 0.5$. Shown in preprocessing&eda.ipynb
   2) Created a Word cloud from listing names. Shown in preprocessing&eda.ipynb
   3) ...

- Modelling Procedure: [In Progress]
  1) Linear Regression (OLS)
  2) Ridge Regression
  3) Lasso 
    - Overview the Lasso model, unique attributes, and optimization process. 
    - Show difference from Ridge. (plot beta coeffs as $\lambda -> \inf$ for Lasso and Ridge to show the difference between the two shrinkage methods. (Lasso: Betas reach 0. Ridge: Betas reach ~ 0)
    - Run various direct/iterative methods to solve for Lasso coefficients (LU, QR, Cholesky, Gauss-Seidel, SVD, Power), and show derivation.
    - If time permits, repeat for Multi-task Lasso.
  4) ... 

- Evaluation: (accuracy and time complexity
  - Metric: MSE, run time, generalizability/interpretatbility.

------------------------------------------

Navigating this project:
* `./data`: contains 2 .csv files containing raw and preprocessed AirBnB data originally sourced from kaggle.com.
  - `AB_NYC_2019.csv`: contains raw airbnb dataset from kaggle.
  - `listings.csv`: contains preprocessed data with 38837 rows × 14 columns.
* `./notebooks`: contains jupyter notebooks of our preprocessing, EDA, modelling, and testing. 
  - `preprocessing&eda.ipynb` contains preprocessing and eda.
  - `OLS.ipynb` contains linear regression (ordinary least squares) model training and testing.
  - `Ridge Regression.ipynb` contains ridge regression model training and testing.
  - `Lasso Regression.ipynb` contains lasso regression model training and testing.  
  - `Elastic Net Regression.ipynb` contains elastic net regression model training and testing.
    





Contributors: Mikaela Lim, Gianni Spiga, Sharon Vien, Kevin Xu
