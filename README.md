# heart-disease-risk-classification
End-to-end machine learning project on the UCI Heart Disease dataset, applying data preprocessing, feature selection, and logistic regression to predict heart disease presence with strong classification performance.
# UCI Heart Disease Prediction

## 📌 Project Overview

This project builds a **binary classification model** to predict the **presence of heart disease** using clinical and demographic features from the **UCI Heart Disease dataset**. The goal is to demonstrate an end-to-end data science workflow, from data understanding and preprocessing to modeling and evaluation.

Heart disease severity in the original dataset is represented on a scale from **0 to 4**. For this project, the task is reframed as a **binary problem**:

* **0**: No heart disease
* **1**: Presence of heart disease (original values 1–4)

This framing reflects a common real-world use case: **risk detection rather than severity diagnosis**.

---

## 📊 Dataset

* **Source:** UCI Machine Learning Repository – Heart Disease Dataset
* **Observations:** 920 patients
* **Features:** 16 clinical and demographic variables
* **Target variable:** `num` (heart disease severity)

### Target Distribution

* No disease (0): 411
* Disease present (1–4): 509

The dataset is moderately imbalanced toward positive (disease) cases.

---

## 🧹 Data Preparation

* No missing values detected
* No rows removed during outlier analysis
* Identifier column (`id`) dropped to prevent data leakage
* Categorical variables encoded
* Numerical variables prepared for modeling

---

## 🔧 Feature Insights

Correlation analysis highlighted several features strongly associated with heart disease presence, including:

* Chest pain type (`cp`)
* Maximum heart rate achieved (`thalch`)
* Exercise-induced angina (`exang`)
* ST depression (`oldpeak`)
* Sex

These features align with known clinical risk indicators.

---

## 🤖 Modeling Approach

* **Problem type:** Binary classification
* **Train–test split:** 80% training / 20% testing
* **Model:** Logistic Regression (`max_iter = 1000`)

Logistic Regression was selected for its interpretability and suitability for clinical risk prediction tasks.

---

## 📈 Model Performance

On the test set, the model achieved:

* **Accuracy:** 1.00
* **Precision:** 1.00
* **Recall:** 1.00
* **F1-score:** 1.00
* **ROC-AUC:** 1.00

These results indicate perfect separation on the test data.

⚠️ **Note:** Such performance suggests potential overfitting or strong dataset-specific patterns. External validation on independent data is recommended before real-world use.

---

## 🧠 Key Takeaways

* Clinical features can strongly predict heart disease presence
* Logistic Regression provides both high performance and interpretability
* Proper problem framing (binary vs. severity) is critical in healthcare modeling

---

## ⚠️ Limitations

* Results are based on a single dataset
* No external validation performed
* Not intended for clinical diagnosis

---

## 📁 Repository Structure

```
├── notebooks/        # Jupyter notebooks with analysis and modeling
├── data/             # Dataset files (if included)
├── figures/          # Plots and visualizations
├── README.md         # Project documentation
```

---

## 🚀 Next Steps

* Validate model on an external heart disease dataset
* Compare with tree-based models (Random Forest, XGBoost)
* Explore multiclass severity prediction

---

## 📜 Disclaimer

This project is for **educational and portfolio purposes only** and should not be used for medical decision-making.
