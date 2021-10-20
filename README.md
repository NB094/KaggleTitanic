# KaggleTitanic

## Introduction

The `Titanic.ipynb` notebook aims to predict the survivors from the Titanic shipwreck based on the [Kaggle dataset.](https://www.kaggle.com/c/titanic/overview) PyCaret is a package for Python that tests many different machine learning models at the same time and returns a list of those with the highest accuracy; we'll be using this for the analysis herein.

The procedure of analysis is as follows:
1. Exploratory Data Analysis & Hypothesizing
2. Data Cleaning
3. Shortlist Best ML Models with PyCaret
4. Verify PyCaret Results with Manual Implementation

The training dataset contains the following features:
* PassengerId – a unique ID number for the passenger.
* Survived – whether or not that passenger survived (0 = No, 1 = Yes)
* Pclass – ticket class (1st, 2nd, or 3rd class)
* Name – name of the passenger
* Sex – sex of the passenger
* Age – age of the passenger, in years
* SibSp – # of siblings / spouses aboard the Titanic
* Parch – # of parents / children aboard the Titanic
* Ticket – ticket number of the passenger
* Fare – fare paid by the passenger
* Cabin – passenger's cabin number
* Embarked – port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

## Usage
Install the `requirements.txt` in a new environment within the terminal, and open the `Titanic.ipynb` in Jupyter Lab or Jupyter Notebook.

## Results
The notebook currently tests two different machine learning models: LightGBM and RandomForest, which were selected from a list of models that PyCaret highlighted. PyCaret estimated these models' accuracy as 0.8265 and 0.7878 respectively. When submitted on Kaggle, the LightGBM model achieves a score of 0.73684 and the RandomForest model achieves a score of 0.76794. In other words, the RandomForest model can accurately predict whether or not a passenger survived the Titanic accident 77% of the time (although the scores are slightly lower than what PyCaret had estimated).

## Further Development
Here are some ideas I have for improving the scores:
* Try predicting results directly using PyCaret and submitting to Kaggle to see their difference in score compared to the manual method.
* Perform feature engineering to give the models more data to work with
* Tuning additional parameters via grid searching
* Test different models such as XGBoost to compare their results to LightGBM and RandomForest.
