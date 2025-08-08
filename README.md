# 🎯 Student Depression Prediction – Machine Learning Project  

## 📌 Project Description  
This project aims to **build predictive models to detect the likelihood of students suffering from depression** and identify the most influential factors using machine learning techniques.  

With the increasing pressures of study and work, along with limited rest periods, students are exposed to chronic stress that may lead to depression. This project helps in **data analysis, selecting the most important features, and testing multiple algorithms** to choose the most accurate and suitable model.  

---

## 📂 Dataset Used  
- **Source**: Kaggle – *Student Depression Dataset*  
- **Records before preprocessing**: 27,901  
- **Number of columns**: 18 (10 numerical, 8 categorical)  
- **Example columns**:  
  - Age, Gender, Academic Pressure, CGPA, Sleep Duration, Financial Stress, Suicidal Thoughts, Depression_Status  
- **Format**: CSV  

---

## 🛠️ Data Preprocessing  
1. **Handling missing values**: Filled missing values in the *Financial Stress* column with the mean.  
2. **Removing irrelevant features**: ID, City, Work Pressure, Job Satisfaction.  
3. **Outlier handling**: Analyzed and kept them as they had minimal effect.  
4. **Categorical encoding**:  
   - Yes/No → 0/1  
   - One-Hot Encoding (Gender)  
   - Binary Encoding (Profession, Degree)  
   - Label Encoding (Dietary Habits)  
5. **Balancing the dataset**: Used **SMOTE** oversampling to achieve a 50/50 class distribution.  

---

## 📊 Data Visualization  
- Gender distribution and depression cases by gender.  
- Distribution of numerical features (e.g., Academic Pressure, Sleep Duration, CGPA).  
- **KDE Plots** showing how higher values in certain features (e.g., Academic Pressure, Financial Stress, Suicidal Thoughts) correlate with depression.  

---

## 🔍 Feature Selection  
Three techniques were tested:  
- **Correlation Analysis** → identified 7 strong features.  
- **Mutual Information (MI)** → optimal performance achieved with 9 features.  
- **Recursive Feature Elimination (RFE)** → matched MI results and was chosen for its efficiency.  

---

## 🤖 Algorithms Applied  
- **SVM (Support Vector Machine)** – Accuracy: 85%  
- **KNN (k=7)** – Accuracy: 83%  
- **Decision Tree** – Accuracy: 80%  
- **Random Forest** – **Best** with 86% accuracy and 0.86 recall for both classes.  

---

## 🏆 Final Outcome  
- **Best model**: Random Forest  
- **Reason for selection**: Highest recall (important in medical datasets to reduce false negatives) with high accuracy and stable performance.  
- **Note on accuracy**: The models did not achieve accuracy in the 90%+ range due to the complexity and variability of the dataset. Mental health data is inherently challenging to predict with extremely high accuracy without risking overfitting, given the intertwined and non-linear nature of contributing factors.  
