# Analysis.ipynb  

This notebook contains the data preprocessing, exploratory data analysis (EDA), and machine learning implementation steps for the **Crime Type and Location Prediction** project.  

---

## **Table of Contents**  
1. [Introduction](#introduction)  
2. [Dataset Overview](#dataset-overview)  
3. [Data Preprocessing](#data-preprocessing)  
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
5. [Feature Engineering](#feature-engineering)  
6. [Model Training and Evaluation](#model-training-and-evaluation)  
7. [Results](#results)  

---

### **Introduction**  
This notebook demonstrates how crime data is processed, analyzed, and used to train machine learning models for:  
- **Crime Type Classification** (e.g., identifying the nature of a crime based on associated features).  
- **Location Prediction** (e.g., predicting a crime's geographic coordinates and area).  

---

### **Dataset Overview**  
The dataset contains 933,425 records with the following key attributes:  
- **Target Variables**:  
  - *Crime Type* (`Crm Cd Desc`)  
  - *Location* (`LAT`, `LON`, and `AREA`)  
- **Features**: Demographics, crime location details, and incident codes.  

---

### **Data Preprocessing**  
Steps performed:  
1. **Handling Missing Values**: Dropped rows with missing target values.  
2. **Encoding Categorical Features**:  
   - Applied Label Encoding for categorical data such as `Vict Sex` and `AREA NAME`.  
3. **Feature Scaling**: Standardized numerical features like `Vict Age`, `LAT`, and `LON`.  

---

### **Exploratory Data Analysis (EDA)**  
1. **Distribution Analysis**:  
   - Visualized the frequency of different crime types.  
   - Analyzed victim demographics by age and sex.  

2. **Geographic Insights**:  
   - Mapped crime density using latitude and longitude coordinates.  

---

### **Feature Engineering**  
Generated meaningful inputs by:  
- Combining categorical and numerical features for model training.  
- Removing irrelevant columns such as `DR_NO` that don't add predictive value.  

---

### **Model Training and Evaluation**  
Implemented the following models:  
1. **Logistic Regression**: Used for crime type classification.  
2. **Random Forest Classifier**: Applied for classification and prediction tasks.

#### **Metrics Used**:  
- Accuracy  
- Precision, Recall, F1-Score  
- Confusion Matrix  

---

### **Results**  
- **Crime Type Classification**:  
  - Logistic Regression achieved an accuracy of 78.6%.  
  - Random Forest outperformed Logistic Regression with an accuracy of 84.2%.  

- **Location Prediction**:  
  - Decision Tree provided interpretable results, focusing on geographical attributes like `LAT`, `LON`, and `AREA`.  
  - Random Forest showed robustness across multi-class predictions.  

---

### **Usage**  
To execute this notebook:  
1. Clone the repository:  
   ```bash  
   git clone <repository-link>  
   cd <repository-name>  
   ```  
2. Install required libraries:  
   ```bash  
   pip install -r requirements.txt  
   ```  
3. Run the notebook:  
   ```bash  
   jupyter notebook analysis.ipynb  
   ```  
