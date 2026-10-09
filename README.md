# Machine Learning Classification and Model Evaluation

A Python/Jupyter Notebook project exploring supervised classification, dimensionality reduction for visualization, and model evaluation using scikit-learn.

## Project Overview

This notebook demonstrates classification workflows on two built-in scikit-learn datasets:

- **Breast Cancer Wisconsin dataset:** Binary classification with Logistic Regression and Random Forest.
- **Handwritten Digits dataset:** Multiclass classification using Logistic Regression.

The breast cancer experiment also uses **Principal Component Analysis (PCA)** to display the data in two dimensions and visualize model decision boundaries.

## Techniques and Tools

- Python, Jupyter Notebook, Google Colab
- pandas, NumPy, Matplotlib
- scikit-learn
- Train/test splitting
- Logistic Regression and Random Forest classification
- PCA for 2D visualization
- Accuracy, confusion matrices, and ROC curves

## Results

The following accuracies are reported in the saved notebook outputs:

| Dataset | Model | Test accuracy |
| --- | --- | ---: |
| Breast Cancer Wisconsin | Logistic Regression | 96.49% |
| Breast Cancer Wisconsin | Random Forest | 97.37% |
| Handwritten Digits | Logistic Regression | 96.66% |

The notebook also includes confusion-matrix plots and ROC curves for both breast cancer classifiers. These values are from the notebook's saved execution, not a new independent benchmark.

## Notebook Contents

1. Imports and a Google Drive CSV-loading example.
2. Logistic Regression on the breast cancer dataset.
3. Two-dimensional PCA projection of the breast cancer data.
4. Visualization of the Logistic Regression decision boundary in PCA coordinates.
5. Random Forest training and decision-boundary visualization.
6. Confusion matrices and ROC curves for the two classifiers.
7. Logistic Regression classification of handwritten digits.

## Getting Started

### Requirements

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

### Run the notebook

1. Clone or download this repository.
2. Open in Jupyter Notebook, VS Code, or Google Colab.
3. Run the model-training and evaluation cells in order.

**Note:** The first cells contain a Google Colab-specific Google Drive mount and reference a private file path (`/content/drive/MyDrive/Colab Notebooks/GSCopy.csv`). This CSV is not included in the notebook. To run those cells, provide your own file and update the path, or skip the Google Drive/CSV-loading cells. The scikit-learn breast cancer and digits datasets are loaded directly from the library.

## Limitations and Future Improvements

- The PCA projection is used for **visualization**, while the classifiers are trained on the original feature space. The displayed decision boundaries therefore represent model predictions on inverse-transformed points from the 2D PCA plane.
- The PCA transformation is fitted on the complete breast cancer dataset for visualization; fitting it on the training set only would be preferable in a more rigorous evaluation workflow.
- The notebook contains a repeated Random Forest training cell, which could be removed for clarity.
- Future work could add stratified cross-validation, hyperparameter tuning, feature scaling where appropriate, and a consolidated model comparison table.

## Purpose

This project demonstrates practical understanding of classification algorithms, dimensionality reduction, visualization, and model performance assessment in Python.

## Disclaimer

This is an educational machine learning exercise. The breast cancer classification example is not a clinical diagnostic tool.
