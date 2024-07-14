# Jupyter on Replit

Create Jupyter notebooks on Replit!

Instructions:

1. In the shell run `./generate_password.sh`
2. Enter password for your Jupyter notebook.
3. Copy enecrypted password to a Replit Secret with the name `NOTEBOOK_PASSWORD`
4. Run the repl
5. Open the webview in a new tab (you cannot log in via the webview in the workspace)
6. Log in with the password you entered in step 2


Here's an updated `README.md` file with more details on the machine learning models used, their statistics, and the commands to run the program:

```markdown
# Credit Card Fraud Detection with Anomaly Detection Methods

This project demonstrates how to detect credit card fraud using anomaly detection techniques in Python, specifically through the use of Isolation Forest and Local Outlier Factor algorithms.

## Table of Contents
- [Introduction](#introduction)
- [Setup](#setup)
- [Data Preprocessing](#data-preprocessing)
- [Exploration](#exploration)
- [Anomaly Detection Methods](#anomaly-detection-methods)
- [Results](#results)
- [Running the Program](#running-the-program)
- [Conclusion](#conclusion)
- [License](#license)

## Introduction

Fraud detection is a critical area in finance, and this project utilizes machine learning techniques to identify fraudulent transactions in credit card datasets. Given the highly imbalanced nature of the dataset, this project focuses on unsupervised learning methods to detect anomalies.

## Setup

To run this project, ensure you have Python installed along with the following libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

You can install the required libraries using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Data Preprocessing

The dataset is first imported from a CSV file, and only 10% of the data is used to make computations manageable. Key preprocessing steps include:
- Loading the data and inspecting columns.
- Visualizing distributions using histograms.
- Calculating the fraction of fraudulent transactions.
- Creating a correlation matrix to understand relationships between variables.

## Exploration

During exploration, histograms reveal that most of the features (V1 through V28) cluster around zero with few outliers. The analysis indicates a significant class imbalance, with approximately 0.17% of transactions labeled as fraudulent.

## Anomaly Detection Methods

Two anomaly detection algorithms are implemented:

1. **Isolation Forest**:
   - Constructs a set of random decision trees to isolate anomalies.
   - Parameters include `max_samples`, `contamination`, and `random_state`.

2. **Local Outlier Factor**:
   - Measures the local density deviation of data points with respect to their neighbors.
   - Parameters include `n_neighbors` and `contamination`.

Both algorithms are evaluated using metrics such as accuracy, precision, recall, and F1-score. Here are the key statistics from the evaluation:

- **Local Outlier Factor**:
  - Accuracy: 99.65%
  - Precision (fraudulent transactions): 0.02%
  - Recall: Low
  - F1-Score: Low

- **Isolation Forest**:
  - Accuracy: 99.75%
  - Precision (fraudulent transactions): 30%
  - Recall: Slightly improved over LOF
  - F1-Score: Better than LOF

## Running the Program

To run this program, follow these steps:

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Run the following command:

```bash
python Credit.ipynb
```


## Conclusion

This project illustrates the importance of understanding the dataset's characteristics and the implications of precision and recall in machine learning. While the methods explored here provide a foundational approach to fraud detection, further improvements could be achieved by experimenting with more complex models or utilizing the full dataset.

```
