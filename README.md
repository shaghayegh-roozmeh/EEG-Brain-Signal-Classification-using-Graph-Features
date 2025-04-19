# EEG Brain Connectivity Classification using Graph Features

This project analyzes EEG signals from infants to classify them as healthy or disordered using graph-based features extracted from brain connectivity matrices. The analysis is conducted in Python using a combination of signal processing, graph theory, and machine learning.

## 📚 Overview

I apply signal processing and graph theory techniques to extract features from EEG connectivity matrices derived from:
- Pearson Correlation
- Phase Lag Index (PLI)
- Phase Locking Value (PLV)

These matrices are then converted into graphs, and features such as node degree, clustering coefficient, and efficiency are computed. After feature selection using a statistical test (t-test), I train SVM, XGBoost and Randome Forest classifiers to predict whether the EEG sample comes from a healthy or disordered subject.

## 🧠 Pipeline Steps

1. Data Loading: EEG .mat files for both healthy and disordered infants.
2. Feature Extraction:
   - Compute correlation, PLI, and PLV matrices for each EEG epoch.
3. Graph Conversion:
   - Convert each matrix into an undirected graph.
   - Extract topological features.
4. Feature Aggregation:
   - Average features over epochs per subject.
5. Feature Selection:
   - Use t-tests to select statistically significant features.
6. Classification:
   - Train SVM, XGBoost and Randome Forest models on selected features for each connectivity method.

## 📁 File Structure

- Brain_Signal_EEG.ipynb: Main notebook for the full pipeline
- /Healthy/: Folder containing .mat files for healthy subjects
- /Disorder/: Folder containing .mat files for disordered subjects

## ✅ Best Result
- PLV + Random Forest achieved the highest mean accuracy of 0.79
- correlation matrices + Random Forest the highest mean accuracy of 0.79

