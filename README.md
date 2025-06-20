# Predicting Glioma Grading: Machine Learning Approach

This repository contains code and documentation for a machine learning project focused on predicting glioma grading using genomic and clinical features. The project was developed as part of CGS3342 and is based on data from The Cancer Genome Atlas (TCGA).

## Overview

- **Objective:** Predict the grade of glioma (low-grade vs. high-grade) using a combination of genetic mutations, demographic features, and machine learning techniques.
- **Dataset:** TCGA Brain Glioma Grading Dataset, available on Kaggle.
- **Features:** Includes 23 variables—20 genes and mutation markers (e.g., IDH1, TP53, ATRX), plus demographic information (gender, age, race).
- **Target:** Binary tumor grade (0 = low-grade, 1 = high-grade glioma).

## Methodology

- **Model:** Feed-forward neural network (deep learning).
- **Data Preprocessing:** Categorical features are one-hot encoded.
- **Validation:** 2-fold cross-validation to ensure robust evaluation.
- **Hyperparameter Tuning:** Experimented with different numbers of epochs, hidden layers, and hidden units per layer.

## Results

| Model Configuration         | Precision | Recall | F1-Score | Accuracy |
|----------------------------|-----------|--------|----------|----------|
| 3 hidden layers, 32 units  | 0.800     | 0.895  | 0.845    | 0.862    |
| 5 hidden layers, 64 units  | 0.809     | 0.830  | 0.819    | 0.846    |

- **Best Accuracy:** ~86% for predicting glioma grading.
- **Confusion Matrix:** Demonstrated strong performance in distinguishing between low- and high-grade gliomas.

## Project Structure

```
project/
├── clinical_glioma_grading.csv         # processed datasets
├── gliomaprediction.ipynb              # Jupyter notebooks for analysis
└── README.md                           # This file
```

## Usage

1. **Data Preparation:** Place the TCGA glioma dataset in the `data/` directory.
2. **Preprocessing:** Run preprocessing scripts to encode features and split the data.
3. **Model Training:** Use the notebooks or scripts in `notebooks/` or `src/` to train and evaluate the neural network.
4. **Evaluation:** Review metrics and visualizations in the `results/` directory.

## References

- **Dataset:** Clinical_gliomagrading on Kaggle
- **Literature:**  
  - McCaffrey, James. "How to Do Neural Binary Classification Using Keras."
  - Barstugan, Ozkaya, Ozturk. "Coronavirus (COVID-19) Classification Using CT Images by Machine Learning Methods."
- **Project Slides:** See attached PDF for detailed methodology and results.

## Contributors

- Nandini Muresh
- Anveetha Suresh
- Aashna Kothari
- Francessa Palladino
