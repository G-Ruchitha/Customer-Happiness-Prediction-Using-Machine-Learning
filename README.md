PROJECT REPORT: Predicting Customer Happiness

OBJECTIVE

The objective of this project is to develop a machine learning model to predict customer happiness, with a particular focus on identifying unhappy customers based on survey responses about logistics and delivery services. Key factors analyzed include on-time delivery, order accuracy, pricing, courier satisfaction, and app usability. The primary metric of interest is recall, aimed at accurately identifying unhappy customers to enhance overall customer satisfaction.

DATA PREPARATION

Dataset Overview: The dataset was loaded and checked for balance and null values. It was confirmed to be balanced with no missing values.
Exploratory Data Analysis (EDA): Extensive EDA was conducted using visualization techniques like bar plots, box plots, and heatmaps to understand feature relationships and their impact on customer satisfaction.

MODEL SELECTION

Model Choice: Models were selected based on the results of LazyPredict, which was used to perform a preliminary evaluation of various models on the dataset. The models chosen for detailed evaluation—Logistic Regression, SVC, Gaussian Naive Bayes, Decision Trees, Random Forest, AdaBoost, and XGBoost—demonstrated the most promise based on their initial performance metrics.

Seed Value: A seed value of 7352 was used to ensure reproducibility in data splitting and model training.

MODEL DEVELOPMENT and EVALUATION

Model Training:

Logistic Regression: Accuracy of 65.38%, recall for unhappy customers (0) was 0.36, and for happy customers (1) was 0.87.

Support Vector Machines (SVC): Accuracy of 73%, recall for unhappy customers (0) was 0.82, and for happy customers (1) was 0.67.

Gaussian Naive Bayes: Accuracy of 50%, recall for unhappy customers (0) was 0.45, and for happy customers (1) was 0.53.

Decision Trees: Accuracy of 73.1%, recall for unhappy customers (0) was 0.64, and for happy customers (1) was 0.80.

Random Forest: Accuracy of 73.1%, recall for unhappy customers (0) was 0.55, and for happy customers (1) was 0.87.

AdaBoost: Accuracy of 57%, recall for unhappy customers (0) was 0.55, and for happy customers (1) was 0.60.

XGBoost: Accuracy of 73%, recall for unhappy customers (0) was 0.64, and for happy customers (1) was 0.80.

BEST MODEL SELECTION:

Voting Classifier (Hard Voting): The combination of Logistic Regression, SVC, and Decision Trees achieved an accuracy of 76.9%. Notably, it had the highest recall for unhappy customers (0) at 0.91, indicating its superior capability to correctly identify unhappy customers. This aligns well with the project's objective of maximizing recall for unhappy customers while maintaining a strong performance for happy customers.

OPTIMIZATION and FEATURE SELECTION

Hyperopt Optimization: Applied Hyperopt for parameter tuning but observed that results were consistent with the Voting Classifier (Hard Voting) model.

Feature Selection: Implemented Recursive Feature Elimination (RFE) using Decision Trees to select the top 4 features ('X2', 'X3', 'X4', 'X5'). Despite using fewer features, the performance of the Voting Classifier with Hard Voting remained the same, demonstrating efficiency in model performance with reduced features.

CONCLUSION

The Voting Classifier with Hard Voting proved to be the best model due to its high recall for unhappy customers (0.91) and its effective performance with fewer features. This approach meets the project's goal of accurately identifying unhappy customers to address issues proactively. The model’s performance and reduced feature set contribute to both operational efficiency and computational effectiveness.

