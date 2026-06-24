# Airline Passenger Satisfaction Analysis & Segmentation

## Project Overview
This project analyzes airline passenger satisfaction to understand what drives it and to predict whether a passenger is satisfied or not. Beyond classification, it also explores **customer segmentation** to identify distinct passenger groups based on travel behavior — work that can inform both predictive modeling and targeted service improvements.

## Dataset
- **Source:** [Airline Passenger Satisfaction on Kaggle](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)
- **Files:** `train.csv` (103,904 rows), `test.csv` (25,976 rows)
- **Features:** 25 features covering passenger demographics, flight experience metrics (seat comfort, online booking ease, onboard services), and delay information
- **Target:** `satisfaction` — satisfied vs. neutral/dissatisfied


## Methodology

**1. Exploratory Data Analysis (EDA)**
- Examined distributions of age, flight distance, delays, and satisfaction
- Visualized satisfaction by class, type of travel, and other key features
- Identified missing values and outliers

**2. Data Preprocessing**
- Filled missing values (e.g., `Arrival Delay in Minutes`)
- Encoded categorical features: `Gender`, `Customer Type`, `Type of Travel`, `Class`
- Converted target variable to binary (1 = satisfied, 0 = neutral/dissatisfied)
- Scaled numeric features using `StandardScaler`

**3. Customer Segmentation (Clustering)**
- Applied K-Means clustering on key behavioral and satisfaction features
- Identified distinct passenger segments and visualized them to understand differing travel profiles

**4. Prediction (Classification)**
- Trained a **Random Forest Classifier** to predict passenger satisfaction

## Results

**Classification performance (test set):**
- **Accuracy: 96.4%**
- Precision, recall, and F1-score balanced across both satisfied and dissatisfied classes

**Feature importance (top drivers of satisfaction):**
| Feature | Importance |
|---|---|
| Online boarding | 16.7% |
| Inflight Wi-Fi service | 15.3% |
| Class | 11.0% |
| Type of Travel | 9.4% |
| Inflight entertainment | 5.6% |
| Seat comfort | 4.4% |

Lower-importance features included Gender and Departure Delay in Minutes. Full feature importance visualization is available in the notebook.

## Insights
- Smooth online boarding and reliable Wi-Fi service are the strongest predictors of passenger satisfaction — stronger even than delay-related metrics
- Travel class and type of travel meaningfully shape passenger expectations and reported satisfaction
- For airlines, prioritizing improvements to the boarding process, Wi-Fi, seat comfort, and entertainment is likely to yield the largest gains in overall satisfaction

## Tech Stack
Python (pandas, NumPy, matplotlib, seaborn, scikit-learn) — Random Forest (classification), K-Means (clustering), feature engineering, scaling, and encoding

## Author
Rabiya Farheen
MSc Data Science, Technical University of Braunschweig, Germany
