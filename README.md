# **Predicting Seasonal Influenza Vaccination Uptake Through  A Comparative Machine Learning Approach**


---
## **1. Project Overview & Business Problem**
## **1.1 Business Problem**
Every year, seasonal influenza causes significant mortality and economic loss due to healthcare costs and lost productivity. While vaccines are widely available, a large portion of the population remains unvaccinated. Public health organizations require a precise, data-driven method to identify which demographic and behavioral key factors highly influence an individual's decision to get vaccinated.
***
### **Objective:**
The goal of this project is to build a **predictive machine learning model** that identifies the key factors that influence whether an individual receives the seasonal flu vaccine or not. This helps healthcare providers allocate resources more efficiently and allows for targeted communication strategies that increase overall vaccination rates.
***
## **1.2 Business Understanding**
 ### ***1.2.1 Key Stakeholders:***
 1. ***Global Health Organizations (WHO / UNICEF)***
- Responsible for studying broad behavioral trends to update global policy and combat misinformation.

2. ***National & Local Health Departments (e.g., Ministry of Health):*** 
- Responsible for identifying which populations are mostly unvaccinated and use this to allocate their limited budgets to the right neighborhoods.

3. ***Public Health Marketing Teams:*** 
- To design effective awareness campaigns.

4. ***Healthcare Providers & Clinics:*** 
- They can use model's insights to improve patient-doctor communication especially to the unlikely-to-vaccinate" patients.

5. ***Pharmaceutical Supply Chain Managers:*** 
- They derive vaccination probabilities to predict regional vaccine demand, preventing both shortages and medicine waste.

6. ***Health Insurance Companies:***
- They benefit from the reduced clinical costs associated with influenza due to higher community immunization rates.
***
### ***1.2.2 Key Goals***
1. ***Classification Model:*** Build a classification model with an AUC score above 0.75 that distinguishes between vaccinated and unvaccinated individuals, allowing for more effective health intervention strategies.


2. ***Feature Analysis Report:*** Identify the top 5 features that highly influence vaccination behavior.


3. ***Minimize the Generalization Gap:*** This is to ensure the model performs reliably on real-world, unseen survey data.
***
## **2. Data Understanding**
 ### ***2.1 Data Source:***
The data for this project is sourced from the `National 2009 H1N1 Flu Survey (NHFS)`. While the survey was conducted during the H1N1 pandemic, it collected extensive data on Seasonal Flu vaccination patterns, which serves as our target variable.

This dataset is ideal for behavioral insights because it captures personal opinions and daily habits.
***
 The `training_set_features` & `training_set_labels` datasets were used for this project.
 ### ***2.2 Dataset Characteristics:***
 - **Total Records:** We have 26,707 survey responses.


- **Feature Set:** 37 predictor variables, including:

  **1. Behavioral:** (e.g., behavioral_face_mask, behavioral_wash_hands).

  **2. Opinions:** (e.g., opinion_seas_vacc_effective, opinion_seas_sick_from_vacc).

  **3. Demographics:** (e.g., age_group, education, race, income_poverty).

  **4. Health History:** (e.g., doctor_recc_seasonal, chronic_med_condition).
 ### **2.3 Target Variable Analysis:** 
The target variable is **seasonal_vaccine:**

**0:** Did not receive the seasonal flu vaccine.

**1:** Received the seasonal flu vaccine.
***
## **Tools & Libraries**

- **Python 3.10+**  
- **Pandas** – Data manipulation  
- **NumPy** – Numerical computations  
- **Seaborn & Matplotlib** – Data visualization  
- **Scikit-learn** – Machine learning models & evaluation metrics
- **StatsModel** - Multicollinearity testing
***
## Methodology 
### **1. Data Preparation and Pre-Processing**
- Check for duplicates
- Drop irrelevant columns
- Apply train-test split
- Detect and deal with missing values
- Convert categorical data to numeric format through one-hot encoding
- Normalize our numeric data
- Check for and remove multicollinearity (correlated predictors)
  ***
### **2. Modelling**
- Linear Regression
- Random Forest Classification Regression
***
### **3.Model Evaluation**
- Accuracy Score
- Confusion Matrix
- Classification Report
- ROC AUC Score
***
### **4. Feature Importance**  
   - Identify the most influential features that highly influnce vaccination behaviour
***
### **5. Key Results**
**Best Model:** Random Forest Classification Model

**Primary Metric (ROC AUC):*** 0.838 (Exceeding the 0.75 benchmark)

**Baseline Model (Logistic Regression):** 0.819 AUC
***
<img width="850" height="552" alt="image" src="https://github.com/user-attachments/assets/75e7ae28-9e14-470a-b644-09ad8b9ee8bf" />

***

### **6. Recommendations**

1.  `doctor_recc_seasonal`:
- Finding: A direct recommendation from a healthcare provider is the strongest predictor of whether a patient will get vaccinated.

- Recommendation: Fund programs that encourage physicians to speak up. This can be done by providing them with toolkits to ensure they ask every patient about their flu shot during routine visits.

2. `opinion_seas_vacc_effective`:
- Finding: People believing in the effectiveness of the vaccine is more important than their fear of side effects or the cost of the shot.

- Recommendation: Marketing materials should move away from just saying "It's Safe" and focus more on "How Well It Works." Use data-driven storytelling to show how the vaccine prevents hospitalizations in the local community.

3. `opinion_seas_risk`:
- Finding: Individuals who perceive themselves as "low risk" for getting influenza are significantly less likely to vaccinate, regardless of their access to healthcare.

- Recommendation: Use demographic data to identify low-perception groups (likely younger adults) and create social media campaigns that highlight how the flu can impact even healthy individuals or their vulnerable family members.

<img width="1096" height="550" alt="image" src="https://github.com/user-attachments/assets/e55bcd3d-2462-4a87-9d35-f6e4040ef327" />


