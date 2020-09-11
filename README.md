# Loan Eligibility Test

### Problem statement:
A home loan provider keeps records of their clients and want to automate the process of testing eligibility for future loan, i.e. should a client be given new or more loan based on the previous data?. It can help the company to target those clients and nurture them for more Business.

### Type of Data-mining task:
Our data-set is already labeled (Loan_status: “Yes / No”) and we have to build a (ML) model to classify the labels based on the given determining factors (fields). it is a Classification task under Supervised learning approach in Data Mining.

### Dataset and brief overview:
We have one labeled data-set **Labeled_Data.csv** with the following fields to train and test our model. **Loan_Status** is our target class to be classified by our model.

| Fields            | Descriptions                                 |
| -------------     | ---------------------------------            |
| Loan_ID           | Unique Loan ID                               |
| Unique Loan ID    | Male/ Female                                 |
| Married           | Applicant married (Y/N)                      |
| Dependents        | Number of dependents                         |
| Education         | Applicant Education (Graduate/Under Graduate |
| Self_Employed     | Self employed (Y/N)                          |
| ApplicantIncome   | Applicant income                             |
| CoapplicantIncome | Co-applicant income                          |
| LoanAmount        | Loan amount in thousands                     |
| Loan_Amount_Term  | Term of loan in months                       |
| Credit_History    | Credit history: meet guidelines              |
| Property_Area     | Urban / Semi Urban / Rural                   |
| Loan_Status       | Loan approved (Y/N)                          |


To deploy and test our model in real world, we have another data-set which is unlabeled **Unlabeled_Data.csv**. We need to submit the model predictions as **submission.csv** either to [Kaggle](https://www.kaggle.com/competitions) or [Analytics Vidhya](https://datahack.analyticsvidhya.com/contest/practice-problem-loan-prediction-iii/) to know the actual performance score of our model on this data-set.

### Domain knowledge:
From our financial background we know that Loan is the main selling product of a Loan provider or a Bank and often considered as low risk or secure investment which yields also low Return (ROI). Banks tend to care more about a client’s credit history, present wealth and income as well as the loan amount, he/she applied for. Client’s age can also be an important factor. A human being (Bank manager) can easily make decision based on these information but we need to automate the process by making the computer to understand and learn patterns so that it can correctly identify future cases.

### Hypothesis:
A client will get loan If he/she:
1. has good credit history. (Trustworthy)
1. has good income (Capability to pay back)
1. has valuable property like in the Urban and semi-urban areas. (Back up) i.e. if the client becomes insolvent then the bank can recover the loan amount by selling those Assets.


### Methodology:
We will use routine procedures of Data-Mining. Since in this case, Data set is readily available online from various sources in easily readable format like CSV, we will skip the Data collection steps.

Hence, we will initially go through the following steps:
1. Reading and Exploring Data to check
    1. variable (field) data types
    2. duplicates
    3. missing values
    4. outliers
    5. correlation
    6. balance in target class
2. Selecting classification algorithm based on type of analysis (here bi-variate analysis or binary classification). We will use Decision Tree / Naive Bayes in the initial stage for simplicity.
3. Data pre-processing: We will go through standard pre-processing for the base model which are (Note: Different algorithms require different pre-processing which we will do in advanced pre-processing):
    1. Removing the duplicates
    2. Dealing the missing values (removing or filling)
    3. Dropping fields based on domain knowledge
    4. Dealing outliers (log transformation)
    5. Data type conversion (to numeric)
    6. Dropping fields (as required)
    7. Saving and creating data-sets for analysis
4. Model building, training and testing with Accuracy as performance measurement criteria. There are many measurement criteria available, for now we are keeping this project simple.
5. Improvements:
    1. Cross-validation: 10 Fold
    2. Parameter optimization: GridsearchCV
    3. Advanced pre-processing
        1. Dealing with categorical variables (1 hot encoding)
        2. Scaling values (Standard scaling)
        3. Feature engineering (Creating new features)
        4. Dimensionality reduction (based on PCA)
6. Further improvement options (Optional): Ensemble learning methods -
    1. Bootstrap aggregating (bagging): Random Forest
    2. Boosting: CatBoost / XGBoost / LightGBM
    3. Stacking

### Performance evaluation:
    Accuracy

### Requirements:
    Python 3.8, (Jupyter Notebook), pandas-1.1.1, numpy-1.19.1, scipy-1.5.2, scikit-learn-0.23.2, matplotlib-3.3.1, seaborn-0.10.1

### Resources that were helpful:
Thanks to **DataCamp** [1](https://www.datacamp.com/community/tutorials/decision-tree-classification-python), [2](https://www.datacamp.com/community/tutorials/naive-bayes-scikit-learn) and **Analytics Vidhya** [3](https://www.analyticsvidhya.com/blog/2016/01/complete-tutorial-learn-data-science-python-scratch-2/).