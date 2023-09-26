https://huggingface.co/spaces/Justin-J/Using-the-Streamlit-application-and-machine-learning-project-forecast-and-analyze-customer-Churn

# Using the Streamlit application and machine learning project, forecast and analyze customer Churn. 

[![View My Profile](https://img.shields.io/badge/View-My_Profile-green?logo=GitHub)](https://github.com/justinjabo250)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5?logo=linkedin&logoColor=orange)](https://www.linkedin.com/in/jabo-justin-2815341a2/) 
[![View Repositories](https://img.shields.io/badge/View-My_Repositories-blue?logo=GitHub)](https://github.com/justinjabo250?tab=repositories)
[![View My Profile](https://img.shields.io/badge/MEDIUM-Article-purple?logo=Medium)](https://medium.com/@jabojustin250)
[![My App](https://img.shields.io/badge/My-Website-darkgreen)](https://huggingface.co/spaces/Justin-J/Using-the-Streamlit-application-and-machine-learning-project-forecast-and-analyze-customer-Churn)


<p align="center">
  <img src="images/welcome.jpg" alt="ExpressorLogo" width="800">
</p>

## Project Overview

In this project, our goal is to identify the likelihood that a customer will quit the company, the key churn indicators, and potential retention strategies. Churn is one of the major problems affecting the telecom industry. Studies show that the top 4 wireless service providers in the US experience a 1.9% to 2% monthly average churn rate.

Customer turnover is one of a business's major costs. Customer churn, sometimes referred to as customer attrition or customer turnover, is the proportion of customers who stopped using your company's product or service within a defined time frame. If you began the year with 500 clients and ended it with 480, for instance, then 4% of those 500 clients left. If we could reasonably predict when a client quits and why they depart, it would be very helpful to the business in planning its retention campaigns.


<p align="center">
  <img src="images/logo.jpg" alt="ExpressorLogo" width="800">
</p>


This solution would assist this telecom company in providing better customer service by identifying those clients who may be considering leaving.

## The presentation follows the following outline

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
- [Data](#data)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Deployment](#deployment)


## Objectives

- Objective 1: Data Exploration
- Objective 2: Data Preprocessing
- Objective 3: Model Selection and Training
- Objective 4: Model Evaluation
- Objective 5: Results & Analysis
- Objective 6: Deployment and Future Improvements


## Summary
| Code | Name                                                | Summary of the work                                                                                          |                                                                                              Streamlit App    |                                                                                                |
|------|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Capstone  | Expressor Customer Churn Prediction, ML Approach     | [Summary_PPT]() |  [Streamlit App](https://huggingface.co/spaces/Justin-J/Using-the-Streamlit-application-and-machine-learning-project-forecast-and-analyze-customer-Churn)      |



## Project Setup

To set up the project environment, follow these steps:

1. Clone the repository:

git clone my_github 

```bash 
https://github.com/justinjabo250/Using-the-Streamlit-application-and-machine-learning-project-forecast-and-analyze-customer-Churn
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Create a virtual environment:

- **Windows:**
  ```bash
  python -m venv venv
  venv\Scripts\activate
  ```

You can copy each command above and run them in your terminal to easily set up the project environment.


## Data

The data set used in this project was sourced from the [Zindi](https://zindi.africa/competitions/customer-churn-prediction-challenge-for-azubian).

## Data set Description

| Column Name     | Type   | Description                                                              |
|-----------------|-----------------|--------------------------------------------------------------------------|
| REGION          | Categorical     | The location of each client                                               |
| TENURE          | Numeric         | Duration with the network                                                 |
| MONTANT         | Numeric         | Top-Up Amount                                                             |
| FREQUENCE_RECH  | Numeric         | The number of times a customer refilled                                    |
| REVENUE         | Numeric         | Monthly income of each client                                             |
| ARPU_SEGMENT    | Numeric         | Income over 90 days divided by 3                                          |
| FREQUENCE       | Numeric         | Number of times the client has made an income                              |
| DATA_VOLUME     | Numeric         | Number of connections                                                     |
| ON_NET          | Numeric         | Inter Expresso call                                                       |
| ORANGE          | Numeric         | Calls to Orange                                                           |
| TIGO            | Numeric         | Calls to Tigo                                                             |
| ZONE1           | Numeric         | Calls to Zone1                                                            |
| ZONE2           | Numeric         | Calls to Zone2                                                            |
| MRG             | Categorical     | A client who is going                                                      |
| REGULARITY      | Numeric         | Number of times the client is active for 90 days                           |
| TOP_PACK        | Categorical     | The most active packs                                                     |
| FREQ_TOP_PACK   | Numeric         | Number of times the client has activated the top pack packages             |
| CHURN           | Binary          | Target variable to predict - Churn (Positive: customer will churn, Negative: customer will not churn) |


## Exploratory Data Analysis

During the exploratory data analysis (EDA) phase, a comprehensive investigation of the churn dataset was conducted to gain insights through various types of analyses.

- **Univariate analysis:** A thorough examination of each variable individually was performed. Summary statistics such as mean, median, standard deviation, and quartiles were calculated to understand the central tendency and spread of the data.

<p align="center">
  <img src="images/Univariate.png" alt="Univariate" width="600">
</p>

- **Bivariate analysis:** Relationships between pairs of variables were explored to identify patterns and potential predictor variables for sepsis classification.

<p align="center">
  <img src="images/Bivariate.png" alt="Bivariate" width="600">
</p>

- **Multivariate analysis:** Relationships among multiple variables were examined simultaneously, allowing for a deeper understanding of their interactions and impact on sepsis.

<p align="center">
  <img src="images/multivariate.png" alt="multivariate" width="600">
</p>

### Hypotheses:
1. Customers with longer tenure are less likely to churn than those with short tenure.

2. Customers with lesser income are likely to churn than those who have higher

These hypotheses, along with the results of the EDA, contribute to a deeper understanding of the dataset and provide valuable insights for further analysis and model development.

### Business Questions
1. What is the relation of the preditor class (Churn) to other variable
- Churn rate
- Churn vrs. Tenure
2. What type of services offered by the telecom industry (Expressor)

3. What is the average tenure of customers?

## Modeling

The unbalanced nature of the data was considered when evaluating models throughout the modeling phase. The AUC score would be the ideal performance evaluation estimator since it offers a fair evaluation for unbalanced datasets.


Area Under the Curve (AUC) was used to assess the performance of the six models that weren't selected.

- **Logistic Regression** 
- **Decision Tree** 
- **Random Forest** 
- **GaussianNB**
- **ComplementNB**
- **Support Vector Machine (SVM)**

These models were evaluated based on their AUC and logloss scores, providing insights into their performance on the imbalanced dataset. 


We used the AUC metric to evaluate the models' performance because our dataset was unbalanced.

- AUC values for the top-performing model, the logistic regression model, reached 80%.

- ComplementNB consistently displayed strong performance in various circumstances.

- When compared to other models, GaussianNB had a higher log loss and a considerably lower AUC score.


### Streamlit deployment 

Navigate to the cloned repository and run the command:

```bash 
pip install -r requirements.txt
``` 
To run the demo app (being at the repository root), use the following command:
```bash 
streamlit run streamlitApp.py
```

### App Execution on Huggingface

Here's a step-by-step process on how to use the [Streamlit App](https://huggingface.co/spaces/Justin-J/Using-the-Streamlit-application-and-machine-learning-project-forecast-and-analyze-customer-Churn) on Huggingface:



## Contribution
You contribution, critism etc are welcome. We are willing to colaborate with any data analyst/scientist to improve this project. Thank your 

## Contact

`Justin Jabo` 

`Data Analyst`
`Azubi Africa`

- [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5?logo=linkedin&logoColor=orange)](https://www.linkedin.com/in/jabo-justin-2815341a2/) 
