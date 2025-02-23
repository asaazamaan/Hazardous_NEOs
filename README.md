# **Predicting Hazardous NEOs (Near-Earth Objects)**  
A Machine Learning Project for Identifying Potentially Dangerous Asteroids  

---

## **Overview**
This project aims to predict whether a **Near-Earth Object (NEO)** is hazardous based on real-world data collected by **NASA (1910-2024)**. The dataset contains **338,199 records**, where each record represents an asteroid tracked for its proximity to Earth. Some objects are classified as *hazardous*, indicating potential risk to our planet.
---

## **Project Workflow**
 **Data Importing and cleaning** →**Exploratory Data Analysis (EDA)** →**Data Preprocessing** →**Model Training and Evaluation**

---

## **Features & Implementation**
### **1️⃣ Data Cleaning & Preprocessing**
✔️ **Handled missing values** by removing incomplete records  
✔️ **Dropped unnecessary columns** (e.g., `neo_id`, `name`, `orbiting_body`)  
✔️ **Removed duplicate rows**  
✔️ **Checked class imbalance** (Found that hazardous asteroids are underrepresented)  
✔️ **Feature Scaling** using `StandardScaler`  

### **2️⃣ Exploratory Data Analysis (EDA)**
✔️ **Visualized feature distributions** using histograms & pair plots  
✔️ **Plotted correlations** between features using heatmaps  


### **3️⃣ Feature Engineering**
✔️ Created new features like:  
   - `size_ratio` → ratio between max & min estimated diameter  
   - `velocity_size_ratio` → relative velocity divided by max estimated diameter  
   - `inv_miss_distance` → inverse of miss distance  
✔️ **Removed less important features** based on feature importance analysis  

### **4️⃣ Handling Imbalanced Classes**
✔️ Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset  
✔️ Ensured that SMOTE was applied **only on training data**  

### **5️⃣ Model Training & Evaluation**
We trained and evaluated **five different models** using both **Stratified K-Fold Cross-Validation** and **Train-Test Split**:  

📌 **Models Used:**  
✔️ **Logistic Regression**  
✔️ **Decision Tree Classifier**  
✔️ **Random Forest Classifier**  
✔️ **XGBoost Classifier**  
✔️ **CatBoost Classifier**  

📌 **Evaluation Metrics:**  
✔️ **Accuracy**  
✔️ **Precision**  
✔️ **Recall**  
✔️ **F1-Score**  
✔️ **AUC-ROC Curve**  

---

## **Key Insights from Model Performance**
📌 **Best Model Selected:** **Random Forest Classifier**  
✔️ **Achieved the highest AUC-ROC & F1-score**, making it the most reliable for detecting hazardous asteroids.  

✔️ **Logistic Regression & Decision Tree struggled** with imbalanced data despite SMOTE.  
✔️ **XGBoost & CatBoost performed well**, but **Random Forest outperformed them** in precision and recall balance.  

---

## **6️⃣ Feature Importance Analysis**
✔️ **Extracted feature importance from Random Forest**  
✔️ **Visualized the most critical features** contributing to model predictions  

📌 **Top Features based on the best model (Random Forest):**  
1. **Estimated Diameter (Max)**   
2. **Absolute Magnitude**  
3. **magnitude_size_ratio**  
4. **velocity_size_ratio**  
5. **Relative Velocity**  

---

## **Technologies Used**
✔️ Python  
✔️ Pandas  
✔️ NumPy  
✔️ Matplotlib & Seaborn  
✔️ Scikit-Learn  
✔️ Imbalanced-learn (SMOTE)  
✔️ XGBoost & CatBoost  

---

## **Installation & Usage**
### **Clone this repository**
```bash
git clone https:  https://github.com/asaazamaan/Hazardous_NEOs.git
cd Hazardous_NEOs
```

---

## **Acknowledgments**
✔️ **Dataset sourced from [Kaggle: NASA NEO Dataset](https://www.kaggle.com/datasets/ivansher/nasa-nearest-earth-objects-1910-2024)**  
✔️ **Developed as part of the MLSC Data Science & Machine Learning Course Graduation Project**  

---
