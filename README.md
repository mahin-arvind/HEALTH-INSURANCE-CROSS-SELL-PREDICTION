# HEALTH-INSURANCE-CROSS-SELL-PREDICTION
Cross-selling to existing clients has been one of the primary methods of generating new
revenue for many businesses. Identifying the potential buyers among existing clients can
help a company plan its communication strategy accordingly, thereby optimizing its
business model and increasing revenue.
In this project, our goal was to use the Health Insurance Cross-Sell dataset to understand
Vehicle Insurance Cross Sale Responses, apply machine learning techniques to identify
Vehicle Insurance buyers among pre-existing policyholders and provide explanations from
the best classifying model to understand factors affecting customer responses.

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

These obstacles were overcome in the Feature Engineering phase of the project, when:
1. Categories that occur less than 5 per cent of the time were binned together and
recognized as ‘Rare’.
2. The age of the client’s vehicle was numerically encoded.
3. Outliers in Annual Premium were capped at their lower and upper quartiles.
4. Categorical features were One Hot Encoded in order to be interpreted as categories.

After Feature Engineering, the dataset was scaled and split into training and testing sets.
Three sampling techniques, namely: Tomek Links, Synthetic Minority Oversampling
Technique (SMOTE) and SMOTE-EditedNearestNeighbors were performed on the training
set in order to counter the Imbalanced Dataset.

Eight models, namely Logistic Regression, Gaussian Naive Bayes, Decision Trees,
Gradient Boosting, CatBoosting, LightGBM, Bagging and Random Forest were tested and
evaluated based on their F2 scores. F2 score was the preferred metric as it gave emphasis
in minimizing false negatives and was relevant as it could help identify maximum
a number of potential customers.

Upon model deployment, tuning and evaluation, we found that the best performing model
was the Gaussian Naive Bayes classifier trained on SMOTE sampled training set with an
F2 score of 0.634614, precision of 27.58 per cent and recall of 94.02 per cent. The finalized
model’s predictions were dependent on the customer’s previous insurance status and
existing damages on the vehicle.

When the dataset was explored earlier in the project, approximately, one in every ten
clients had a positive cross-sale response when they were approached for cross-sale
(12.25 % success rate). From the confusion matrix, we were able to tell that the model
had correctly identified 94.04 per cent of the positive responses with a success rate of
27.58 per cent in predicting positive responders. This means that, approximately, three out
of every ten predicted buyers produced a positive response.

Therefore, the model not only helped identify a large part of the potential vehicle insurance
buyers but had also increased the success rate of cross-sales, helping the company save
a significant amount of time and resources by generating better leads.
