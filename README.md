# Obesity-Classification-ML
Predicting obesity levels using machine learning technique(logistic regression)

It includes preprocessing (encoding & scaling), model training, and evaluation using metrics like accuracy, confusion matrix, and classification report.

---

Dataset
Source: [UCI Machine Learning Repository – Estimation of obesity levels](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition)

Sample: 2111 
Target classes (7 total):
  - Insufficient_Weight/Underweight
  - Normal_Weight
  - Overweight_Level_I
  - Overweight_Level_II
  - Obesity_Type_I
  - Obesity_Type_II
  - Obesity_Type_III

---

 Features Used

-Numerical (scaled):  
  `Age`, `Height`, `Weight`, `FCVC`, `NCP`, `CH2O`, `FAF`, `TUE`
  
- Categorical (encoded):  
  `Gender`, `family_history_with_overweight`, `FAVC`, `CAEC`, `SMOKE`, `SCC`, `CALC`, `MTRANS`

---

Feature Descriptions

| Column                          | Description                                                                  |
|----------------------------------|-----------------------------------------------------------------------------|
| `Age`                            | Age of the individual                                                       |
| `Height`                         | Height of the individual (in meters)                                        |
| `Weight`                         | Weight of the individual                                                    |
| `family_history_with_overweight`| Whether the individual has overweight issues in their family (Yes/No)        |
| `FAVC`                           | Frequent consumption of high-calorie food (Yes/No)                          |
| `FCVC`                           | Frequency of vegetable consumption (1–3 scale)                              |
| `NCP`                            | Number of main meals per day (usually 1–4)                                  | 
| `CAEC`                           | Consumption between meals (No, Sometimes, Frequently, Always)               |
| `SMOKE`                          | Whether the individual smokes (Yes/No)                                      |
| `CH2O`                           | Daily water intake (1–3 liters approx.)                                     |
| `SCC`                            | If the individual monitors caloric intake (Yes/No)                          |
| `FAF`                            | Frequency of physical activity (hours/week)                                 |
| `TUE`                            | Time spent using technology (hours/day)                                     |
| `CALC`                           | Frequency of alcohol consumption (No, Sometimes, Frequently, Always)        |
| `MTRANS`                         | Mode of transportation (Walking, Bike, Public Transport, Automobile, etc.)  |

---

 Model & Preprocessing

- Model Used: Logistic Regression  
- Preprocessing:
  - Categorical encoding (ordinal and label)
  - Feature scaling using `StandardScaler` (only for selected numeric columns)
  - Train-test split with `stratify=y` (to preserve class balance)

---

 Results

- Accuracy: ~87.2%
- Evaluation:
  - Confusion Matrix  
  - Classification Report (Precision, Recall, F1-score)  
  - Balanced prediction across all 7 classes

