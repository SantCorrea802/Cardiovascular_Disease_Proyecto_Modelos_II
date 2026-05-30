# Cardiovascular Disease Prediction Project

This repository contains a machine learning course project for cardiovascular disease prediction using exploratory data analysis, preprocessing, supervised classification models, dimensionality reduction, and final model comparison.

The project evaluates five model families: Logistic Regression, KNN, Random Forest, Support Vector Machine, and Multilayer Perceptron. The official model-selection metric is ROC-AUC, while recall, F2-score, false negatives, and false positives are also analyzed due to the clinical relevance of cardiovascular disease screening.

## Repository Structure

```text
PROYECTO_MODELOS_II/
├── dataset/
│   ├── cardio_train.csv
│   └── data_cleaned.csv
│
├── EDA_preprocessing/
│   └── EDA.ipynb
│
├── Models/
│   ├── logistic_regression.ipynb
│   ├── knn.ipynb
│   ├── random_forest.ipynb
│   ├── svm.ipynb
│   └── mlp_ann.ipynb
│
├── ExportedModels/
│   ├── exported_logistic_regression.joblib
│   ├── exported_knn.joblib
│   ├── exported_random_forest2.joblib
│   ├── exported_svm.joblib
│   └── exported_mlp.joblib
│
├── FinalStage/
│   ├── 01_selected_models.ipynb
│   ├── 02_dimensionality_reduction.ipynb
│   ├── 03_prueba_inferencia_modelo_final.ipynb
│   └── ReportAssets/
│
├── Informe/
│   └── Cardiovascular_Disease_Prediction_Through_Data_Preprocessing_and_Classification_Techniques.pdf
│
└── README.md
```
Folder Description
dataset/: contains the original dataset and the cleaned dataset used by the models.
EDA_preprocessing/: contains the exploratory data analysis and preprocessing notebook.
Models/: contains the individual training notebooks for each machine learning model.
ExportedModels/: contains the trained models exported with joblib.
FinalStage/: contains the final model comparison, dimensionality reduction experiments, and a simple inference test.
Informe/: contains the final academic report in IEEE format.
Execution Order

To reproduce the project, run the notebooks in the following order:

EDA_preprocessing/EDA.ipynb
Performs exploratory data analysis, cleaning, feature engineering, and generates data_cleaned.csv.
Models/logistic_regression.ipynb
Trains and evaluates Logistic Regression.
Models/knn.ipynb
Trains and evaluates K-Nearest Neighbors.
Models/random_forest.ipynb
Trains and evaluates Random Forest.
Models/svm.ipynb
Trains and evaluates Linear SVM and RBF SVM.
Models/mlp_ann.ipynb
Trains and evaluates the Multilayer Perceptron neural network.
FinalStage/01_selected_models.ipynb
Compares the final metrics of all five models and selects the final model.
FinalStage/02_dimensionality_reduction.ipynb
Applies feature analysis, PCA, and UMAP to evaluate dimensionality reduction on the top two models.
FinalStage/03_prueba_inferencia_modelo_final.ipynb
Loads the exported final model and performs a simple prediction test.
Environment

The exported models were generated using a scikit-learn compatible environment. For loading the exported .joblib models, use:

pip install scikit-learn==1.6.1 pandas numpy matplotlib joblib jupyter

If the notebooks are executed from scratch, small numerical differences may appear depending on the environment and library versions.

Final Model

The final selected model is the Multilayer Perceptron because it achieved the highest validation ROC-AUC among the evaluated models. The model is interpreted as a screening-oriented classifier, since threshold adjustment prioritized recall and F2-score to reduce false negatives.

Report

## The final report is available in:

Informe/Cardiovascular_Disease_Prediction_Through_Data_Preprocessing_and_Classification_Techniques.pdf

## Video

