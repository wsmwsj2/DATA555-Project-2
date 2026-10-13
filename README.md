# Breast Cancer Classification

This project uses the Breast Cancer Wisconsin (Diagnostic) Dataset. The goal is to predict whether a tumor is benign or malignant.

## Dataset

The dataset contains 569 rows. Column 0 contains ID numbers, column 1 contains the diagnosis, and the other columns contain tumor measurements. In column 1, benign tumors are changed to 0 and malignant tumors are changed to 1.

Dataset source: https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic

## Data Check and Exploration

The data has no missing values and no duplicate rows. The ID column is removed because it is not useful for prediction. Histograms, a bar chart, and box plots are used to examine the data. The plots show that malignant tumors usually have larger radius, perimeter, area, and concave point values.

## Models

The data is divided into 80% training data and 20% testing data. Logistic Regression is used as the baseline model. The notebook also compares SVM, KNN, Decision Tree, Random Forest, and Naive Bayes.

The baseline Logistic Regression model has an accuracy of 0.95 and an AUC of 0.95.

## Model Improvement

Columns 2, 3, 4, 5, and 9 are selected for the alternative Random Forest model. The Random Forest accuracy after feature selection is 0.94. GridSearchCV is used to test different values for `n_estimators` and `max_features`. The accuracy after tuning is 0.94, so the tuned model does not perform better than the baseline model.

## Files

`Assignment_7_Breast_Cancer_Classification.ipynb` contains the code, plots, results, and explanations.

`breast+cancer+wisconsin+diagnostic/wdbc.data` contains the dataset used by the notebook.

## How to Run

Open `Assignment_7_Breast_Cancer_Classification.ipynb` in Jupyter Notebook, Google Colab, or VS Code. Keep the dataset folder in the same folder as the notebook. Run all cells from the top.

The project uses pandas, matplotlib, seaborn, and scikit-learn.
