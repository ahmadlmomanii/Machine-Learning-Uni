# Dry Bean Classification Using SVM and Optimization Algorithms

<p align="center">
  **A Machine Learning Project for Multiclass Classification and Optimizer Performance Evaluation**
</p>

---

## 📌 Project Overview

This project focuses on classifying dry bean varieties using machine learning techniques, specifically Support Vector Machines (SVM).

The main objective is to investigate how different optimization algorithms affect the performance of SVM models when applied to a multiclass classification problem.

The project evaluates four SVM kernels and compares five optimization algorithms based on classification performance, convergence behavior, training loss, and computational time.

The experiments use the Dry Bean Dataset, which contains numerical features extracted from images of seven different dry bean varieties.

## 🎯 Project Objectives

- Explore and analyze the Dry Bean Dataset.
- Perform data preprocessing and feature standardization.
- Build a baseline SVM classifier.
- Evaluate different SVM kernel functions.
- Implement and compare five optimization algorithms.
- Analyze training loss and convergence behavior.
- Evaluate models using multiple classification metrics.
- Identify the best-performing optimizer and kernel combination.

## 📊 Dataset

**Dataset:** Dry Bean Dataset

**Source:** [Kaggle - Dry Bean Dataset](https://www.kaggle.com/datasets/muratkokludataset/dry-bean-dataset)

The dataset contains 13,611 observations and 17 columns:

- 16 numerical features.
- 1 target variable (`Class`).

### Bean Classes

The dataset includes seven dry bean varieties:

1. BARBUNYA
2. BOMBAY
3. CALI
4. DERMASON
5. HOROZ
6. SEKER
7. SIRA

### Features

The numerical features describe the geometric characteristics of bean images, including:

- Area
- Perimeter
- MajorAxisLength
- MinorAxisLength
- AspectRation
- Eccentricity
- ConvexArea
- EquivDiameter
- Extent
- Solidity
- Roundness
- Compactness
- ShapeFactor1
- ShapeFactor2
- ShapeFactor3
- ShapeFactor4

## ⚙️ Project Methodology

The project follows a structured machine learning workflow:

1. **Data Loading:** Import the dataset from Kaggle.
2. **Exploratory Data Analysis (EDA):** Examine distributions, class frequencies, statistical summaries, and feature correlations.
3. **Data Preprocessing:** Check missing values, identify duplicate records, and prepare the features and target.
4. **Train-Test Split:** Split the dataset into training and testing sets using stratified sampling.
5. **Feature Scaling:** Apply standardization to numerical features.
6. **Baseline SVM:** Train and evaluate SVM models using different kernels.
7. **Optimizer Experiments:** Evaluate five optimization algorithms independently.
8. **Performance Evaluation:** Compare classification metrics, training loss, and training time.
9. **Final Comparison:** Rank the optimizers based on their performance.

## 🧠 SVM Kernel Functions

Four kernel functions were investigated:

| Kernel | Description |
|---|---|
| Linear | Linear decision boundaries |
| Polynomial | Nonlinear polynomial decision boundaries |
| RBF | Radial Basis Function for nonlinear classification |
| Sigmoid | Sigmoid-based kernel transformation |

## 🚀 Optimization Algorithms

Five optimization algorithms were evaluated:

### 1. Gradient Descent (GD)

Uses the gradient of the objective function to update model parameters iteratively.

### 2. Stochastic Gradient Descent (SGD)

Updates model parameters using individual training samples, providing frequent parameter updates.

### 3. Mini-Batch Gradient Descent

Uses small batches of training samples to combine aspects of batch and stochastic optimization.

### 4. RMSProp

Adapts the learning rate using a moving average of squared gradients.

### 5. Adam

Combines momentum and adaptive learning-rate estimation to optimize model parameters.

Each optimizer was evaluated separately using the four SVM kernel configurations.

## 📈 Experimental Results

### Baseline SVM Results

The RBF kernel achieved the best baseline performance.

| Metric | Score |
|---|---:|
| Accuracy | 92.25% |
| Precision | 93.54% |
| Recall | 93.22% |
| Macro F1 | 93.36% |
| Weighted F1 | 92.27% |

### Final Optimizer Comparison

The following table presents the best kernel configuration for each optimizer, ranked by Macro F1-score.

| Optimizer | Best Kernel | Accuracy | Macro F1 |
|---|---|---:|---:|
| SGD | RBF | 91.40% | 92.55% |
| Mini-Batch GD | RBF | 90.59% | 91.86% |
| GD | RBF | 85.71% | 87.30% |
| Adam | Linear | 81.21% | 80.08% |
| RMSProp | Linear | 80.69% | 79.01% |

### Training Time Comparison

| Optimizer | Training Time |
|---|---:|
| SGD | 40.23 seconds |
| Mini-Batch GD | 4.31 seconds |
| GD | 5.56 seconds |
| Adam | 1.71 seconds |
| RMSProp | 1.70 seconds |

### Key Findings

- SGD achieved the highest Accuracy and Macro F1-score among the five optimizer experiments.
- Mini-Batch Gradient Descent achieved competitive classification performance with significantly lower training time.
- RBF was the best-performing kernel for GD, SGD, and Mini-Batch GD.
- Linear was the best-performing kernel for Adam and RMSProp.
- Adam and RMSProp demonstrated lower training times in these experiments.

**Overall Best Configuration:** SGD with RBF Kernel.

## 🛠️ Technologies and Libraries

The project uses the following technologies:

- Python
- Jupyter Notebook
- Kaggle Notebooks
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## 📉 Evaluation Metrics

The models were evaluated using:

- **Accuracy:** Overall percentage of correctly classified samples.
- **Precision:** Ability to make correct positive class predictions.
- **Recall:** Ability to identify actual samples belonging to each class.
- **Macro F1-score:** Average F1-score across all classes, treating each class equally.
- **Weighted F1-score:** F1-score averaged according to the number of samples in each class.
- **Training Loss:** Measures the optimization objective during training.
- **Training Time:** Measures the time required to train each model.

## ⚠️ Limitations

- The optimization experiments used different epoch counts and hyperparameter configurations.
- Training time depends on the implementation and computational environment.
- Selecting the best kernel using test-set performance may introduce selection bias. A separate validation strategy is recommended for a more rigorous comparison.
- Results may vary with different random seeds and hyperparameter settings.

## 🔮 Future Improvements

Potential future improvements include:

- Hyperparameter optimization for each optimizer.
- Cross-validation for more reliable model evaluation.
- Testing additional optimization algorithms.
- Evaluating model generalization on unseen datasets.
- Comparing convergence speed under equivalent computational budgets.
- Further investigating class-specific classification errors.

## 👨‍💻 Author

**Ahmad Al-Momani**

Data Science & Artificial Intelligence Student

GitHub: [Add your GitHub profile URL]

---

## 📚 Dataset Reference

Koklu, M., & Ozkan, I. A. (2020). *Multiclass classification of dry beans using computer vision and machine learning techniques.*

Dataset available on [Kaggle](https://www.kaggle.com/datasets/muratkokludataset/dry-bean-dataset).

---

<p align="center">
  **Built with Python and Machine Learning**
</p>
