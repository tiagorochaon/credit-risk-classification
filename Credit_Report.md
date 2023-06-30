Module 12 Report


Overview of the Analysis

The purpose of this analysis was to develop machine learning models for credit risk assessment. The data used in the analysis contained financial information related to loans, and the goal was to predict the risk of loan default. The analysis involved the following stages:

Data preprocessing: The lending data was loaded into a Pandas DataFrame, and the labels and features were extracted accordingly.

Model training and evaluation: Two machine learning models were trained and evaluated, namely Model 1 and Model 2. Model 1 was based on logistic regression, while Model 2 utilized resampling techniques.

Results
Here are the results of the machine learning models:

Model 1

Accuracy: 0.952

Precision (0): 0.995

Precision (1): 0.860

Recall (0): 0.995

Recall (1): 0.910


Confusion Matrix:

[[14926    75]
 [   46   461]]
Classification Report:


Copy code
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     15001
           1       0.86      0.91      0.88       507

    accuracy                           0.99     15508
   macro avg       0.93      0.95      0.94     15508
weighted avg       0.99      0.99      0.99     15508


  
Model 2


Accuracy (Resampled): 0.994

Precision (0): 1.00

Precision (1): 0.85

Recall (0): 0.99

Recall (1): 0.99


Confusion Matrix (Resampled):

[[14915    86]
 [    3   504]]


Classification Report (Resampled):

              precision    recall  f1-score   support

           0       1.00      0.99      1.00     15001
           1       0.85      0.99      0.92       507

    accuracy                           0.99     15508
   macro avg       0.93      0.99      0.96     15508
weighted avg       1.00      0.99      0.99     15508


Summary


Both models performed well in predicting credit risk, but they had slightly different performance characteristics.

Model 1 demonstrated an accuracy of 0.952 and achieved a high precision and recall for both healthy loans (0) and high-risk loans (1). It correctly identified 99.5% of healthy loans and 91% of high-risk loans. However, the precision for high-risk loans was relatively lower compared to the precision for healthy loans. Model 1 would be suitable when it is important to predict both healthy and high-risk loans accurately, but with a slightly higher tolerance for false positives in high-risk loan predictions.

Model 2, which utilized resampling techniques, showed an accuracy of 0.994. It had high precision and recall scores for both loan categories, with precision of 100% for healthy loans and 85% for high-risk loans. The model achieved excellent performance in identifying high-risk loans, with a recall score of 99%. This model is recommended when the priority is to accurately identify high-risk loans, even if it results in a few more false positives.

Considering the results, Model 2 performed slightly better in terms of accuracy and precision for high-risk loans. However, the choice of the model depends on the specific requirements and priorities of the credit risk assessment problem. If the focus is on minimizing the number of false positives in identifying high-risk loans, Model 2 is recommended. If a balanced approach is desired, where both healthy loans and high-risk loans are predicted accurately, Model 1 would be a suitable choice.

It is important to note that these models can be further improved and optimized by exploring additional techniques, fine-tuning hyperparameters, and incorporating more advanced algorithms. Regular updates and retraining of the models with new data are also recommended to ensure their performance remains up-to-date.

Overall, the machine learning models provide valuable tools for credit risk analysis, enabling financial institutions to make informed decisions, allocate resources effectively, and manage credit risks with greater confidence.
