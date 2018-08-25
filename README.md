# home_credit_loans

Kaggle Competition For Predicting Loan Default.

### Summary

This competition provided data on client applications for home loans and supplementary
data such as clients past loans, credit history, credit card activity, and some
demographic information such as information on where the applicants are from or
currently live.

### Results

After trying different algorithms I landed on using LightGBM as my main model.
I chose LGBM because it's scores were approximately the same as XGBoost, but it
took a fraction of the time to train. My final AUC score for the competition was
0.77 both cross-validated and on submissions. While this wasn't very high on the
leader-boards (top score is 0.81), I was consistently able to improve my score on
each submission.

The default (untuned, all features) score for LGBM was 0.72. Through parameter tuning
I was able to boost that score iteratively up to 0.77.

I also tried some feature engineering and feature selection to help the model generalize
better. However these did not seem to add much value to the model. Though i'm not
positive of the implementation, I believe LGBM is good at handling both imbalanced
classes and overfitting (through parameter tuning), so feature selection was
not necessary for improving the score.

I was however able to combine my engineered features and run through feature selection
to build a model of equivalent score with only 300 variables as apposed to all 500+.


### Files

The data files presented are

  - Applications: main data file containing current application information as
    well as some supplementary features.
  - Bureau and BureauBalances: Information on applicants credit history
  - Previous Applications: Previous credit applications.
  - Credit card balance: Monthly Credit Card balances for applicants
  - POS Cash Balances: Balances for previous POS and cash loans for applicants
  - Installments Payments: Payment history for previous credit loans

There are 8 ipynbs in this repo. 5 cleaning notebooks and 3 used for modeling.

The cleaning notebooks are:

1. Application.ipynb
  - Clean the training and test application data

2. Bureau_Balances.ipynb
  - Clean and combine the Bureau and BureauBalances data

3. Credit_Card.ipynb
  - Clean the Credit Card, POS Cash Balances, and Installment/payments data

4. Previous_Applications.ipynb
  - Clean the Previous_Applications data

The modeling notebooks are

1. Feature_Engineering.ipynb
  - Use matrix factorization, k-means clustering, and naive bayes classifier
  to generate new features.

2. Feature_Selection.ipynb
  - Use correlation analysis, Chi-Squared test, Recursive Feature Elimination
  and L1 Regularization to determine most important, predictive features.

3. Build_Models.ipynb
  - Explore different ML algorithms, build and tune models.
