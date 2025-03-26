# Cancer Genomics and Personalized Medicine

## Project Overview

This project focuses on leveraging **machine learning** techniques to predict cancer treatment outcomes using **genomic data**. By analyzing real-world clinical and genomic data from **The Cancer Genome Atlas (TCGA)**, the project aims to assist in **personalized treatment strategies** - a crucial step toward precision medicine.

> **Dataset:** [TCGA (Breast Cancer subset)](https://portal.gdc.cancer.gov/)
> **Institution:** School of Engineering & Applied Science, George Washington University  

---

## Objectives

- Predict **vital status** (alive/dead) of cancer patients.
- Predict **AJCC pathologic stage** of cancer.
- Predict **treatment type** (radiation, pharmaceutical, etc.).
- Build a **MultiOutputClassifier** to address multiple outcomes simultaneously.

---

## Methodology

### Data Cleaning & Preprocessing
- Removed columns with >30% missing data
- Replaced `'--'`, `'unknown'`, `'not reported'` with NaN
- Dropped duplicates
- Handled outliers using Z-scores

### Feature Engineering
- **Label Encoding** for binary/categorical columns
- **Ordinal Encoding** for cancer stages
- **One-Hot Encoding** for non-ordered categorical features

### Exploratory Data Analysis (EDA)
- Descriptive statistics and distribution plots
- Correlation heatmaps
- Target variable visualizations

### Modeling
- Used **MultiOutputClassifier** with different base classifiers:
  - Naive Bayes
  - Logistic Regression
  - Random Forest
  - **Decision Tree (selected model)**
- Evaluated with accuracy, precision, recall, ROC AUC

---

## Results

| Target Column         | Selected Model | Metrics (Accuracy / AUC etc.) |
|----------------------|----------------|-------------------------------|
| `vital_status`       | Decision Tree  | Best performance           |
| `ajcc_pathologic_stage` | Decision Tree  | Best performance           |
| `treatment_type`     | Decision Tree  | Best performance           |

---

## Future Work

- Model hyperparameter tuning
- Integration with clinical decision systems
- Inclusion of other cancer types from TCGA
- Feature explainability using SHAP or LIME

---

## Installation

```bash
git clone https://github.com/ishapaliwal/cancer-genomics-personalized-medicine.git
cd cancer-genomics-personalized-medicine
pip install -r requirements.txt
```

---

## References
- [The Cancer Genome Atlas (TCGA)](https://portal.gdc.cancer.gov/)
- Deep Learning for Drug Response Prediction [Frontiers in Medicine, 2023](https://www.frontiersin.org/journals/medicine/articles/10.3389/fmed.2023.1086097/full)
- Explainable Deep Learning in Oncology [Genome Medicine, 2021](https://genomemedicine.biomedcentral.com/articles/10.1186/s13073-021-00968-x)

---

## Contact
For any queries or collaboration requests, please contact me at isha.paliwal11@gmail.com.
