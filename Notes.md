# Credit Default Notes

# EDA & Cleaning

_From https://www.kaggle.com/willkoehrsen/start-here-a-gentle-introduction/notebook
Saved in Python_Programs/Machine_Learning_


  - Examine Distribution of Target (check for imbalanced classes)
  - Examine Column Types
    - Check and Separate dtypes (dates, objects, numbers)
    - KEEP TRACK OF THESE DTYPE MAPPINGS/DISTRIBUTION
  - Remove/Impute Anomalies
    - You can also create a categorical value (0,1) for whether or not the data was anomalous.
    - Only for numeric vars yea?
  - Fill Missing Variables
    - strings have weird NAs
    - Fill with Interpolations? Median? Mean? See notebook.
  - Label Encode binary features and OHE multiple categorical ftrs
    - _Make sure to drop categories that are not in the test set!_
    - check out df.align?
  - Aggregate to Training Dataset Level (Application)
  - Merge All Datasets
  - Align columns to the TEST dataset
  - Fill/Drop Nas (Created by merge)


__NOTE__: Do 1 dataset at a time to save processing time and memory.


# Model Prep
  - Look for correlations
  - Feature Engineering
  - Feature Selection
  - Inbalanced Classes:
    - Can I sequentially train on proportioned samples?
    - Undersample/Oversample Majority?


__NOTE__: Make sure that you perform all transformations you made on the training data
        on the testing data as well!



# Modeling

Gonna do a few things:

Feature selection
  - loan_preds_kaggle.ipynb
    * I've run this once and it didn't help the model.
      Will run again after feature engineering,
      but will probably need to do some sort of search over number of features
      to use based on cross_validation... tough/intensive

Build And Tune Models
  - NavieBayes
    o fit independent nb algos and make gausian that predicts based on probabilities (or just avg them)
  - Trees
    o Param tune and fit ET, RF, GB, LightGBM, XGB
    o Param tune with BayesianOptimization
    o See Machine_Learning folder

Sampling
  - Over and Under Sample Classes in training
  - Look at online training

Feature Engineering
  - Cluster for new features
  - PCA/SVD/NMF


__NOTE__ For Each Model, save/submit the _parameters_ in the note section!
