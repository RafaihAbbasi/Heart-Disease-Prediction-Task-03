# 🫀 Task 3: Heart Disease Prediction (Binary Classification)

## 📌 Task Objective
The objective of this task is to design and evaluate a diagnostic classification pipeline capable of predicting whether a patient is at risk of heart disease based on clinical health metrics. This project applies binary classification techniques, handling real-world health data containing missing parameters and mixed feature types.

## datasets Used
* **Dataset:** Heart Disease UCI Dataset (`heart_disease_uci.csv`)
* **Data Scale:** 920 patients, 16 baseline features pre-encoding.

## 🛠️ Data Preprocessing & Exploratory Analysis
1. **Data Cleaning:** Extracted redundant index identifiers and imputed missing numeric metrics with column medians. Categorical missing values were filled utilizing their statistical modes.
2. **Feature Engineering:** Consolidated multi-class diagnostic states into a binary target framework (`0` for No Disease, `1` for Heart Disease).
3. **Encoding:** Converted categorical text variables (such as chest pain type and thalassemia traits) into model-readable numerical structures using One-Hot Encoding, resulting in 22 total features.
4. **Visualizations Implemented:** * **Histograms:** To observe underlying patient age distribution peaks.
   * **Boxplots:** To isolate extreme statistical outliers within resting blood pressure metrics.
   * **Bar Plots:** To verify overall dataset class balance between positive and negative risk targets.

## 🤖 Models Applied
The preprocessed training data was split into an **80% training set** and a **20% testing set** to benchmark two distinct classification strategies:
* **Logistic Regression** (Linear parametric classification)
* **Decision Tree Classifier** (Non-parametric tree-based splitting)

## 📈 Key Results & Findings

### 1. Performance Metrics
Both models demonstrated high generalization capabilities on unseen testing variables:
* **Logistic Regression Accuracy:** `82.61%` (Top Performing Model)
* **Decision Tree Accuracy:** `82.07%`

### 2. Evaluation Artifacts Included
* **Confusion Matrices:** Plotted via Seaborn heatmaps to track and evaluate exact True Positives, True Negatives, False Positives, and False Negatives.
* **ROC-AUC Curves:** Assessed true positive rate behaviors across shifting decision thresholds to mathematically verify baseline model separation capacities.

### 3. Clinical Feature Importance
By pulling structural feature importance metrics directly from the trained Decision Tree model, the top critical indicators dictating heart disease risks were identified as:
1. **`cp_painless` (Asymptomatic Chest Pain):** Emerged as the strongest predictor of underlying heart conditions.
2. **`exang_true` (Exercise-Induced Angina):** Highlighted heart stress during physical exertion.
3. **`oldpeak` (ST Depression induced by exercise relative to rest):** Validated as a crucial electrocardiogram risk metric.
