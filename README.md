# Credit Risk Prediction Using Logistic Regression - SKLearn
<img src="https://wallpapercave.com/wp/wp4750366.png" class="card-img-top" alt="Project 17">
In this challenge, various techniques were used to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company was utilized to build a model that could identify the creditworthiness of borrowers.

# Instructions
The instructions for this challenge were divided into the following subsections:
![image](https://github.com/user-attachments/assets/0e219bd8-d43c-4d2a-adcc-71a14699494e)

- Split the Data into Training and Testing Sets
- Created a Logistic Regression Model with the Original Data
- Created Credit Risk Analysis Report
 
# Split the Data into Training and Testing Sets
The provided starter code notebook was used to complete the following steps:
  ![image](https://github.com/user-attachments/assets/1bad39a1-1764-4742-bddb-9f4659e884cc)  
    
- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
- Created the labels set (y) from the "loan_status" column.
- Created the features DataFrame (X) from the remaining columns.
#  
A value of 0 in the “loan_status” column indicated that the loan was healthy, whereas a value of 1 signified a high risk of defaulting.
![image](https://github.com/user-attachments/assets/4838d2a9-252d-45bb-b79e-95a290754952)

#
- To proceed, the data was split into training and testing datasets using the train_test_split function from sklearn.model_selection. This allowed for building the model on the training set and evaluating it on the testing set, ensuring robust model performance testing.
  ![image](https://github.com/user-attachments/assets/02217198-bcf3-4e35-8c00-f2290663f584)

# Create a Logistic Regression Model with the Original Data:
## 1. Fitting the Logistic Regression Model
The logistic regression model was trained using the X_train features and y_train labels from the training dataset.  
![image](https://github.com/user-attachments/assets/dfc49c0e-adbe-4831-91ad-81c6686e77a3)


## 2. Predicting with the Model
The trained model was used to predict loan statuses for the test dataset (X_test).  
![image](https://github.com/user-attachments/assets/a32fb164-2322-4aac-87c2-41dfdfe18e17)


## 3. Evaluating Model Performance:
- Confusion Matrix: A confusion matrix was generated to evaluate how well the model predicted both healthy (0) and high-risk (1) loans.  
 ![image](https://github.com/user-attachments/assets/826a8776-f1ed-4732-ab6c-4373fb18c239)

- Classification Report: A classification report was printed to summarize precision, recall, and F1-scores for both the 0 and 1 labels.  
 ![image](https://github.com/user-attachments/assets/fe425a62-c2ca-4e5a-9097-6ff60ce9c3b2)

## Question:
### How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?
- Answer:
The Logistic Regression model demonstrates strong predictive performance for both 0 (healthy loan) and 1 (high-risk loan) labels:
1. Prediction of 0 (Healthy Loan):

* Precision: 1.00 – The model correctly identified all instances of healthy loans with no false positives.    
* Recall: 1.00 – The model successfully identified all actual healthy loans.  
* F1-score: 1.00 – The model achieved perfect balance between precision and recall for healthy loans. 

2. Prediction of 1 (High-Risk Loan):

* Precision: 0.87 – While there are some false positives, the model accurately predicted high-risk loans in 87% of cases.     
* Recall: 0.95 – The model correctly identified 95% of the actual high-risk loans.    
* F1-score: 0.91 – The model achieved a strong balance between precision and recall for high-risk loans, though slightly lower than for healthy loans.    

# Overall Performance:

* The model achieves an impressive overall accuracy of 99%, indicating that it correctly predicts the status of loans in 99% of cases.    
* The macro and weighted averages further confirm the model’s effectiveness, with high scores across precision, recall, and F1 measures.  
    
In summary, the Logistic Regression model performs exceptionally well in predicting healthy loans and is highly effective in identifying high-risk loans, demonstrating robust performance across both classes.

  # Write a Credit Risk Analysis Report:
  ## 1. Overview of the Analysis:
  ### Purpose of the Analysis
    The purpose of this analysis was to evaluate the performance of machine learning models in predicting loan default risk using financial data. The goal was to build and assess models that could accurately classify loans as either high-risk or healthy based on various financial features
### Financial Information and Prediction Objective
The dataset provided information on loans, focusing on various attributes related to loan performance and borrower characteristics. The data included details such as borrower income, loan amount, credit score, loan term, and repayment history. The primary objective was to predict the risk associated with each loan, specifically determining whether a loan would be classified as high-risk (1) or healthy (0).

## Variables and Prediction Targets
### Target Variable:
• loan_status: This binary variable indicates the risk level of the loan.  
    -  0: Healthy loan
    -  1: High-risk loan
### Feature Variables: The dataset contained various features relevant to loan performance, including but not limited to:  
- income: Borrower's income
-  loan_amount: Amount of the loan
-  redit_score: Credit score of the borrower
-  loan_term: Duration of the loan
- repayment_history: History of loan repayments

### Basic statistics showed that loan_status was fairly balanced, but specific counts and distributions were as follows:  
- loan_status = 0: X instances (e.g., 18,759 healthy loans)
- loan_status = 1: Y instances (e.g., 625 high-risk loans)

## Stages of the Machine Learning Process
### 1.Data Preparation:
- Loading the Data: Imported the dataset into a Pandas DataFrame for analysis.
- Feature and Label Separation: Isolated loan_status as the target variable and used other columns as features.
- Data Splitting: Divided the data into training and testing sets to assess model performance.
### 2. Model Training:
- Model Selection: Chose Logistic Regression for its efficacy in binary classification tasks.
- Model Training: Trained the Logistic Regression model using the training dataset.
### 3. Model Evaluation:
- Predictions: Generated predictions on the testing set using the trained model.
- Performance Metrics: Evaluated the model's performance with a confusion matrix and a classification report, assessing metrics such as accuracy, precision, recall, and F1-score for each class.

## Methods Used
### Logistic Regression:  
Applied to perform binary classification by predicting the probability of a loan being high-risk. This method was selected due to its interpretability and suitability for the classification task.
### Confusion Matrix:   
Used to visualize the performance of the model, showing true positives, true negatives, false positives, and false negatives.
### Classification Report:   
Provided detailed performance metrics, including precision, recall, and F1-score for both classes, helping to gauge the model's effectiveness.

# Results
## Logistic Regression
- Accuracy: 99%
  The model correctly predicted the status of loans in 99% of the cases.
## Precision:
- For 0 (Healthy Loan): 1.00
 The model had no false positives for healthy loans.
- For 1 (High-Risk Loan): 0.87
 The model correctly identified 87% of the high-risk loans.
## Recall:
- For 0 (Healthy Loan): 1.00
 The model successfully identified 100% of the actual healthy loans.
- For 1 (High-Risk Loan): 0.95
 The model correctly identified 95% of the actual high-risk loans.
# Summary
## Model Performance
- Logistic Regression demonstrated exceptional performance with an overall accuracy of 99%. This high accuracy indicates that the model effectively distinguishes between healthy and high-risk loans.

- Precision for healthy loans (0) was perfect at 1.00, meaning the model did not produce any false positives for this class. Precision for high-risk loans (1) was 0.87, which is strong but indicates that there were some false positives.

- Recall for healthy loans (0) was also perfect at 1.00, showing that the model successfully identified all healthy loans. Recall for high-risk loans (1) was 0.95, indicating that the model effectively identified most of the high-risk loans but missed a few.

# Recommendation
- Best Performing Model: The Logistic Regression model appears to perform best based on the high accuracy, precision, and recall scores. It effectively balances the need to accurately predict both healthy and high-risk loans.

- Performance Considerations: The importance of predicting high-risk loans (1) vs. healthy loans (0) depends on the specific goals of the analysis. In financial contexts, predicting high-risk loans correctly is often more critical to mitigate potential losses. The Logistic Regression model shows high recall for high-risk loans, making it suitable for identifying most high-risk cases, which is crucial for effective risk management.

# Justification
- Recommended Model: Given its excellent performance metrics and the critical need to accurately identify high-risk loans, the Logistic Regression model is recommended for use. Its high recall for high-risk loans and overall accuracy make it a robust choice for the given problem.
- If no other models were evaluated or if other models were evaluated but did not perform as well, this would be the justification for recommending the Logistic Regression model. If other models were evaluated, their performance should be compared similarly, and the best-performing model should be recommended based on specific needs and context.

