# Explainable Vaccine Hesitancy Prediction System with XAI Fusion

## 🔍 Overview

Vaccine hesitancy remains a critical challenge in public health, particularly among healthcare workers where informed and evidence-based decisions are essential. While machine learning models can achieve high predictive accuracy, they often lack transparency, limiting their usefulness in real-world decision-making.

This project presents an explainable machine learning framework that integrates predictive modeling with advanced explainability techniques to identify and interpret the key factors influencing COVID-19 vaccine hesitancy among Malaysian healthcare workers.

## 🎯 Problem Statement

Traditional machine learning models prioritize predictive performance but provide limited insight into why a prediction is made. In high-stakes domains such as healthcare and policy-making, interpretability is essential for trust, accountability, and actionable insights.

This project addresses:

* Accurate prediction of vaccine hesitancy
* Transparent and interpretable model decisions
* Identification of key behavioral and perception-based factors

## 🧠 Objectives

* Develop predictive models for vaccine hesitancy (Primary and Booster doses)
* Apply feature selection and aggregation strategies
* Generate both global and local explanations using XAI techniques
* Improve explanation consistency through fusion of SHAP and LIME
* Identify significant features aligned with behavioral frameworks


## 📊 Dataset

The dataset consists of survey responses from Malaysian healthcare workers, capturing demographic, behavioral, and perception-based variables related to COVID-19 vaccination.

### Feature Categories

* Demographics (age, ethnicity, years of employment)
* Vaccine perception (protection, side effects, clinical trial confidence)
* Beliefs and attitudes (mandatory vaccination, alternative medicine)
* Trust and misinformation factors

## ⚙️ Methodology

### 1. Data Preprocessing

* Handling missing values
* Encoding categorical variables
* Normalization of features

### 2. Feature Selection & Aggregation

**Feature selection methods:**

* ANOVA
* Chi-Square
* Information Gain

**Feature aggregation:**

* MVH (Mean Vaccine Hesitancy)
* MVP (Mean Vaccine Perception)
* MBA (Mean Booster Attitude)

These transformations improve model interpretability and reduce dimensionality.

### 3. Model Development

The following machine learning models were evaluated:

* K-Nearest Neighbors (KNN)
* Decision Tree (DT)
* Naive Bayes (GNB, MNB)
* Support Vector Machine (SVM)
* Random Forest (RF)
* Ensemble models (Bagging, Boosting, XGBoost)

The **Linear SVM model** achieved the best performance and was selected for further analysis.

### 4. Explainable AI Framework

#### 🔹 Global Explanation (SHAP)

* Identifies overall feature importance
* Provides global ranking of influential factors

#### 🔹 Local Explanation

* SHAP (local): instance-level contribution
* LIME: alternative local explanation

#### 🔹 XAI Fusion Strategy

To improve explanation consistency:

* Combined SHAP and LIME outputs
* Evaluated agreement using:

  * Kendall Tau
  * Rank-Biased Overlap (RBO)
  * Recall@K

This approach enhances robustness and reliability of explanations.

### 5. Experimental Design

The experiments were conducted under multiple configurations:

* Primary dose dataset
* Booster dose dataset
* All features vs selected features vs aggregated features

## 📈 Results

* The **Linear SVM model** achieved the best predictive performance
* The fusion of SHAP and LIME improved explanation consistency
* Consistent key features identified across experiments:

  * Clinical Trial Confidence
  * Vaccine Protection Perception
  * Mandatory Belief
  * Side Effect Confidence
  * Alternative Medicine Belief

These findings align with:

* Health Belief Model (HBM)
* Theory of Planned Behavior (TPB)

## 🧩 Key Contributions

* Developed an explainable ML framework integrating global and local explanations
* Proposed a fusion-based XAI approach for improved consistency
* Demonstrated the importance of interpretability in healthcare analytics
* Provided actionable insights into vaccine hesitancy factors

## 🛠️ Tech Stack

* Python
* scikit-learn
* SHAP
* LIME
* Pandas
* NumPy
* Matplotlib
* Seaborn

## 📂 Project Structure

```text
vaccine-hesitancy-xai/
│
├── data/              # Sample or processed data (not full dataset)
├── notebooks/         # Jupyter notebooks for experiments
├── src/               # Core scripts (training, preprocessing)
├── model/             # Saved trained models
├── xai/               # SHAP & LIME explainability scripts
├── results/           # Visualizations and evaluation outputs
├── requirements.txt
└── README.md
```

## 🔒 Data Availability

The dataset used in this project contains sensitive survey data from Malaysian healthcare workers and cannot be publicly shared due to privacy and ethical considerations.

To reproduce this project, users may:

* Use a similar public dataset
* Simulate data with similar structure
* Follow the provided methodology and pipeline

## 🚀 Future Work

* Deploy as an explainable decision-support system
* Develop an interactive dashboard for visualization
* Extend the framework to other domains (e.g., finance, risk modeling)
* Integrate additional explainability techniques

## 📌 Conclusion

This project demonstrates that combining machine learning performance with explainability is essential for high-stakes domains. The proposed XAI fusion framework improves the consistency and reliability of explanations, making it suitable for real-world decision-making in healthcare and beyond.

## 👤 Author

Developed as part of a Master's research project in Explainable Machine Learning.
