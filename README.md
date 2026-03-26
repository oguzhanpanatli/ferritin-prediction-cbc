# ferritin-prediction-cbc
Source code for Beyond Prediction: Explainable Machine Learning for Ferritin Estimation from Complete Blood Count

# CBC-Based Ferritin Estimation using Machine Learning

This repository contains the official Python implementation and Jupyter Notebooks for the data preprocessing, hyperparameter optimization, and model training processes associated with our manuscript on predicting continuous and binary ferritin levels using Complete Blood Count (CBC) data.

## 🔬 Clinical Context & Background
The primary objective of our study is to predict low plasma ferritin levels. Plasma ferritin concentration reflects the body's iron storage status and is therefore the most commonly used biomarker for diagnosing iron deficiency.

In cases of iron deficiency, erythropoiesis is impaired, and newly produced red blood cells are generally microcytic (mean corpuscular volume (MCV) < 80 fL) and hypochromic (mean corpuscular hemoglobin (MCH) <  1.7 fmol). Since ferritin is not routinely included in the laboratory requests for many anemic primary care patients, iron deficiency often remains undiagnosed. Furthermore, the measurement of ferritin, which is essential for distinguishing iron deficiency anemia from other types of anemia, is relatively costly.

Conversely, a Complete Blood Count (CBC) is a highly accessible and cost-effective routine test. Leveraging CBC parameters, machine learning models can assist in both estimating ferritin levels and accurately distinguishing iron deficiency anemia from other forms of anemia.

## 🚀 Technical Overview
To address the architectural complexities of the predictive models for both classification (Normal vs. Low Ferritin) and regression (Continuous Ferritin Levels) tasks, hyperparameter optimization was conducted using KerasTuner. The models evaluated include Artificial Neural Networks (ANN), XGBoost, Random Forest, Support Vector Machines (SVM), and Logistic Regression.

## 📁 Repository Contents
* `1_FerritinPredictionClassificationML.ipynb`: Source code for the ML models binary classification task (including  optimization, ROC/AUC generation, and confusion matrices).
* `02_FerritinPredictionClassificationANN.ipynb`:Source code for the ANN binary classification task (including ANN optimization, ROC/AUC generation, and confusion matrices).
* `03_FerritinPredictionRegressionANN.ipynb`: Source code for the continuous ferritin value prediction task (including deeper ANN architecture and MSE evaluations).

*(Note: Due to patient privacy and ethical restrictions, the raw clinical dataset is not publicly shared in this repository.)*

## 📊 Dataset Characteristics
Although the raw clinical dataset cannot be shared publicly due to patient privacy and ethical regulations, the models were developed and evaluated using a comprehensive dataset with the following properties:

* **Total Observations:** 7,200 patient records
* **Total Variables:** 11 features (9 numeric, 2 categorical)
* **Independent Variables (9 Predictors):** * Age, Gender, HGB (12-16), MCV (81-101), HCT (36-44), WBC (4.5-10), MPV (9-12), MCH (27-35), RDW-CV (11.5-14.5)
* **Dependent Variables (2 Targets):**
  * `Ferritin Level`: Categorical target used for the binary classification task (Low vs. Normal).
  * `Ferritin (30-400)`: Continuous target used for the regression task.

## ⚙️ How to Run
You can easily review or run the `.ipynb` files by importing them directly into Google Colab or Jupyter Notebook.
