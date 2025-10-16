#Postpartum Depression Detection

🧠 Postpartum Depression Detection using Machine Learning
📋 Overview

Postpartum Depression (PPD) is a critical mental health condition that affects mothers shortly after childbirth, typically within 6–8 weeks. This project aims to develop a machine learning-based system capable of detecting postpartum depression from structured behavioral and psychological data.

By analyzing features such as anxiety, emotional instability, and behavioral changes, the system assists in early diagnosis and prevention of mental health deterioration — potentially reducing the risk of self-harm and ensuring better postnatal care.

A comparative analysis was performed among three classification models:

K-Nearest Neighbors (KNN)

Naive Bayes

Decision Tree

The goal was to determine the most efficient and reliable model for identifying signs of postpartum depression.

📊 Dataset Description

Source: Kaggle – Postpartum Depression Dataset

Total Data Points: 1,503
Features: 12
Target Variable: Feeling anxious (Binary: Yes / No)

Each record represents behavioral and psychological indicators of a mother, categorized using categorical values (Yes/No). These were later numerically encoded using one-hot encoding for model training.

⚙️ Feature Processing

Dropped irrelevant columns: ID, Timestamp

Removed rows with null values to maintain data integrity

Applied one-hot encoding to categorical features

No feature scaling was needed since all encoded values range between 0 and 1

⚖️ Dataset Balance

The target distribution was:

Yes: 968 (64.92%)

No: 523 (35.07%)

Thus, the dataset is reasonably balanced with a 60:40 ratio.

🧩 Data Splitting

The dataset was divided as follows:

Training Set: 70%

Testing Set: 30%

Stratification: Applied to maintain class balance across splits.

🤖 Model Training & Evaluation

Three machine learning algorithms were trained and evaluated based on accuracy, precision, recall, and F1-score.

Model	Accuracy	Precision	Recall	F1-Score
KNN	88.17%	0.91	0.92	0.91
Naive Bayes	82.59%	0.85	0.85	0.85
Decision Tree	97.10%	0.97	0.97	0.97

🩺 Since this is a mental health-related problem, minimizing false negatives is critical — hence recall is the most important metric.
The Decision Tree model achieved the highest recall and overall performance, making it the most suitable choice for postpartum depression detection.

🧠 Key Findings

Decision Tree achieved the highest accuracy and recall (97.10%).

KNN performed well with moderate recall.

Naive Bayes had the lowest performance, likely due to its independence assumption not fitting the dataset correlations.

Overfitting risk in Decision Tree was noted but acceptable given the dataset size and performance metrics.

🚀 Conclusion

This study highlights the potential of machine learning in early mental health diagnostics, particularly postpartum depression.
The Decision Tree model demonstrated strong predictive capability, which could help in developing screening tools for healthcare professionals.

Future improvements could include:

Expanding dataset size for better generalization.

Experimenting with ensemble methods (Random Forest, XGBoost).

Incorporating temporal and clinical data for deeper insights.

💻 Technologies Used

Python 3.9+

Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

Environment: Jupyter Notebook / Google Colab
