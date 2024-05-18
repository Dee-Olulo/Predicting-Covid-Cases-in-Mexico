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

### Univariate analysis

Distribution of the target variable

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/8a884df6-f3f7-4aff-a3fc-29da751aca56)

The graph shows the highest number of negative covid results of aproximately 5000 , followed by positive results of approximately 4000 lastly appproximately 1000 people had not yet received their results.

## Bivariate analysis

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/81943452-1a41-4957-bec0-48434d0b8ebd)

The 5th month (May) had the highest number of positive covid results and the cases dropped significantly during the month of July.

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/b446c13d-74b2-471c-8754-b8a1b3ef923a)

More females tested negative while more males tested positive.In both categories:
- The majority of the test results are Negative (represented by the blue bars).
- The second most common result is Positive (represented by the orange bars).
- The least common result is Awaiting Results (represented by the green bars).


![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/74c23f0e-0697-43ba-8257-ff0f93da34c2)

May had the highest number of covid Test results while July had the least number of covid test results

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/b32d0218-2023-4331-9d2e-f9e0ca756b70)

Most of the people that had tested positive survived while those that died were few approximately 400.

## Multivariate analysis

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/21fb04cd-2a52-4110-a313-2962c0d96e06)

Most of the people that were not pregnant and tested positive died

## Modelling

### Logistic Regression Modelling

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/0a6f0d58-418b-4e35-9f3b-6e53d8e7b638)

**Observations**

**Accuracy:** The model's accuracy is 63%, indicating the percentage of correctly predicted instances. However, it should be considered alongside other metrics for a complete evaluation.

**Precision:** The precision is 68%, implying that more than half of the predicted positive instances are actually true positives.

**Recall:** The recall is 34%, indicating the model's ability to correctly identify positive cases among all actual positive cases.

**F1 Score:** The F1 score, at 0.453731, represents a moderate balance between precision and recall.

**Confusion Matrix :** The confusion matrix provides a detailed breakdown of the model's predictions, including the number of true negatives, false positives, false negatives, and true positives.


The confusion matrix provides information on the model's performance in classifying instances. In this case, the confusion matrix reveals the following:

**True Negatives (TN):** There are 1039 instances where the model predicted the test result as negative, and the individual is indeed free of COVID-19..

**False Positives (FP):** There are 156 instances where the model predicted the test result as positive, but the individual does not have COVID-19.

**False Negatives (FN):** There are 653 instances where the model predicted the test result as negative, but the individual does have COVID-19

**True Positives (TP):** There are 329 instances where the model predicted the test result as positive, and the individual does have COVID-19.

Based on the confusion matrix, it is evident that the model struggles with correctly identifying instances that are actually positive results, as indicated by the relatively high number of false negatives (653). This observation aligns with the low recall score (34%) obtained in the evaluation results.

**AdaBoost Classifier**
![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/a41a9dfb-33ae-4aab-9f80-b64c8f471d91)



The model's accuracy is 62%, indicating the percentage of correctly predicted instances. While this is slightly above random guessing for a balanced dataset, it should be considered alongside other metrics to understand its real-world performance.

Overall Precision (68%): This was incorrectly stated in the provided criteria. Correct precision is 59% for class 1 and 63% for class 0. Precision of 59% for positive cases means that more than half of the predicted positive instances are true positives. Recall:

Overall Recall (34%): This was also incorrectly stated. Correct recall is 49% for class 1 and 72% for class 0. Recall of 49% for positive cases indicates that the model is missing half of the actual positive cases, which is concerning for early detection and containment. F1 Score:

Overall F1 Score (0.453731): This was incorrectly stated. Correct F1 score is 0.54 for class 1 and 0.67 for class 0. An F1 score of 0.54 for positive cases represents a moderate balance between precision and recall but indicates room for improvement in both metrics. 

## Decision Trees

**Decision Trees with Bagging Performance:**

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/3689829a-1f14-42d0-b32b-5ee2ed5599e0)

Decision Trees with Bagging Performance:

Accuracy: The model's accuracy is 63%, meaning that 63% of the total predictions (both positive and negative) are correct. Precision:

precision for class 1 (positive cases) is 65%, implying that more than half of the predicted positive instances are actually true positives. However, there are still a significant number of false positives, indicated by the relatively high number of false positives (346 instances).

Recall: The recall for class 1 (positive cases) is 40%, indicating that the model misses 60% of the actual positive cases. This is concerning for early detection and containment of COVID-19, as a high recall is crucial for identifying as many positive cases as possible.

F1 Score: The F1 score for class 1 (positive cases) is 50%, representing a moderate balance between precision and recall. However, there is room for improvement, particularly in recall.

#### Random Forest with Bagging and Subspace Sampling:

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/5b59865c-b3a8-4c08-b61f-72d1a911df06)

**Accuracy:**

The model's accuracy is 56%, meaning that 56% of the total predictions (both positive and negative) are correct.This is quite low. This indicates that the model is making a significant number of incorrect predictions

###  ROC Curves

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/097bf19e-fe9a-482d-875f-63078a9f803b)

### Feature Importance

![image](https://github.com/Dee-Olulo/Predicting-Covid-Cases-in-Mexico/assets/151445934/b9832d32-075b-4c39-b371-44244bbd64ce)

## Best Model Evaluation

**Logistic Regression with GridSearchCV**  appears to be the best performer among the models in predicting the highest percentage 
of positive cases.This means that individuals who actually have the virus are more likely to be identified correctly. This would be the best Model for the Ministry of Health to ensure:

Accurate case predictions support the planning and distribution of healthcare resources like hospital beds, ventilators, and medical staff.
Identification of  high-risk groups and optimizing vaccine distribution.

**Model Evaluation**

**Accuracy:**

The model's accuracy is 62%, meaning that 62% of the total predictions (both positive and negative) are correct

**Precision:** The precision is 59%, implying that more than half of the predicted positive instances are actually true positives, but there is still a significant number of false positives.

**Recall:** The recall for class 1 indicates that the model misses 50% of the actual positive cases, which is concerning for early detection and containment.

**F1 Score:** The F1 score, at 54%, represents a moderate balance between precision and recall.

**Detailed Confusion Matrix**

**Evaluation True Negatives (TN):** 849 instances where the model correctly predicted negative cases.

**False Positives (FP):** 346 instances where the model incorrectly predicted positive cases (individuals do not have COVID-19 but were predicted as positive).

**False Negatives (FN):** 491 instances where the model incorrectly predicted negative cases (individuals have COVID-19 but were predicted as negative).

**True Positives (TP):** 491 instances where the model predicted the test result as positive, and the individual does have COVID-19
n.

**The Most important features for predicting Covid19 positive results are:**

patient_type_Inpatient

age

date_symptoms

died 

pneumonia_yes

## Conclusion and Recomendations
**Age:** Prioritize vaccination for older adults, as age is a significant predictor of severe COVID-19 outcomes.

**Date Symptoms First Appeared:** Implement aggressive testing and contact tracing strategies for individuals who report early onset of symptoms to quickly identify and isolate positive cases.
 
**Patient Type (Inpatient):** Prioritize allocation of hospital beds and ventilators to facilities handling a higher proportion of inpatients, as these patients are more likely to have severe cases.

Ensure that hospitals with a high number of inpatients are adequately staffed with specialized healthcare professionals.

**Moratlity**: Conduct thorough reviews of mortality cases to identify factors leading to severe outcomes and improve treatment protocols.

**pneumonia_yes:** Respiratory Support: Provide adequate respiratory support, including supplemental oxygen and ventilators, for patients with pneumonia.


### Limitations

The dataset used in the case study was constrained by limited information. Key factors like vaccination status, geographic location, behavioral aspects such as mask-wearing, symptom severity, and genetic history could significantly enhance accuracy and predictive capabilities.
