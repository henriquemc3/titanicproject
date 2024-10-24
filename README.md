# titanicproject Model card 

## basic information 
Group Members:
Hana, hana.aglan@gwu.edu
Frank, frank_guo@gwu.edu
James, joconnell10@gwu.edu
Henrique, henriquecassol@gwu.edu

**Model date:** October 2024

**Model version:** 2.0

**Model license:** Apache 2.0

**Primary intended uses:**

## intended use 

**Primary intended users:** students in GWU DNSC 3288 learning to model

**Out-of-scope use cases:** 

## training data 
- data dictionary 

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
- Number of rows in test data: 1,308
- State any differences in columns between training and test data: None

## model details 



## quantative analysis 

### correlation heatmap

