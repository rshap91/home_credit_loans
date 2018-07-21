# Credit Default Notes

# EDA & Cleaning

_From https://www.kaggle.com/willkoehrsen/start-here-a-gentle-introduction/notebook
Saved in Python_Programs/Machine_Learning_


  - Examine Distribution of Target (check for imbalanced classes)
  - Examine Column Types
    - Check and Separate dtypes (dates, objects, numbers)
  - Remove/Impute Anomalies
    - You can also create a categorical value (0,1) for whether or not the data was anomalous.
    - Only for numeric vars yea?
  - Fill Missing Variables
    - strings have wierd NAs
    - Fill with Interpolations? Median? Mean? See notebook.
  - Label Encode binary features and OHE multiple categorical ftrs
    - _Make sure to drop categories that are not in the test set!_
    - check out df.align?

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

# Anomalies:

Just need a note on this as it seems to be the least straight forward and
most manual portion of cleaning.



## Application

NOTE REG = Registered
