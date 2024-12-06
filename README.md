# titanicproject Model card 

## Basic information 
Group Members:
Hana, hana.aglan@gwu.edu
Frank, frank_guo@gwu.edu
James, joconnell10@gwu.edu
Henrique, henriquecassol@gwu.edu

**Model date:** October 2024

** Model version:
- **python version:** 3.10.12
- **Sklearn version:** 1.5.2
- **Model license:** Apache 2.0

**Primary intended uses:**

## Intended use:

- **Primary intended uses:** educational purpose

- **Primary intended users:** students 

- **Out-of-scope use cases:** everything is not educational purpose 

## Training data 
- Source of test data: Kaggle titanic competition
- Training data 68% of total data & Validation date is 32% of the total data
- Number of rows in training/validation data: 1,309
- Data dictionary:

| **Name**     | **Modeling Role** | **Measurement Level** | **Description**                                             |
|--------------|-------------------|-----------------------|-------------------------------------------------------------|
| PassengerID  | ID                 | int                   | Unique row identifier                            | 
| survival     | Target             | int                   | Survival status (0 = No, 1 = Yes)                           |
| pclass       | input          | int                   | Passenger's ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)        |
| name         | input          | string                | Name of passenger       | 
| sex          | demographic information          | string                | Gender of the passenger                       |
| age          | demographic information          | float                  | Age in years                                  |
| sibsp        | input          | int                 | Number of siblings/spouses aboard the Titanic               |
| parch        | input          | int                   | Number of parents/children aboard the Titanic               |
| ticket       | input          | string                   | Ticket number                                               |
| fare         | input          | float                | Passenger fare                                              |
| cabin        | input          | string/float               | Cabin number                                                |
| embarked     | input          | string               | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |


## Test Data
- Source of test data: Kaggle titanic competition 
- Number of rows in test data: 418
- State any differences in columns between training and test data: The target variable has been removed as a variable

## Model details 
- Columns used as inputs in the final model


- Column(s) used as target(s) in the final model

- Type of model: Random forest 
- Software used to implement the model: GoogleCoLab
- Version of the modeling software

- Hyperparameters or other settings of your model





## Quantitative analysis 

### Correlation heatmap

## ethical consideration 

### Potential negative impacts of using your model:

#### Math or software problems
- The random forest model is a "Black box" model, which means that it doesn't show the intermediate deduction procedures like the decision tree model, which leads to poor explainability and no way to appeal.
- Overfitting Risk: The model has a training accuracy of 100%, which suggests overfitting, meaning the model may not adjust well to new, unseen data. This could result in inaccurate predictions in real-world situations. 
- Bias in Data Processing: The imputation of missing values (ex. Median for age) could potentially introduce biases that affect prediction accuracy as well as fairness

#### Real-world risks: who, what, when or how
- who: this model was created for the Kaggle competition and the code is only for educational purposes, the people who are being influenced are students and machine learning beginners.
- what: this model may enhance the bias and discrimination based on the Titanic data set, leading to discriminatory predictions.
- when: When individuals attempt to use this model to predict future disasters, it may lead to inaccurate results. Additionally, real-world risks may arise if this model is applied to contexts beyond its intended educational purpose.
- Unfair treatment of specific groups: By blindly replicating the patterns in the historical data, the model perpetuates the inequalities that existed at the time, such as gender bias (favoring women) and socioeconomic bias (favoring first-class passengers). This can lead to a situation where the model's predictions seem to validate or justify these past injustices, instead of challenging or neutralizing them.

### Describe potential uncertainties relating to the impacts of using your model:
- Math or software problems
#### Real-world risks: who, what, when or how?

- shouldn't use the result to predict any future disaster. 
### Describe any unexpected or results

