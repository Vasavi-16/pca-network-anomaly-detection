# PCA-Based Network Anomaly Detection

## Overview

This project explores anomaly detection in network traffic using Principal Component Analysis (PCA) on the KDD Cup 99 dataset.

The model learns patterns from normal network traffic and uses reconstruction error to identify potentially anomalous records.

## Objectives

* Preprocess numerical and categorical network features.
* Apply PCA for dimensionality reduction.
* Learn a baseline from normal training records.
* Identify anomalies using reconstruction error and a validation-based      threshold.
* Evaluate performance using classification metrics.

## Approach

1. Load the KDD Cup 99 dataset using scikit-learn.
2. Convert the original labels into normal and attack classes.
3. Split the data into training, validation, and test sets.
4. One-hot encode categorical features and scale numerical features.
5. Train Incremental PCA using normal training records.
6. Calculate reconstruction errors and select an anomaly threshold using normal validation records.
7. Evaluate predictions on the held-out test set.

## Technologies

* Python
* pandas
* NumPy
* scikit-learn
* SciPy
* Jupyter Notebook

## Evaluation

The model is evaluated using:

* Confusion matrix
* Precision
* Recall
* F1-score
* Average Precision

The notebook contains the implementation and evaluation results.

## Dataset

The project uses the 10% version of the KDD Cup 99 dataset, retrieved using `fetch_kddcup99` from scikit-learn.

The dataset is an older benchmark, so results should not be interpreted as evidence of performance on modern network traffic.

## Limitations

* PCA-based anomaly detection depends on the selected number of components and anomaly threshold.
* The model may produce false positives and false negatives.
* Unseen feature combinations do not necessarily represent previously unseen attack types.
* Performance on this dataset may not generalize to real-world network environments.

## Future Improvements

* Compare PCA with Isolation Forest.
* Analyze false positives and false negatives.
* Investigate performance on unseen feature rows.
* Explore evaluation on more recent network intrusion datasets.
