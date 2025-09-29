# Healthquare (Health Square): Personal Health Coaching Service

### Background

In modern society, health is often overlooked as a key asset despite its importance for overall well-being. ***Healthquare*** was designed to address this gap by helping users measure and improve their health through lifestyle data such as diet, sleep, exercise, and alcohol consumption. The service provides personalized health scores, peer comparisons, and improvement tips, all within a single, engaging platform.

---

### Project Objective

* Predict user's health scores based on lifestyle patterns
* Classify user health status using machine learning models, and provide results and improvement tips via a web service

### Dataset and Key Variables

* **Source:** Kaggle - Synthetic Health and Lifestyle Data
* **URL:** [https://www.kaggle.com/datasets/pratikyuvrajchougule/health-and-lifestyle-data-for-regression](https://www.kaggle.com/datasets/pratikyuvrajchougule/health-and-lifestyle-data-for-regression)
* **Key Variables:**

  * Features: `Age`, `BMI`, `Exercise_Frequency`, `Diet_Quality`, `Sleep_Hours`, `Smoking_Status`, `Alcohol_Consumption`
  * Target: `Health_Score`
  * New Target: `Health Class`

### Workload
1. **Project Planning:** Topic selection, data collection
2. **Data Analysis:** Data preprocessing, visualization
3. **Model Building:** Machine leartning training and evaluation
4. **Web Service**

### Main Tasks

> **Responsible for Data Analysis and Machine Learning**
 
#### ① Data EDA

* No missing values
* Outlier existing
* Low correlation level among features
* Linearly related to target
* Largely different scales of features
* Unreasonable and biased target

#### ② Data Preprocessing and Feature Engineering

* Outlier removal
* Normalization with Standard Scaler
* Target Engineering 
  * Define an optimal range for each health factor (e.g., BMI, sleep, exercise) on a 10 point scale, deducting points when values deviated from the healthy range
  * Aggregate these scores to create a new target variable of `New Health Score`
  * Produce the final target of `Health Class` converting the continuous score into categorical health levels by 10-point intervals

#### ③ Model Design and Evaluation

* Apply and compare multiple classification models
* Select the final model: **`Logistic Regression`**
  * Normally distributed variables
  * Independent among variables
  * Features linearly correlated with target

---

### Web Service Demonstration
