# titanicproject Model card 
Group Members:
Hana, hana.aglan@gwu.edu
Frank, frank_guo@gwu.edu
James, joconnell10@gwu.edu

Model date: October 2024


Model version 2.0

| **Name**     | **Modeling Role** | **Measurement Level** | **Description**                                             |
|--------------|-------------------|-----------------------|-------------------------------------------------------------|
| PassengerID  | ID                 | Nominal               | Survival status (0 = No, 1 = Yes)                           |
| survival     | Target             | Nominal               | Survival status (0 = No, 1 = Yes)                           |
| pclass       | Predictor          | Ordinal               | Passenger's ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)        |
| sex          | demographic information          | Nominal               | Gender of the passenger                       |
| Age          | Predictor          | Ratio                 | Age in years                                                |
| sibsp        | Predictor          | Ratio                 | Number of siblings/spouses aboard the Titanic               |
| parch        | Predictor          | Ratio                 | Number of parents/children aboard the Titanic               |
| ticket       | Predictor          | Nominal               | Ticket number                                               |
| fare         | Predictor          | Ratio                 | Passenger fare                                              |
| cabin        | Predictor          | Nominal               | Cabin number                                                |
| embarked     | Predictor          | Nominal               | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |




## Test Data
- Source of test data: Kaggle titanic competition 
- Number of rows in test data: 1,308
- State any differences in columns between training and test data: None
