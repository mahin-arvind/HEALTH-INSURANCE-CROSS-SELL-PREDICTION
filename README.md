# HEALTH-INSURANCE-CROSS-SELL-PREDICTION


   ![cliche-steth-pic](https://images.unsplash.com/photo-1532938911079-1b06ac7ceec7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8aGVhbHRoJTIwaW5zdXJhbmNlfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=800&q=60)

## 📖 Introduction

Cross-selling to existing clients has been one of the primary methods of generating new
revenue for many businesses. Identifying the potential buyers among existing clients can
help a company plan its communication strategy accordingly, thereby optimizing its
business model and increasing revenue.
In this project, the goal is to use the Health Insurance Cross-Sell dataset to understand
Vehicle Insurance Cross Sale Responses, apply machine learning techniques to identify
Vehicle Insurance buyers among pre-existing policyholders and provide explanations from
the best classifying model to understand factors affecting customer responses.

## 📖 EDA Observations and findings

The important observations identified during EDA were:
1. Most customers that purchased vehicle insurance had existing damages in their
vehicles, were not previously insured and owned vehicles aged over a year.
2. It was also observed that most policyholders of the health insurance company come
from three region codes: 28, 8 and 41.
3. The policy sales channels most preferred to reach out to the clients were channel
numbers 152, 26 and 124

The obstacles identified in the EDA phase of the project were:
1. The highly imbalanced dataset, with only 12.25 per cent of positive responses
observed.
2. Categorical attributes like Region Code and Policy Sales Channel contained over fifty
categories.
3. Vehicle Age attribute categorized a vehicle’s age into three categories in the form of
strings.
4. The numerical features, Annual Premium, contained a notable number of outliers.

## 📖 Feature Engineering
These obstacles were overcome in the Feature Engineering phase of the project, when:
1. Categories that occur less than 5 per cent of the time were binned together and
recognized as ‘Rare’.
2. The age of the client’s vehicle was numerically encoded.
3. Outliers in Annual Premium were capped at their lower and upper quartiles.
4. Categorical features were One Hot Encoded in order to be interpreted as categories.

## 📖 Sampling Methods
After Feature Engineering, the dataset was scaled and split into training and testing sets.
Three sampling techniques, namely:
* Tomek Links
* Synthetic Minority OversamplingTechnique (SMOTE), and
* SMOTE-EditedNearestNeighbors were performed on the training set in order to counter the Imbalanced Dataset.

## 📖 ML Models Evaluated

Eight models, namely 
1. Logistic Regression
2. Gaussian Naive Bayes
3. Decision Trees
4. Gradient Boosting
5. CatBoosting
6. LightGBM
7. Bagging, and 
8. Random Forest were tested 

## 📖 Evaluation Metric
* F2 score was the preferred metric as it gave emphasis in minimizing false negatives and was relevant as it could help identify maximum
a number of potential customers.


## 📖 Results
*  Upon model deployment, tuning and evaluation, we found that the best performing model
was the Gaussian Naive Bayes classifier trained on SMOTE sampled training set with an
F2 score of 0.634614, precision of 27.58 per cent and recall of 94.02 per cent. 

* The finalized model’s predictions were dependent on the customer’s previous insurance status and
existing damages on the vehicle.

## 📖 Conclusions
* When the dataset was explored earlier in the project, approximately, one in every ten
clients had a positive cross-sale response when they were approached for cross-sale
(12.25 % success rate).
* From the confusion matrix, we were able to tell that the model
had correctly identified 94.04 per cent of the positive responses with a success rate of
27.58 per cent in predicting positive responders. 
* This means that, approximately, three out of every ten predicted buyers produced a positive response.

Therefore, the model not only helped identify a large part of the potential vehicle insurance
buyers but had also increased the success rate of cross-sales, helping the company save
a significant amount of time and resources by generating better leads.

## 📋 References

1. Christopher M. Bishop, “Pattern Recognition and Machine Learning”, Pg.
137-139
2. Zhi-Hua Zhou, “Ensemble Methods Foundations and Algorithms”, Pg. 57-58
3. John T. Hancock and Taghi M. Khoshgoftaar, “CatBoost for big data: An
Interdisciplinary Review”
4. Essam Al Daoud, “Comparison between XGBoost, LightGBM and CatBoost
Using a Home Credit Dataset”.
5. Jason Brownlee,“Imbalanced Classification with Python: Better Metrics,
Balance Skewed Classes, Cost-Sensitive Learning”.

## 📋 Execution Instruction
The given IPython Notebook can be either downloaded to be run locally on Jupyter Notebook or on Google Colab via browser.

## 📜 Credits
* Project Done by Mahin Arvind Chanthira Sekaran
* Project Verified by Almabetter

## ☎ Contact

[![image](https://user-images.githubusercontent.com/95841292/202914376-d5a83f3d-110a-4476-896e-1da078b185dc.png)](https://www.linkedin.com/in/mahinarvind/) [![image](https://user-images.githubusercontent.com/95841292/202914715-787f6ae3-d9f6-491c-9cae-c717131ddebd.png)](https://github.com/mahin-arvind) [![image](https://user-images.githubusercontent.com/95841292/202914883-bce71634-6c2b-4305-8020-4b240cb76e41.png)](https://medium.com/@mahinarvindds) [![image](https://user-images.githubusercontent.com/95841292/202914940-5d5eba71-e45d-4e95-8dfe-65e45d255aec.png)](https://drive.google.com/file/d/1Hg5poNigBXo8cxisb9KjLc-H7Qy-Epsg/view?usp=share_link)
