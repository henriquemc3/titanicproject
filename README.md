# titanicproject Model card 
Group Members:
Hana, hana.aglan@gwu.edu
Frank, frank_guo@gwu.edu
James, joconnell10@gwu.edu

Model date: October 2024

Model version 2.0

Model license: Apache

Primary intended uses:

Primary intended users: students in GWU DNSC 3288 learning to model

Out-of-scope use cases: 

| **Name**     | **Modeling Role** | **Measurement Level** | **Description**                                             |
|--------------|-------------------|-----------------------|-------------------------------------------------------------|
| PassengerID  | ID                 | int                   |                            |
| survival     | Target             | int                   | Survival status (0 = No, 1 = Yes)                           |
| pclass       | Predictor          | int                   | Passenger's ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)        |
| name         | Predictor          | string                |        |
| sex          | demographic information          | string                | Gender of the passenger                       |
| Age          | demographic information          | float                  | Age in years                                  |
| sibsp        | Predictor          | int                 | Number of siblings/spouses aboard the Titanic               |
| parch        | Predictor          | int                   | Number of parents/children aboard the Titanic               |
| ticket       | Predictor          | string                   | Ticket number                                               |
| fare         | Predictor          | float                | Passenger fare                                              |
| cabin        | Predictor          | string/float               | Cabin number                                                |
| embarked     | Predictor          | string               | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |




## Test Data
- Source of test data: Kaggle titanic competition 
- Number of rows in test data: 1,308
- State any differences in columns between training and test data: None
