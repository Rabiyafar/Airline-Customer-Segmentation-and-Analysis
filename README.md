Airline Passenger Satisfaction Analysis & Segmentation
Project Overview
This project analyzes airline passenger satisfaction using a dataset from Kaggle. The goal is to understand factors influencing satisfaction and predict whether a passenger is satisfied or not using machine learning. Additionally, the project explores customer segmentation to identify passenger groups with distinct behavior patterns.
Dataset
Source: Kaggle – Airline Passenger Satisfaction
Files: train.csv (103,904 rows), test.csv (25,976 rows)
Features: 25 features including passenger demographics, flight experience metrics (seat comfort, online booking ease, onboard services), and delays.
Target: satisfaction – whether the passenger is satisfied or neutral/dissatisfied.

Project Structure
Airline_Passenger_Segmentation/
│
├── data/
│   ├── train.csv
│   └── test.csv
│
├── notebooks/
│   └── Airline_Segmentation.ipynb
│
├── scripts/
│   └── preprocessing.py
│
├── README.md
└── requirements.txt

Steps Performed
1. Exploratory Data Analysis (EDA)
Checked distributions of age, flight distance, delays, and satisfaction.
Visualized satisfaction by class, type of travel, and other key features.
Identified missing values and outliers.

2. Data Preprocessing
Filled missing values (e.g., Arrival Delay in Minutes).
Encoded categorical features: Gender, Customer Type, Type of Travel, Class.
Converted target variable satisfaction to binary: 1 = satisfied, 0 = neutral/dissatisfied.
Scaled numeric features using StandardScaler.

3. Customer Segmentation (Clustering)
Applied K-Means clustering on key features.
Identified distinct passenger segments based on travel behavior and satisfaction metrics.
Visualized clusters to gain insights into passenger profiles.

4. Prediction (Classification)
Used Random Forest Classifier to predict passenger satisfaction.
Performance Metrics on Test Set:
Accuracy: 96.4%
Precision, Recall, F1-score: Balanced across satisfied and dissatisfied classes.

5. Feature Importance
Top factors influencing satisfaction:
Online boarding (16.7%)
Inflight Wi-Fi service (15.3%)
Class (11%)
Type of Travel (9.4%)
Inflight entertainment (5.6%)
Seat comfort (4.4%)

Lower importance features: Gender, Departure Delay in Minutes, etc.

Visualization: Bar chart of feature importance included in the notebook.

Insights
Smooth online boarding and Wi-Fi services are the most critical for passenger satisfaction.
Business class and type of travel significantly influence expectations.
Airlines can prioritize improvements in boarding process, Wi-Fi, seat comfort, and entertainment to improve overall passenger satisfaction.

Technologies Used
Python (pandas, NumPy, matplotlib, seaborn, scikit-learn)
Machine Learning: Random Forest, K-Means
Data preprocessing, feature engineering, scaling, and encoding

