# Data Science Portfolio

## Welcome to my data science portfolio!

[![author](https://img.shields.io/badge/author-pedroalmeida-red.svg)](https://www.linkedin.com/in/pedro-almeida-ds/)

<p align="center">
  <img src="https://github.com/allmeidaapedro/Portfolio-Ciencia-de-Dados/blob/main/images/Black%20Modern%20Personal%20LinkedIn%20Banner.png">
</p>

Hello! My name is Pedro Almeida, and I am a 20-year-old student pursuing a Bachelor's degree in Computer Engineering at the University of Brasília. Currently, I work as a Data Science Intern at Mundiale. In this role, I assist in the analysis and interpretation of data sets, extracting valuable insights. I collaborate with multidisciplinary teams to identify and implement improvements in data processes. I contribute to the development of Natural Language Processing (NLP) models for textual data analysis, as well as other models for purchase propensity and sales forecasting, for example. I provide support to the team in the critical analysis of results obtained by Machine Learning models, influencing data-driven decisions. I conduct A/B tests to validate hypotheses and optimize the performance of predictive models and actively participate in creating data visualizations and detailed reports. My passion lies in machine learning, data science, statistics, and mathematics, and I am constantly working on projects in these areas. Explore them below!

## Projects

### EXPLORATORY DATA ANALYSIS, CLASSIFICATION, AND REGRESSION

#### [Analysis and modeling of ENEM 2022 microdata](https://github.com/allmeidaapedro/Enem-Modeling)

- **Description:** This is an end-to-end data science project (from data collection to deployment), in which data cleaning, exploratory analysis, and modeling of ENEM 2022 microdata (real public data) are performed.
- **Problem and objectives:** The objective is to perform an analysis and modeling of performance and abstention in the exam. The performance analysis and modeling aim to identify the relationship of variables with the student's score and build a model to predict this score and understand the impact of the variables on it. The abstention analysis and modeling aim to identify the relationship of variables with the student's abstention and build a model to predict the probability of a student abstaining from the exam, as well as to interpret its results in the same way. For this, the LightGBM algorithm was used, given its predictive power, fast training, and prediction.
- **Results:** Interesting relationships were noticed through exploratory data analysis and SHAP value analysis, such as, the higher the mother's education level of the candidate, the higher the performance and the lower the abstention rate. The models had satisfactory performances. With an MAE = 55.7, on average, the model's predictions deviate from the students' actual scores by 55.7 points. With an ROC-AUC = 0.69, there is a discriminatory power in distinguishing students who were present and students who were absent. Two Flask APIs were developed for deploying the models for both analyses mentioned above. Thus, it is possible to predict the score or the probability of abstention of a candidate by providing socio-economic and educational data about them.

### CLASSIFICATION AND REGRESSION

#### [Credit Risk Modeling (PD, EAD, LGD, EL) - Lending Club](https://github.com/allmeidaapedro/Lending-Club-Credit-Scoring)

- **Description:** In this project, I perform credit risk modeling, including Probability of Default (PD), Exposure at Default (EAD), Loss Given Default (LGD), and Expected Loss (EL) models, using data from loans from 2007 to 2014 from the American institution Lending Club.
- **Business problem:** Lending Club faces a significant challenge in managing loss risks while optimizing profits for its investors. The platform hopes to estimate risks accurately to maintain a sustainable and profitable business. So, the CEO wants insights into credit risk in the company's concessions and models of PD, EAD, and LGD to estimate the expected loss (EL) on each loan. This, along with credit scores, will be used to develop possible credit policies in the company. Moreover, being an online platform, it is important to explain to customers why the decision to approve or deny a loan. So, the results of these models should be explainable and interpretable.
- **Objectives:** Develop PD, EAD, and LGD models to compute the expected loss on each loan, EL. From this, develop a credit policy considering the estimated losses and the annualized ROI of each asset. Then, monitor the model, accessing indicators of population stability, assessing the need for a new model one year after it is built.
- **Results:** The PD model had good discriminatory ability, with AUC = 0.7 and KS = 0.3, as well as ordering in scores, concentrating more than 50% of bad customers up to the third score range. The LGD and EAD models had satisfactory predictive power. The credit policy was developed and reduced both expected losses and the default rate. The model was monitored, and the need for a new one was soon assessed, as the scores showed a PSI of 0.19.

#### [Credit Card Churn Prediction](https://github.com/allmeidaapedro/Churn-Prediction-Credit-Card)

- **Description:** This is an end-to-end machine learning project (from data collection to deployment) that uses LightGBM to predict the probability of a customer canceling the credit card service of a bank.
- **Business problem:** The bank manager is tired of seeing more and more customers stop using their credit card product. He needs us to identify the probability of canceling the service for each customer, in order to rank them by cancellation chance and take possible actions from there, such as offering promotions. Identifying potential customers prone to cancellation helps plan retention strategies, maintaining healthy revenue. Acquiring a new customer is more expensive than retaining an existing one.
- **Objectives:** Identify factors associated with customer churn; build a model capable of accurately predicting the probability of canceling the service for a customer; offer action plans for the bank to reduce credit card churn.
- **Results:** It was possible to achieve an estimated gain of $171,477, calculating the difference between the gain of true positives, the retention cost of false positives, and the cost of false negatives that cancel. Additionally, the model exhibits incredible performance, given the quality of the data and the modeling carried out.

### REGRESSION AND TIME SERIES

#### [Store Item Demand Forecasting](https://github.com/allmeidaapedro/Store-Item-Demand-Forecasting)

- **Description:** In this project, I performed time series forecasting using LightGBM to predict the number of sales of 50 items in 10 different stores over a period of 3 months.
- **Business problem:** A retail store manager wishes to plan a strategy to manage stock and investments in 10 stores for 50 products, aiming to effectively meet customer demand. By employing predictive analysis, they seek to improve sales forecasts, maintain product availability, and boost overall store performance.
- **Objectives:** Identify business insights on sales over time, such as seasonal patterns and trends; build a model capable of accurately predicting sales in the next 3 months; Estimate financial outcomes considering these forecasts.
- **Results:** The financial outcome per store, per store
