# Churn-Prediction-G2

## Overview


A bank manager from Credit Card Incorporated (CCI) is facing high attrition for their credit card customers. The bank manager hired our team to realize a solution and formulate a strategy to reduce the high attrition rates. Our team is going to utilize AI models to predict which customers will cancel their card and create a strategy to address the factors causing attrition.

In our report we will cover:

* [***Repository Structure:***](#repository-structure) Our repository structure, commit history, and files
* [***Business Understanding:***](#business-understanding) Our understanding of the goal, key questions, and stakeholders
* [***Data Understanding and Analysis:***](#data-understanding-and-analysis) Our data sources, descriptions, and visualizations
* [***Statistical Analysis:***](#statistical-analysis) Our statistical analysis and interpretation
* [***Conclusion and Recommendations:***](#conclusion-and-recommendations) Our relevant findings and recommendations

Related PowerPoint presentation and Jupyter notebook are linked below:

[PowerPoint Presentation](Capstone_Group2_Presentation.pdf)

![Jupyter Notebook](https://github.com/PaolaMalagon/Churn-Prediction-G2/blob/main/Churn-Prediction-G2.ipynb)

## Repository Structure

Our repository has a simple structure consisting of branches for different team members. The Repositoy Contains the following files -

* **Presentation: "Capstone_Group2_Presentation.pdf"**
* **Jupyter Notebook: "Churn-Prediction-G2.ipynb"**
* **Proposal: "GROUP 2_JUNE 23.pdf"**
* **Data Source: "credit_card_churn.csv"**

## Business Understanding

### Key Business Question

The key questions we are trying to answer is if a customer will cancle their card or not. Additionally, being able to identify what factors specifically are strong predictors for churn will provide value in reducing the attrition. 

### Stakeholder Understanding

The business manager who hired us is trying to lower attrition rates. The have success in the eyes of the stakeholder, our team needs to create a model that will assist in lowering attrition.

Lowering attrition is going to help the bank increase their profits. The longer customers are keeping and using their cards, the greater the benefit for the bank. There are other impacts that are more difficult to measure. A customer could have canceled their card and then became very outspoken against the bank. Negative reviews from previous customers could impact the banks ability to gain new customers. 

## Data Understanding and Analysis

In order to make actionable recommendations for CCI it is imperative to understand and analyze the data.

### Source of Data

We used the following dataset:

[Dataset](credit_card_churn.csv)

### Description of the data

The dataset contains 10,127 rows of client information with no null values. There are 23 columns in the data set, 19 of them are useful for predicting attrition. There were 5 categorical attributes. 

There were several steps for cleaning the data. First, dropping columns that were not relevant to the analysis including client number. Second, encoding the categorical data. Data that had a natural order was label encoded, and data without natural order was one hot encoded. Finally, we had to examine the unknowns in the data. Ulitmately, there were not a significant amount that would affect the results so we left the unknowns in the dataset. 

### Data Analysis

Our team chose to utilize multiple different algorithms to evaluate which model would produce the best results for CCI. The models that we focused on were logistic regression, decisions tree, random forest, and XGBoost. Our team also created an ANN and ADABoost model, but decided to focus our resources on the other models for the best results. 

## Statistical Analysis

To compare our models and make the best recommendations for CCI, our team to fairly evaluate the performance of different models.

### Accuracy

Our first analysis was looking at the accuracy of different models. The majority of the models were performing in the range of 93-97% accuracy. While initially this seems impressive, accuracy is a crude metrics and not the best for comparing the performance of our models

### Precisions, Recall, F-1, and more

To provide a better recommendations our team expanded beyond just accuracy as a metric. Including precision, recall, and f-1 scores gives the team a better sense of what model is performing the best. Additionally, our team wanted to focus on trying to reduce false negative. This is an instance where the model predicts a customer will not churn, and the customer ends up canceling their card. From our business understanding, false negative could have the greatest impact on the business. 

### Best model

Random Forest was the best performing model overall. XGBoost had a slightly higher recall scores with a few less false negatives; however, because the precision and f-1 score were so much lower it was not worth the tradeoff. 

## Conclusion and Recommendations

Our final recommendation to CCI is to implement the Random Forest model.

### Business Solution

The Random forest model scored quite well in recall and false negatives. For CCI, that means they are going to be able to predict fairly accurately which customers will cancel their card. Additionally, there will be less impact from customers who cancel but were not predicted to. The Random Forest model also has visibility and interpretability into which variables are the strongest predictors for a customer to cancel. 

CCI is going to be able to decrease their attrition rate leading to increased customer lifetime value, decreased customer acquisition costs, improved company valuation, and increase in the number of satisfied customers. In the future, CCI could use this model to address similar clafficiation problems such as fraud, or loan approval. 