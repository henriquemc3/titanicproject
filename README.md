# titanicproject Model card 
https://colab.research.google.com/drive/1cNfRREN_TCsaaEVEvRhK3kRbuk8rcb14?usp=sharing 

## Basic information 
Group Members:
Hana, hana.aglan@gwu.edu
Frank, frank_guo@gwu.edu
James, joconnell10@gwu.edu
Henrique, henriquecassol@gwu.edu

**Model date:** October 2024

**Model version:**
- **Python version:** 3.10.12
- **Sklearn version:** 1.5.2
- **Model license:** MIT
- **Model Version:** 1.0
- **Model Implementation Code:** [DNSC3288_titanic project](./DNSC3288_titanic_project.ipynb)

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
- Columns used as inputs in the final model: PassengerId, Survived, Pclass, Sex, Age, Fare, FamilySize, IsAlone, Embarked_Q, Embarked_S

- Column(s) used as target(s) in the final model: Survived

- Type of model: Random forest 
- Software used to implement the model: sklearn
- Version of the modeling software: 1.5.2

- Hyperparameters or other settings of your model:
n_estimators=100, random_state=42


## Quantitative analysis 

| Train AUC | Validation AUC |
|-----------|----------------|
| 1.0000    | 0.9000         |

| Train Accuracy | Validation Accuracy | Test Accuracy |
|-----------|----------------|----------|
| 1.0000    | 0.8435         | 0.7751*   |

- Accuracy: 0.84
- Precision: 0.84
- Recall (True Positive Rate, TPR): 0.77
- F1 Score: 0.80

![Screenshot 2024-12-06 154001](https://github.com/user-attachments/assets/a01a5cf2-fd5c-4543-8d89-180f75bc56f7)
### Correlation heatmap
![Screenshot 2024-12-06 150509](https://github.com/user-attachments/assets/f2a39ba4-3c89-49b9-9283-6c7030b0a124)

## Ethical Consideration

### Potential Negative Impacts of Using Your Model:

#### Math or Software Problems
- The random forest model is a "black box" model, which means it does not show the intermediate deduction procedures like a decision tree model. This leads to poor explainability and no way to appeal.
- The model risks overfitting, as evidenced by 100% training accuracy, meaning it may fail to generalize to unseen data effectively.

#### Real-World Risks: Who, What, When, or How
- **Who**: The primary users are students and machine learning beginners on Kaggle, and the model may influence their understanding of real-world applicability.
- **What**: The model reproduces historical biases, such as favoring women and first-class passengers, perpetuating systemic inequalities.
- **When**: Misuse occurs when the model is applied to predict outcomes in unrelated or future scenarios (e.g., modern disasters), leading to potentially inaccurate and harmful predictions.
- **How**: The model’s replication of historical data patterns perpetuates inequalities, such as gender bias (favoring women) and socioeconomic bias (favoring first-class passengers). This could validate past injustices instead of challenging or neutralizing them.

---

### Describe Potential Uncertainties Relating to the Impacts of Using Your Model:

#### Math or Software Problems
- The "black box" nature of random forest models creates uncertainty in interpreting predictions, as the lack of transparency limits understanding and accountability.
- Overfitting introduces doubts about the reliability of predictions on new, unseen data.

#### Real-World Risks: Who, What, When, or How
- **Who**: There is uncertainty about how different user groups (e.g., non-experts or those unfamiliar with the dataset’s limitations) interpret and use the model’s predictions.
- **What**: Replicating historical biases could lead to unintended consequences, such as reinforcing past injustices.
- **When**: Applying the model in contexts beyond its intended purpose (e.g., disaster prediction) introduces risks of inappropriate and unreliable predictions.


### Describe any unexpected or results
1. When we tried to reduce overfitting by changing model hyperparameter, such as max depth and number of trees, our validation accuracy, recall, and precision all went down. 

2. Even though logically we should have removed passenger ID from the training dataset, when we removed it, validation and test results went down a well.
With Passenger_Id:
Training Accuracy: 100
Validation Accuracy: 84.35
![Screenshot 2024-12-06 143816](https://github.com/user-attachments/assets/4f7c91d9-e7bb-4fa0-b9d2-38a6c9973f8d)
![Screenshot 2024-12-06 145617](https://github.com/user-attachments/assets/102ca6f6-3119-4b35-ace9-1582c5028277)

Without Passenger_Id:
Training Accuracy: 97.89
Validation Accuracy:83.79
![Screenshot 2024-12-06 143528](https://github.com/user-attachments/assets/a459edbe-437a-4950-a9c8-e79f6c20c551)
![Screenshot 2024-12-06 143507](https://github.com/user-attachments/assets/dd1058b9-4b29-4bce-bba1-524b47fd303e)

