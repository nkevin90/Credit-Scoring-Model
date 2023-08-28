# Credit Scoring Project

## Overview

This project develops and evaluates a credit scoring model to predict whether a customer is likely to default on a credit application. The project involves preprocessing, exploratory data analysis (EDA), model training, evaluation, and interpretation of results. Additionally, it includes a FastAPI endpoint for real-time credit scoring predictions.

## Files

- `Case Study Sample.xls`: The dataset used for training and testing the models.
- `README.md`: This README file providing an overview of the project.
- `study.ipynb`: Jupyter notebook containing the project workflow, including preprocessing, EDA, model development, evaluation, and interpretation.
- `app/`: Directory containing FastAPI application files.

## Getting Started

To run this project locally, follow these steps:

1. Clone this repository to your local machine.
2. Install the required dependencies using: `pip install -r requirements.txt`.
3. Explore the `study.ipynb` notebook to understand the project flow and reproduce the analysis.
4. To use the FastAPI endpoint, navigate to the `app/` directory and follow the instructions in the corresponding README.

## Data

The dataset (`Case Study Sample.xls`) includes features related to credit applicants. Features include credit history, employment status, loan amount, age, and more. The target variable indicates whether the customer is a non-defaulter (Good credit [1]) or a defaulter (bad credit [0]).


| OBS#   | Variable Name      | Description                                  | Variable Type | Code Description                                              |
|--------|-------------------|----------------------------------------------|---------------|--------------------------------------------------------------|
| 1      | CHK_ACCT          | Checking account status                     | Categorical   | 0 : < 0 DM<br>1:  0 < ...< 200 DM<br>2 : => 200 DM<br>3:  no checking account |
| 2      | DURATION          | Duration of credit in months                | Numerical     |                                                              |
| 3      | HISTORY           | Credit history                               | Categorical   | 0: no credits taken<br>1: all credits at this bank paid back duly<br>2: existing credits paid back duly till now<br>3: delay in paying off in the past<br>4: critical account |
| 4      | NEW_CAR           | Purpose of credit                            | Binary        | car (new)   0: No, 1: Yes                                    |
| 5      | USED_CAR          | Purpose of credit                            | Binary        | car (used)    0: No, 1: Yes                                  |
| 6      | FURNITURE         | Purpose of credit                            | Binary        | furniture/equipment    0: No, 1: Yes                        |
| 7      | RADIO/TV          | Purpose of credit                            | Binary        | radio/television    0: No, 1: Yes                           |
| 8      | EDUCATION         | Purpose of credit                            | Binary        | education    0: No, 1: Yes                                  |
| 9     | RETRAINING        | Purpose of credit                            | Binary        | retraining    0: No, 1: Yes                                 |
| 10     | AMOUNT            | Credit amount                               | Numerical     |                                                              |
| 11     | SAV_ACCT          | Average balance in savings account          | Categorical   | 0 : <  100 DM<br>1 : 100<= ... <  500 DM<br>2 : 500<= ... < 1000 DM<br>3 : =>1000 DM<br>4 :   unknown/ no savings account |
| 12     | EMPLOYMENT        | Present employment since                    | Categorical   | 0 : unemployed<br>1:  < 1 year<br>2 : 1 <= ... < 4 years<br>3 : 4 <=... < 7 years<br>4 : >= 7 years |
| 13     | INSTALL_RATE      | Installment rate as % of disposable income | Numerical     |                                                              |
| 14     | MALE_DIV          | Applicant is male and divorced              | Binary        | 0: No, 1: Yes                                               |
| 15     | MALE_SINGLE       | Applicant is male and single                | Binary        | 0: No, 1: Yes                                               |
| 16     | MALE_MAR_WID      | Applicant is male and married or a widower  | Binary        | 0: No, 1: Yes                                               |
| 17     | CO-APPLICANT      | Application has a co-applicant              | Binary        | 0: No, 1: Yes                                               |
| 18     | GUARANTOR         | Applicant has a guarantor                   | Binary        | 0: No, 1: Yes                                               |
| 19     | PRESENT_RESIDENT  | Present resident since - years              | Categorical   | 0: <= 1 year<br>1<…<=2 years<br>2<…<=3 years<br>3:>4 years  |
| 20     | REAL_ESTATE       | Applicant owns real estate                  | Binary        | 0: No, 1: Yes                                               |
| 21     | PROP_UNKN_NONE    | Applicant owns no property (or unknown)    | Binary        | 0: No, 1: Yes                                               |
| 22     | AGE               | Age in years                                | Numerical     |                                                              |
| 23     | OTHER_INSTALL     | Applicant has other installment plan credit | Binary        | 0: No, 1: Yes                                               |
| 24     | RENT              | Applicant rents                             | Binary        | 0: No, 1: Yes                                               |
| 25     | OWN_RES           | Applicant owns residence                    | Binary        | 0: No, 1: Yes                                               |
| 26     | NUM_CREDITS       | Number of existing credits at this bank    | Numerical     |                                                              |
| 27     | JOB               | Nature of job                               | Categorical   | 0 : unemployed/ unskilled  - non-resident<br>1 : unskilled - resident<br>2 : skilled employee / official<br>3 : management/ self-employed/highly qualified employee/ officer |
| 28     | NUM_DEPENDENTS    | Number of people for whom liable to provide maintenance | Numerical |                                              |
| 29     | TELEPHONE         | Applicant has phone in his or her name     | Binary        | 0: No, 1: Yes                                               |
| 30     | FOREIGN           | Foreign worker                              | Binary        | 0: No, 1: Yes                                               |
| 31     | RESPONSE          | Credit rating is good                       | Binary        | 0: No, 1: Yes                                               |


## Preprocessing

Categorical and binary data encoding has been performed to prepare the data for model training and evaluation.

## Model Development and Evaluation

The `study.ipynb` notebook details the process of developing and evaluating machine learning models for credit scoring. It covers preprocessing, EDA, model training, performance evaluation, and interpretation.

## FastAPI Endpoint

The `app/` directory contains the FastAPI application that serves as an endpoint for credit scoring predictions. Users can input information, and the application will provide a prediction (non-defaulter or defaulter) and the calculated credit score.

## Usage

1. Explore the `study.ipynb` notebook for an in-depth analysis of the credit scoring project.
2. Follow the instructions in the `app/` directory to set up and run the FastAPI endpoint for real-time predictions.

## Contributing

Contributions to this project are welcome! Feel free to fork this repository, make improvements, and submit a pull request.
