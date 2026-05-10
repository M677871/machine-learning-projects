# Applied Machine Learning Portfolio 

This repository documents my practical journey through the theoretical concepts covered in **CSIS 260: Introduction to Artificial Intelligence** at the University of Balamand (Spring 2026). It contains end-to-end applications of techniques learned from Aurélien Géron's *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow*.

---

## 🏆 Highlight Project: Cervical Cancer Risk Prediction
**Location:** `cervical_cancer_risk_analysis/`  
**Focus:** Imbalanced Binary Classification, PCA, Hyperparameter Tuning

This project represents the culmination of a full pipeline, transitioning from raw exploratory data analysis to a robust, fine-tuned classification system aimed at medical diagnostics. Forecasting biopsy outcomes based on demographic and lifestyle risk factors is highly complex due to the severe imbalance of the minority class (positive cancer cases).

### Key Learnings & Implementations
Over the two phases of this project, I solidified my understanding of the end-to-end Machine Learning ecosystem:

1. **Exploratory Data Analysis (EDA) & Data Preparation**
   Real-world data is heavily flawed. I learned to systematically handle missing values, clean anomalies, and construct insightful visualizations mapping correlations between the top identified risk factors and target outcomes.
2. **Preprocessing & Regularization Pipelines**
   I designed rigorous preprocessing pipelines, utilizing Feature Selection, One-Hot Encoding, and Standard Scaling. Learning how to properly apply **L1/L2 Regularization** was crucial in preventing my models from overfitting noise in the training set.
3. **Addressing Class Imbalance**
   In a medical context, missing a positive diagnosis (False Negative) is dangerous. I explored **SMOTE** (Synthetic Minority Over-sampling Technique) to ensure the models accurately recognized minority cases without data leakage, anchoring it exclusively within training subgroups.
4. **Model Selection & Hyperparameter Tuning**
   I trained and evaluated multiple core algorithms:
   * **Logistic Regression:** Used as a strong, interpretable baseline.
   * **Support Vector Machines (SVM):** Configured with linear and RBF kernels.
   * **Decision Trees & Random Forests:** Leveraged for feature importance and ensemble prediction.
   Instead of settling for default definitions, I successfully applied **Grid Search** and **Random Search** to optimize hyperparameter settings across the board.
5. **Dimensionality Reduction via PCA**
   I implemented **Principal Component Analysis (PCA)** to condense the feature space. Investigating the variance explained by the components helped me compare the performance and training efficiency of algorithms fueled by raw features against PCA-reduced variables.
6. **Advanced Medical Evaluation Metrics**
   Relying on raw accuracy is deceiving for imbalanced sets. I evaluated models purely on **Precision, Recall (Sensitivity), F1-Score**, dynamically adjusting probability thresholds using ROC and PR-AUC curves to identify the most stable diagnostic cutoffs.

*All findings, comparative analysis across models (with and without PCA), and final conclusions exist comprehensively within the documented notebook report.*

---

## 📐 Foundations & Algorithms

### 1. MNIST Classification
**Location:** `classification/`  
**Focus:** Multi-Class Image Classification and Error Analysis

An exploration into computer vision using the famous MNIST digits dataset. This project established my understanding of:
* Transforming binary classifiers into multi-class and multi-label predictors.
* Measuring classification efficacy objectively using Confusion Matrices.
* Performance indicators beyond accuracy (Precision/Recall tradeoffs).

### 2. Applied Linear Regression
**Location:** `linear regression/`  
**Focus:** Error Minimization & Gradient Descent

These introductory modules map continuous variables and tackle statistical dependencies through foundational univariate models:
* **Study Hours vs. Grades:** Mapping academic performance variables.
* **Years of Experience vs. Salary:** Analyzing simple financial curves.

---

## 🛠️ Technology Stack
* **Language:** Python
* **Data Processing:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (Algorithms, PCA, GridSearch, Metrics)
* **Sampling:** Imbalanced-Learn (SMOTE)
* **Visualization:** Matplotlib, Seaborn

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/repo-name.git
   ```
2. **Open the Notebooks:** Start your environment (Jupyter Lab/VS Code). Datasets are bundled locally in each nested folder; no external downloads are needed.
3. **Run sequentially:** The notebooks execute top-to-bottom.
