# Predicting-Covid-Cases-in-Mexico

## Business Understanding

### Problem Statement

The Ministry of Health is struggling to manage the escalating COVID-19 pandemic amid rising cases and limited resources in Mexico. Predictive analysis is urgently needed to inform public health interventions optimize hospital management strategies and  ensure early detection of the virus to provide containment and isolations to the affected.

The primary Objectives are:

1. Identify key factors influencing the rise in Covid-19 cases.

2. Develop a predictive machine learning model to identify factors that may contribute to an increase in positive Covid-19 cases. 

3. Provide insights and recommendation

## Data Understanding

The primary source of COVID-19 data is Mexico’s Ministry of Health .Their data was often shared on platforms like the Dirección General de Epidemiología (General Directorate of Epidemiology) website

The dataset contains 10,000 entries (rows) and 23 columns.This dataset contains information about COVID-19 patients, including demographic information, medical statuc, symptoms, test results, and outcomes

## Methods

The project will follow the following steps:

a. Exploratory Data Analysis: We will perform an in-depth exploration of the dataset to gain insights into the distribution of variables, identify patterns, and detect any data quality issues.

b. Data Preprocessing: This step involves handling missing values, encoding categorical variables, and scaling numerical features.

c. Feature Selection: We will identify relevant features that have a significant impact on customer churn prediction. 

d. Model Selection and Training: We will compare various classification algorithms, such as logistic regression, decision trees, and random forests, to select the most suitable model for predicting customer churn. 

e. Model Evaluation: We will assess the performance of the trained model using appropriate evaluation metrics, including accuracy, precision, recall, and F1-score. 

f. Model Optimization: We will fine-tune the selected model by adjusting hyperparameters and employing techniques like grid search. This optimization process aims to maximize the model's predictive capabilities. The models used include Logistic Regression, Decision Trees and Random Forests. 

In each model the performance metrics; accuracy, precision, recall and f1 score were calculated. Confusion matrix for each model was also plotted. The best model is then evaluated from the models. For LOgicticRegression with GridsearchCV only, feature importance to see which features played a role in customer churn is provided.

## Exploratory Data Analysis

###Univariate analysis

Distribution of the target variable

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/8a884df6-f3f7-4aff-a3fc-29da751aca56)

The graph shows the highest number of negative covid results of aproximately 5000 , followed by positive results of approximately 4000 lastly appproximately 1000 people had not yet received their results.
