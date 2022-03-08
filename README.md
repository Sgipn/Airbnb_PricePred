# Airbnb Price Prediction
------------------------------------------
Current Progress:
* Preprocessing: 
   1) Removed listings with invalid names, 
   2) Removed 'id', and 'host_name' columns for ethical considerations, 
   3) Removed observations with NaN values in last_review (date value) since listings with no reviews will have no last_review.

* EDA: [In Progress]
   1) Created a Correlogram of the 14 remaining variables. Identified number of reviews and reviews per month to be highly correlated. No other pair of variables was highly correlated with high correlation defined at $`|r_ij| \ge 0.5`$. Shown in preprocessing&eda.ipynb
   2) Created a Word cloud from listing names. Shown in preprocessing&eda.ipynb

* Modelling Procedure: [In Progress]
  1) Linear Regression (OLS)
  2) Ridge Regression
  3) Lasso
      - Plot of Beta paths: $`\beta_{j}, j = 1,...,232`$.
      - 10-fold cross validation for $`\lambda`$ tuning. MAE of each of 4000 models was calculated. (10 models per lambda, 400 lamdba values) 
      - Lowest MAE found at $`\lambda \approx 4`$.
      - Prediction Accuracy [In Progress]
      - Testing on Simulated data [In Progress]
  5) ... 

* Evaluation: (accuracy and time complexity
  - Metric: MSE and/or MAE, run time, generalizability/interpretatbility.
  - Lasso Final Model:
      - $$y = 17.21323117 X_{availability_365} + 2.6954145 X_{neighbourhood_group_Brooklyn} + 27.00013305 X_{neighbourhood_group_Manhattan} + 68.55946047 X_{room_type_Entire home/apt} + 14.12280336 X_{room_type_Private room} + \epsilon$$ with $\epsilon$: noise term, and $\lambda = 16.75252472408214$ tuned from minimium MAE .
      - MSE = [running]
      - MAE = [running]
      - R^2 = [running]
      - Adjusted R^2 = 
      - Interpretation: Since all variables were standardized before any training/tuning, we see that the most important variables for predicting airbnb rental price contains the above five variables. Moreover, the type of rental property (room_type_Entire home/apt) is the most important variable that determines price. This makes intuitive sense- rental price of a house will probably be more expensive that renting a room. Additionally, the neighborhood group: Manhattan is the second most important predictor variable. This also makes intuitive sense- perhaps people who are visiting NYC will more likely rent a property if it is close to well-known tourist hotspots/shopping areas such as in Manhattan. This can be supported by our WordCloud from our EDA where 'Manhattan' is a buzzword among listing descriptions-- perhaps property owners recognize that Manhattan is a buzzword that can increase likelihood of rental.    
      - h<sub>&theta;</sub>(x) = &theta;<sub>o</sub> x + &theta;<sub>1</sub>x

------------------------------------------

Navigating this project:
* `./data`: contains 2 .csv files containing raw and preprocessed AirBnB data originally sourced from kaggle.com.
  - `AB_NYC_2019.csv`: contains raw airbnb dataset from kaggle.
  - `listings.csv`: contains preprocessed data with 38837 rows × 232 columns.
* `./notebooks`: contains jupyter notebooks of our preprocessing, EDA, modelling, and testing. 
  - `preprocessing&eda.ipynb` contains preprocessing and eda.
  - `OLS.ipynb` contains linear regression (ordinary least squares) model training and testing.
  - `Ridge Regression.ipynb` contains ridge regression model training and testing.
  - `Lasso Regression.ipynb` contains lasso regression model training and testing.  
  - `Elastic Net Regression.ipynb` contains elastic net regression model training and testing.
    





Contributors: Mikaela Lim, Gianni Spiga, Sharon Vien, Kevin Xu
