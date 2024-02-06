# Welcome to my data science portfolio!

[![author](https://img.shields.io/badge/author-pedroalmeida-red.svg)](https://www.linkedin.com/in/pedro-henrique-almeida-oliveira-77b44b237/)


<p align="center">
  <img src="images/welcome.jpg"%>
</p>

I'm Pedro Almeida from Brazil, a 20-year-old B.Sc. student majoring in Computer Engineering at the Federal University of Brasília. Currently, I'm working as a Data Scientist Intern at Mundiale. In this role, I assist in analyzing and interpreting datasets to extract valuable insights. I collaborate with multidisciplinary teams to identify and implement data process improvements. Additionally, I contribute to the development of Natural Language Processing (NLP) models for analyzing textual data, and other models for business cases such as propensity to buy and sales time series forecasting. My responsibilities extend to supporting the team in critically analyzing results from Machine Learning models, influencing data-driven decisions. I also execute A/B tests to validate hypotheses and optimize predictive model performance, actively participating in creating data visualizations and detailed reports. My enthusiasm lies in machine learning, data science, statistics, and mathematics, and I'm constantly working on projects in these areas. Explore them below!

## PROJECTS
 
 
## EXPLORATORY DATA ANALYSIS, CLASSIFICATION AND REGRESSION

### [**Enem analysis and modelling**](https://github.com/allmeidaapedro/Enem-Analysis)
- This is an end-to-end data science project (from data collection to deployment) where data cleaning, exploratory data analysis, and modeling are performed on microdata from the ENEM 2022 (real public data). ENEM (Exame Nacional do Ensino Médio) is a standardized national exam in Brazil used for university admissions and evaluation of high school education.
- Cleaning was crucial, given that the original microdata set was over 2 GB in size, making data manipulation, analysis, and modeling impractical. After completion, a parquet file was obtained, reducing the size of the original dataset from over 2 GB to approximately 221.7 MB, nearly 10%.
- The analysis and modeling are divided into two approaches:
  - Performance analysis and modeling: The goal of this analysis is to identify the key variables impacting the candidate's score, understand their relationship with performance, and utilize them for predicting the score. For the prediction task, a Lasso Regression model is employed, due to interpretability (coefficients), regularization and feature selection characteristics. Furthermore, a certain linear relationship between the features and the target was observed. For example, as the candidate's mother's education level increased, the performance also increased monotonically. This factor, coupled with the absence of multicollinearity, favored the selection of such a linear model.
  - Absenteeism analysis and modeling: The objective of this analysis is to identify the primary factors influencing a candidate's absence from the exam. Additionally, it aims to examine how these factors correlate with absenteeism and predict the probability of a student's abstention. For the prediction task, a Logistic Regression model is utilized, due to interpretability (exponential coefficients), regularization through l1 penalty, class_weight hyperparameter and efficiency characteristics. Furthermore, a certain linear relationship between the features and the target was observed. For example, as the candidate's mother's education level increased, the abstention rate decreased monotonically. This factor, along with the absence of multicollinearity, favored the choice of such a linear model.
- Two Flask APIs were developed for deploying the models from both aforementioned analyses. This enables the prediction of a candidate's score or the probability of absenteeism by providing socioeconomic and educational data about the candidate.
- [Click here to check out the entire project](https://github.com/allmeidaapedro/Enem-Analysis)

- Some interesting points discovered include:
- 1. Observing Lasso Regression coefficients, the increase of one unit in has_computer_at_home variable, that is, from zero to one, or from one to two or more, reflects an increase of 9.45 in the overall score, considering all other variables constant. That makes sense, as we observed in the performance analysis that students who did not have a computer at home exhibited lower performance compared to those who did.
  <p align="center">
  <img width="80%" height="80%" src="images/nota_pc_net.png">
  </p>

- 2. Observing Logistic Regression coefficients exponentials (representing the odds-ratio), for each increase of one unit in age group (i.e., from adolescent to young adult, adult to middle-aged to elderly, for example), the odds of abstention increase by 35%, considering all other variables constant. That makes sense, as we observed in the absence analysis that the abstention rate among adult, middle-aged, and elderly candidates was higher than that of adolescent and young adult candidates.

  <p align="center">
  <img width="80%" height="80%" src="images/comparecimento_faixa_etaria.png">
  </p>

- Some results obtained and model validation;

<p align="center">
  <img width="65%" height="30%" src="images/actual_predicted.png">
</p>

<p align="center">
  <img width="80%" height="80%" src="images/faixas_score_ausentes.png">
</p>

- Deployment;

<p align="center">
  <img width="70%" height="70%" src="images/desempenho_predicao.png">
</p>

<p align="center">
  <img width="70%" height="70%" src="images/predicao_abstencao.png">
</p>



## CLASSIFICATION


### [**German Bank's Credit Scoring**](https://github.com/allmeidaapedro/Credit-Scoring-German-Bank)
- This is an end-to-end machine learning project (from data collection to deploy) that uses Random Forest to assign credit scores to potential customers of a German bank.
- By doing so, it can make informed decisions, protecting Return on Investment (ROI) while minimizing credit risk.
- I estimated financial results calculating ROI using the expected revenue from non-defaulters' loans, the expected loss from defaulters' loans, and the total credit amount lent before the solution and after changing the bank's credit policy from my credit scoring model. Finally, after extending credit only to customers with a credit score of 600 or higher, the ROI increased from 9.55% to 42.64%.
- [Click here to check out the entire project](https://github.com/allmeidaapedro/Credit-Scoring-German-Bank)

- Some results obtained and model validation.
<p align="center">
  <img width="65%" height="30%" src="images/probability_distributions_by_default.png">
</p>

- Deployment.
<p align="center">
  <img width="70%" height="70%" src="images/predict_page_webapp.jpeg">
</p>


### [**Credit Card Churn Prediction**](https://github.com/allmeidaapedro/Churn-Prediction-Credit-Card)
- This is an end-to-end machine learning project (from data collection to deploy) that utilizes XGBoost to predict customer's probability of churning in a bank's credit card service.
- Identifying likely churners helps plan strategies for retention, maintaining healthy revenue. Acquiring a new customer is costlier than keeping one. 
-  The main objectives were: Identify the factors associated with customer churn; construct a model capable of predicting as many potential churners as possible; offer action plans for the bank to reduce credit card customer churn.
- It was possible to achieve an estimated gain of $198,098.82 by calculating the difference between the true positive gain, the cost of retaining false positives and the cost of false negatives churning.
- [Click here to check out the entire project](https://github.com/allmeidaapedro/Churn-Prediction-Credit-Card)

- Some analysis made;
<p align="center">
  <img width="80%" height="80%" src="images/numeric_distributions_by_churn.png">
</p>
 
- Deployment;
<p align="center">
  <img width="20%" height="20%" src="images/output_example.jpeg">
</p>


## REGRESSION / TIME SERIES FORECASTING

### [**Store Item Demand Forecasting**](https://github.com/allmeidaapedro/Store-Item-Demand-Forecasting)
- In this project, I performed time series forecasting using LightGBM to predict sales for 50 items across 10 different stores in a 3-month period.
- By doing this, the company will be able to strategically manage inventory and allocate resources effectively, maximizing overall revenue and profit. 
- The financial result per store, per store and item and for the total company is present inside the project.
- [Click here to check out the entire project](https://github.com/allmeidaapedro/Store-Item-Demand-Forecasting)

- Some analysis made;
<p align="center">
  <img width="50%" height="50%" src="images/time_series_decomposition.png">
</p>

- Model results;
<p align="center">
  <img width="80%" height="80%" src="images/actual_pred_graph_lgb.png">
</p>


## CLUSTERING

### [**Retail Store's Customer Segmentation and Fidelity Program**](https://github.com/allmeidaapedro/Customer-Segmentation-Retail)
- In this project, I performed an unsupervised learning clustering task using K-Means on unlabeled training data to segment and profile customers for a retail store.
- After segmenting the clients, a loyalty program called "Prosperous" was developed based on the profile of our best customers, the Prosperous ones. 
- The loyalty program has the potential to increase the total store revenue by 9%, amounting to $125,228.55. Therefore, the project is worthwhile.
- [Click here to check out the entire project](https://github.com/allmeidaapedro/Customer-Segmentation-Retail)

- Clustering;
<p align="center">
  <img width="65%" height="65%" src="images/sihouette_plot_kmeans.png">
</p>

- Model results;
<p align="center">
  <img width="80%" height="100%" src="images/scatterplot_clusters.png">
</p>


## EXPLORATORY DATA ANALYSIS

### [**Olist Store**](https://github.com/allmeidaapedro/Olist-Analysis)
- In this project, I performed an exploratory data analysis of a Brazilian e-commerce company, Olist. Some business questions were formulated and answered through techniques involving data collection, cleaning, exploration, and visualization.
- [Click here to check out the entire project](https://github.com/allmeidaapedro/Olist-Analysis)
- Some interesting business questions that have been answered include:
- 1. The sales grew over the two years, reaching their peak in November 2017, likely due to Black Friday. Furthermore, it is noticeable that after this peak in 2017, sales tend to maintain at a high number compared to previous years.

<p align="center">
  <img width="65%" height="65%" src="images/vendas_mensal.png">
</p>

- 2. The states in the South and Southeast regions concentrate the highest numbers of orders, customers, and sellers. Particularly, the state of São Paulo and its capital exhibit values higher than all others. Meanwhile, states in the North and Northeast regions show the lowest indicators.

<p align="center">
  <img width="65%" height="65%" src="images/pedidos_por_cidade.png">
</p>


## IN DEVELOPMENT 
- I am currently studying and working on credit field projects.

## CONTACT ME
* [LinkedIn](https://www.linkedin.com/in/pedro-henrique-almeida-oliveira-77b44b237/)  
* [GitHub](https://github.com/allmeidaapedro)
* [E-mail](pedrooalmeida.net@gmail.com)









