ESILV - Python For Data Analysis - Project 2023 <br>
[ELMALEH Tom](https://www.linkedin.com/in/tom-elmaleh/) <br>
[KARUNATHASAN Nilany](https://www.linkedin.com/in/nilany-karunathasan-7b49691ba/) <br>
[SAMBATH Sïndoumady](https://www.linkedin.com/in/s%C3%AFndoumady-sambath-a7519a209/) <br>

<br>
<h1 align="center">Online Shoppers Purchasing Intention</h1>


### Introduction
This repository contains all files related to the final project of the course Python For Data Analysis. The project aims  to analyze a dataset, build a predictive model, and implement an API. Among the 3 datasets that were assigned to us, "Online Shopper Purchasing Intention dataset" is the one that we have chosen to study. 
 
### Purpose
The purpose of this project is to predict the purchasing intention of a visitor for a particular online store. 

### Dataset Description
The dataset consists of 10 numerical and 8 categorical attributes. The 'Revenue' attribute can be used as the class label. Of the 12,330 sessions in the dataset, 84.5% (10,422) were negative class samples that did not end with shopping, and the rest (1908) were positive class samples ending with shopping.
As we noticed that our dataset was imbalanced, we decided to use the SMOTE ( Synthetic Minority Over-sampling Technique) method in order to obtain a balanced dataset.

### Problem definition & Predictive modeling
This is a classification problem as the target variable is a discrete value (<code> True </code>  or  <code> False </code>) that indicates whether or not a user purchased an item of a particular online store.
Therefore we have used the following classification algorithms to determine the best model: 
        -  KNN <br>
        -  Naive Bayes Classifier <br>
        -  Decision Tree <br>
        -  Random Forest <br>
        -  XGBoost <br>
        -  SVC <br>
        -  Stochastic Gradient Descent <br>
        -  Gradient Boosting Score <br>

<br> For each model, we performed a Grid Search Cross Validation in order to find the best parameters. We used the metric <code> f1 </code>, as it combines the metrics' precision and recall. It's also known as a good metric to measure the performance of classification models and can be used for balanced datasets as well as unbalanced datasets. We then displayed the confusion matrix of each model in order to evaluate their performances. The overall performances of our models were good thanks to SMOTE method we used to rebalance our dataset. 
<br> In order to select the best model we ranked each model based on their scores on the test set and plotted the ROC curves.
The top three models that stood out of the crowd were respectively XGBoost, Random Forest, and Decision Tree.
Among these three, based on the score on the test set, the best classifier was XGBoost. Thus, it's the one that we used for our API.


### API Implementation
1. Download and extract the zip file related to our this repository.
2. Open the folder titled "API" on Visual Studio Code or another IDE of your choice.
3. Open a terminal and execute the "run.py" file by entering the following command :
```python
python run.py
```
4. The output will display the link on which the server is running (for me it was http://127.0.0.1:5000, it might be different for you)
5. Copy-paste the link on your browser.
6. Fill in the form with your input data and submit it by clicking on the  <code> Predict </code>  button.     
7. After submitting the form, scroll down as the result of the prediction should be displayed (ie if either the customer will or not purchase).








