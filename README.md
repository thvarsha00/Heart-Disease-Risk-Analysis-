#  Heart Disease Risk Analysis (EDA Project)

##  Project Overview
Heart disease is one of the leading causes of death worldwide.  
This project performs **Exploratory Data Analysis (EDA)** on the **UCI Heart Disease dataset** to uncover patterns, identify influential risk factors, and provide insights that can form the foundation for predictive modeling.

---

##  Objectives
- Explore the dataset and summarize patient attributes.  
- Perform **Univariate, Bivariate, and Multivariate analysis** using visualization techniques.  
- Engineer meaningful features (age groups, cholesterol levels, blood pressure categories).  
- Apply **statistical tests (Chi-Square, T-Test)** to validate associations.  
- Identify the most important **risk factors for heart disease**.  

---

##  Dataset
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+disease)  
- **Rows:** 303  
- **Columns:** 14 (demographic + clinical features)  
- **Target Variable:**  
  - `0` → No heart disease  
  - `1` → Heart disease present  

---

##  Tools & Libraries
- **Python**
- **Pandas, NumPy** → Data manipulation  
- **Matplotlib, Seaborn, Plotly** → Visualizations  
- **SciPy** → Statistical testing  

---

##  EDA Workflow
1. **Initial Data Exploration**  
   - Shape, info, summary statistics, missing values.  

2. **Target Variable Analysis**  
   - Balanced dataset (≈55% diseased, 45% healthy).  
   - Visualized with bar and pie charts.  

3. **Univariate Analysis**  
   - Distribution of age, cholesterol, blood pressure, max heart rate.  
   - Boxplots to detect outliers.  

4. **Bivariate Analysis**  
   - Cholesterol vs Target  
   - Max HR vs Target  
   - Chest pain type vs Target  

5. **Multivariate Analysis**  
   - Scatterplots (Age vs Cholesterol vs Target).  
   - 3D scatter (Age, BP, Cholesterol).  
   - Correlation heatmap & Parallel Coordinates.  

6. **Feature Engineering**  
   - Age groups (20–40, 40–60, 60–80).  
   - Cholesterol levels (Normal, Borderline, High).  
   - Blood Pressure categories (Normal, Elevated, Hypertension).  
   - Heatmap of Age × Cholesterol.  

7. **Statistical Testing**  
   - **Chi-Square:** Significant association for `cp`, `exang`, `slope`, `ca`, `thal`.  
   - **T-Test:**  
     - Diseased patients → lower max HR, higher ST depression.  
     - BP & cholesterol moderately significant.  

---

##  Key Insights
- **Strong Predictors:**  
  - Low Max Heart Rate (`thalach`)  
  - High ST Depression (`oldpeak`)  
  - Chest Pain Type (asymptomatic)  
  - Exercise-Induced Angina (`exang`)  

- **Moderate Predictors:**  
  - Age (40+)  
  - Hypertension (high resting BP)  
  - High cholesterol  

- **Less Significant:**  
  - Fasting Blood Sugar (`fbs`)  
  - Resting ECG (`restecg`)  

---

##  Conclusion
- Heart disease is **multi-factorial**; no single variable determines risk.  
- A **combination of age, chest pain, BP, cholesterol, max HR, and exercise-induced angina** best explains risk.  
- Findings provide a strong foundation for **predictive modeling (Logistic Regression, Random Forest, etc.)** in future work.  

---

##  Future Work
- Build and evaluate **classification models**.  
- Apply **feature selection** and compare model performances.  
- Deploy as a **health risk prediction dashboard**.  

---

##  How to Run
1. Clone this repository:  
   ```bash
   git clone https://github.com/your-username/heart-disease-eda.git
   cd heart-disease-eda
