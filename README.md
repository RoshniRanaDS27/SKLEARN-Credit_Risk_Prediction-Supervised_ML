# Credit Risk Prediction Using Logistic Regression - SKLearn
In this challenge, various techniques were used to train and evaluate a model based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company was utilized to build a model that could identify the creditworthiness of borrowers.
# Instructions
The instructions for this challenge were divided into the following subsections:

- Split the Data into Training and Testing Sets
- Created a Logistic Regression Model with the Original Data
- Created Credit Risk Analysis Report

# Split the Data into Training and Testing Sets
The provided starter code notebook was used to complete the following steps:
- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
- Created the labels set (y) from the "loan_status" column.
- Created the features DataFrame (X) from the remaining columns.
#  
A value of 0 in the “loan_status” column indicated that the loan was healthy, whereas a value of 1 signified a high risk of defaulting.
#
- To proceed, the data was split into training and testing datasets using the train_test_split function from sklearn.model_selection. This allowed for building the model on the training set and evaluating it on the testing set, ensuring robust model performance testing.
# Create a Logistic Regression Model with the Original Data:
## 1. Fitting the Logistic Regression Model
The logistic regression model was trained using the X_train features and y_train labels from the training dataset.  
![image](https://github.com/user-attachments/assets/dd9be625-b4fa-413b-8b09-aa320e5cf05d)

## 2. Predicting with the Model
The trained model was used to predict loan statuses for the test dataset (X_test).  
![image](https://github.com/user-attachments/assets/4892e3c3-bc40-47d9-9d83-855150efcfce)

## 3. Evaluating Model Performance:
- Confusion Matrix: A confusion matrix was generated to evaluate how well the model predicted both healthy (0) and high-risk (1) loans.  
  ![image](https://github.com/user-attachments/assets/a7ec5f1d-9602-45c1-9541-f92dde86e710)
- Classification Report: A classification report was printed to summarize precision, recall, and F1-scores for both the 0 and 1 labels.  
  ![image](https://github.com/user-attachments/assets/d8cead05-165a-40cc-8c11-da5a22d12968)
- Performance Question: How well did the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?
  Based on the classification report, the model's performance for both categories was analyzed. If precision and recall for both classes were balanced, the model accurately predicted both types of loans. Discrepancies between the two scores might indicate that the model struggled with either healthy or high-risk loans.

  # Write a Credit Risk Analysis Report:
  ### 1. Overview of the Analysis:
       The purpose of this analysis was to develop and evaluate a logistic regression model that predicts the creditworthiness of borrowers. Using historical lending data, the model aimed to classify loans into two categories: healthy (0) and high-risk (1).
  ### 2. Results:
- Accuracy Score: The accuracy score of the model was computed, representing how often the model predicted loan statuses correctly.
- Precision Score: Precision for both healthy and high-risk loans was assessed, indicating how well the model correctly identified the respective categories.
- Recall Score: Recall for both classes was measured to evaluate the model's ability to capture all true positive instances.
### 3. Summary: 
The logistic regression model's results indicated that it performed reasonably well in predicting both healthy and high-risk loans, as evidenced by balanced precision and recall scores. However, if the model exhibited high accuracy but lower precision for high-risk loans, it might misclassify high-risk loans more frequently, which would be concerning for the company's risk management. Based on these findings, the model may be recommended with additional adjustments or fine-tuning if high-risk loans require better classification.
