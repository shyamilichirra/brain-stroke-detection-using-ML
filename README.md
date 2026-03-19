<div align="center">
  <img src="https://capsule-render.vercel.app/render?type=waving&color=0099ff&height=200&section=header&text=Brain%20Stroke%20Prediction&fontSize=50" width="100%" />

  <p>
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
    <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
    <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white" />
  </p>
  
  <h4>A Machine Learning approach to early stroke detection and risk assessment.</h4>
</div>

---

## 📖 Introduction
A stroke occurs when the blood supply to part of your brain is interrupted or reduced, preventing brain tissue from getting oxygen and nutrients. This project implements various Machine Learning models to predict the probability of a stroke based on parameters like age, BMI, heart disease, and smoking status.



[Image of brain stroke risk factors and symptoms]


## 📊 Dataset
The dataset used for this project is the **Stroke Prediction Dataset** from Kaggle.
* **Link:** [Kaggle Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
* **Attributes:** Gender, Age, Hypertension, Heart Disease, Ever Married, Work Type, Residence Type, Glucose Level, BMI, Smoking Status.

---

## 🛠️ Implementation Details

### 1. Data Preprocessing
* **Feature Selection:** Dropped the `id` column as it had no predictive power.
* **Handling Nulls:** Imputed missing values in the `BMI` column using the **Median** because the data was skewed.
* **Class Imbalance:** Since the dataset was highly imbalanced (fewer stroke cases), we applied **Random Oversampling** to balance the classes.
* **Encoding:** Converted categorical data into numerical format using **Dummy Encoding**.

### 2. Exploratory Data Analysis (EDA)
We utilized `Matplotlib` and `Seaborn` to visualize:
* Target attribute distribution (Pie Charts).
* Correlation between features (Heatmaps).
* Attribute trends (Histograms).



---

## 🚀 Model Performance
The models were trained using an 80-20 split and evaluated based on accuracy and the ROC-AUC score.

| Algorithm | Accuracy |
| :--- | :---: |
| **Random Forest** | **99.48%** |
| Decision Tree | 97.89% |
| XG-Boost | 97.48% |
| KNN | 97.22% |
| Logistic Regression | 76.34% |

**Final Selection:** **Random Forest** was chosen as the primary model. To ensure it wasn't overfitting, we performed **K-Fold Cross-Validation (20 splits)**, which yielded a solid **95.01%** accuracy.

