# HACKATHON

Welcome to our training project submission. Our team, consisting of five dedicated individuals, has embarked on a journey to explore the potential of deep learning in solving real-world problems. The project focuses on the telecommunications industry, where customer retention is a significant challenge. By leveraging advanced machine learning techniques, we aim to predict customer behavior and design targeted retention strategies.

## Problem Statement

The telecommunications industry faces a high customer churn rate, which is the percentage of customers who stop using a company's services within a given time frame. Our project aims to predict customer churn by analyzing relevant data and developing focused retention programs. The goal is to identify the factors that lead to customer attrition and provide actionable insights to reduce churn rates.

## Contributors

- @Praveen Parashar
- @Dharani Ramanlingam
- @Indumathi Purushothaman
- @Lakshman Vithal Sindhe

## Evaluation Criteria

- **Search for a tabular dataset [5 marks]:**
  - Our Response: `WA_Fn-UseC_-Telco-Customer-Churn.csv`
  - **DATASET:** [Kaggle Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

- **Define a problem statement (outcomes: Regression or Classification) [5 marks]:**
  - "Predict behavior to retain customers. You can analyze all relevant customer data and develop focused customer retention programs."

- **Use the following to work on your problem statement:**
  - **Automated ML [10 marks]:** [Azure ML Experiment](https://ml.azure.com/experiments/id/220ab086-8568-44be-816b-630eda241192?wsid=/subscriptions/11ceb257-f3cc-4fc0-aa96-a24dacc91774/resourcegroups/eygroup_2/providers/Microsoft.MachineLearningServices/workspaces/eygroup02&tid=e286c868-a1dd-469e-b686-2078f4936d8d)
  - Response:
    ![Best Model Metrics](https://github.com/user-attachments/assets/44ea984c-3e59-41b1-bea9-4894b4b57730)

## Conclusion

The best model was LightGBM with the following metrics:

| Metric | Value |
| ------ | ----- |
| Accuracy | 0.79269 |
| AUC macro | 0.83629 |
| AUC micro | 0.88359 |
| AUC weighted | 0.83629 |
| Average precision score macro | 0.79177 |
| Average precision score micro | 0.88521 |
| Average precision score weighted | 0.85784 |
| Balanced accuracy | 0.70617 |
| F1 score macro | 0.71743 |
| F1 score micro | 0.79269 |
| F1 score weighted | 0.78592 |
| Log loss | 0.43435 |
| Matthews correlation | 0.44107 |
| Norm macro recall | 0.41234 |
| Precision score macro | 0.73611 |
| Precision score micro | 0.79269 |
| Precision score weighted | 0.78400 |
| Recall score macro | 0.70617 |
| Recall score micro | 0.79269 |
| Recall score weighted | 0.79269 |
| Weighted accuracy | 0.84788 |

The hyperparameter is [here](https://github.com/jyoti-jha/openai-training/blob/main/Automated_ML/Hyperparameter.json)




## Notebook (Python) - Deep Learning [30 marks]

- The deep learning notebook for the classification model can be found [here](https://github.com/jyoti-jha/openai-training/blob/main/Deep_Learning_Telco_classification_model3.ipynb).
- We experimented with two different neural network architectures for this task:

### Architecture 1:
```python
from keras.models import Sequential
from keras.layers import Dense, Dropout

model = Sequential()
model.add(Dense(64, activation='relu', input_dim=X_train_preprocessed.shape[1]))
model.add(Dropout(0.5))
model.add(Dense(32, activation='relu'))
model.add(Dense(1, activation='sigmoid'))
```

### Architecture 2:
```python
from keras.models import Sequential
from keras.layers import Dense, Dropout

model3 = Sequential()
model3.add(Dense(16, activation='relu', input_dim=X_train_preprocessed.shape[1]))
model3.add(Dropout(0.2))
model3.add(Dense(1, activation='sigmoid'))
```
- Both architectures were trained and evaluated on the preprocessed feature set derived from the Telco Customer Churn dataset.

- The models were designed to predict the likelihood of customer churn, with the output layer using a sigmoid activation function suitable for binary classification.

### Metrics selection for evaluation [10 marks]
 - ##### AutomatedML
   The metrics is [here](https://github.com/jyoti-jha/openai-training/blob/main/Automated_ML/Test_metrics.md)
   and for the graph is [here](https://github.com/jyoti-jha/openai-training/blob/main/Automated_ML/Graph.md)

- ##### Deep-Learning
  The metrics is [here](https://github.com/jyoti-jha/openai-training/blob/main/Deep-Learning/Readme.md)


###  Use a LLM of your choice to perform search on private data or literature related to the dataset you have picked: [30 marks] – GPT embedding model

- The notebook can be found [here](https://github.com/jyoti-jha/openai-training/blob/main/Langchain_RAG.ipynb)




