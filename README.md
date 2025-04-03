# Bank Marketing Classification Analysis

## Overview
This repository contains a Jupyter Notebook for analyzing and modeling a **bank marketing classification dataset**. The dataset is used to predict whether a customer will subscribe to a bank's term deposit based on various attributes such as age, job type, and previous campaign interactions.

## Dataset
The dataset used is the **bank marketing dataset**, which includes features like:
- Customer demographics (age, job, marital status, education)
- Contact details (communication type, last contact duration)
- Socioeconomic indicators (consumer confidence index, interest rate)
- Previous marketing campaign interactions

## Prerequisites
To run this project on your local machine, install the following dependencies:

### 1. Install Python
Download and install Python (preferably 3.8 or later) from [python.org](https://www.python.org/downloads/).

### 2. Install Jupyter Notebook
```sh
pip install notebook
```

### 3. Install Required Libraries
```sh
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### 4. Clone the Repository & Navigate
```sh
git clone <repository_url>
cd <repository_folder>
```

## Running the Jupyter Notebook

1. Open a terminal or command prompt.
2. Navigate to the repository folder:
   ```sh
   cd /path/to/your/repository/
   ```
3. Launch Jupyter Notebook:
   ```sh
   jupyter notebook
   ```
4. Open the provided Jupyter Notebook (`v1.ipynb`).
5. Run all the cells sequentially using `Shift + Enter` or `Kernel > Restart & Run All`.

## Notebook Workflow

### 1. Data Loading & Exploration
- Reads the bank marketing dataset using `pandas.read_csv()`.
- Performs an initial inspection using `.info()` and `.describe()`.
- Checks for missing values and inconsistent data.

### 2. Data Preprocessing
- Converts categorical variables into numerical format using **one-hot encoding**.
- Handles missing values and outliers.
- Normalizes numerical features if necessary.

### 3. Model Training & Evaluation

#### **XGBoost Model & Grid Search**
- An **XGBoost classifier** was trained using default parameters.
- A **grid search** was performed to optimize hyperparameters, but the model resulted in a **low accuracy and F1-score**.
- Due to its underperformance, XGBoost was ignored in favor of other models like **Random Forest** and **Logistic Regression**.

#### **Final Model Selection**
- The best-performing model was selected based on:
  - Accuracy
  - Precision
  - Recall
  - F1-score
- The model was evaluated using a **confusion matrix** and ROC-AUC curves.

## Results & Insights
- Identified key features influencing customer subscription decisions.
- Observed that previous marketing interactions and call duration were strong predictors.
- Provided recommendations for improving marketing campaigns.

## Troubleshooting

### 1. ModuleNotFoundError
**Error:** `ModuleNotFoundError: No module named 'pandas'`  
**Solution:** Install missing packages using:
```sh
pip install pandas
```

### 2. FileNotFoundError
**Error:** `FileNotFoundError: [Errno 2] No such file or directory: 'bank_data.csv'`
**Solution:** Ensure the dataset file is placed in the correct directory.

---
By following this guide, you should be able to successfully run the analysis and interpret the results of the bank marketing classification dataset.

