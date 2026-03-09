# AI-Driven Bug Report Classification and Severity Prediction

## Abstract
Software maintenance teams rely heavily on bug reports to identify defects, prioritize issues, and plan corrective actions. However, the rapid growth of large‑scale software projects has resulted in thousands of unstructured bug reports, making manual triaging slow, inconsistent, and resource‑intensive. This project proposes an automated Bug Report Detector that classifies bug reports along two critical dimensions: bug type (e.g., functional, UI, performance) and severity level (e.g., minor, major, critical).

This project proposes an Artificial Intelligence-based system for automatically classifying bug reports using Natural Language Processing (NLP) and machine learning techniques. The proposed system will analyze textual bug reports and predict both the **type of bug** and the **severity level** of the reported issue. The goal is to support developers by improving bug triaging efficiency and enabling faster prioritization of software defects.By automating bug type and severity prediction, this work aims to support faster triaging, reduce developer workload, and enhance the overall efficiency of software maintenance workflows.

---

## Motivation
Large‑scale software systems generate thousands of bug reports throughout their development and maintenance cycles. These reports vary widely in structure, detail, and quality, making manual triaging a time‑consuming and error‑prone process. Developers must read each report, determine the type of issue, and assign an appropriate severity level tasks that require significant domain expertise and often delay the resolution process.

Automating this classification process can substantially reduce developer workload, improve response times, and ensure more consistent triaging decisions. With the rapid advancement of Natural Language Processing (NLP), especially transformer‑based models such as BERT and DistilBERT, it is now possible to build intelligent systems capable of understanding the context and semantics of textual bug reports. Leveraging these models enables more accurate and scalable classification of bug types and severity levels, ultimately enhancing the efficiency and reliability of software maintenance workflows.

---

## Problem Statement
Bug reports submitted to issue‑tracking systems contain unstructured textual descriptions that must be manually analyzed by developers to determine both the type and severity of the issue. As software repositories grow, the volume of incoming reports increases rapidly, making manual triaging inefficient, inconsistent, and difficult to scale. This leads to delays in identifying critical defects and increases the overall maintenance burden on development teams.

This project aims to develop a machine learning system that automatically predicts:

1. **Bug Category** – identifying the nature of the defect (e.g., UI bug, performance issue, crash bug, security vulnerability).
2. **Bug Severity Level** – determining the urgency of the issue (e.g., critical, major, minor, trivial).

Automating these tasks can significantly improve the efficiency, consistency, and accuracy of bug management in modern software engineering environments.

---

## Research Objectives

The primary objectives of this project are:

1)To collect and preprocess real‑world bug report datasets from open‑source software repositories, ensuring high‑quality textual inputs for model training.

2)To design an NLP pipeline capable of extracting meaningful features from unstructured bug report descriptions.

3)To implement traditional machine learning models (e.g., TF‑IDF + SVM) for automated bug type and severity classification.

4)To develop and fine‑tune transformer‑based deep learning models (e.g., DistilBERT) for improved contextual understanding and classification accuracy.

5)To evaluate and compare the performance of traditional ML methods and pre‑trained transformer models across both classification tasks.

6)To demonstrate the effectiveness of AI‑driven automation in enhancing the speed, consistency, and reliability of bug triaging processes.

---

## Dataset

This project utilizes the 50K Bug Report Dataset from Kaggle, a large‑scale collection of software defect reports aggregated from multiple open‑source repositories. The dataset contains over 50,000 real bug reports, making it suitable for training and evaluating machine learning and transformer‑based models for automated bug triaging.The dataset can be accessed at the following link:

https://www.kaggle.com/datasets/mirzayasirabdullah07/50k-bug-dataset
 
The dataset includes the following key fields:

  -Title / Summary – a short description of the issue

  -Description – detailed textual information about the bug

  -Component / Module – the part of the system affected

  -Priority / Severity – the urgency or impact of the issue

  -Labels / Tags – metadata used for categorizing the bug

---

## Methodology

The proposed system will follow a structured machine learning pipeline.

### Data Preprocessing
The textual bug reports will undergo several preprocessing steps including:

- Text normalization
- Tokenization
- Removal of punctuation and special characters
- Stop-word removal
- Lowercasing of text

### Feature Representation

Two different feature extraction techniques will be explored:

**TF-IDF Representation**

Term Frequency–Inverse Document Frequency (TF-IDF) will be used to convert textual bug reports into numerical vectors suitable for traditional machine learning algorithms.

**Transformer-Based Embeddings**

Contextual embeddings generated using pre-trained transformer models such as **BERT** or **DistilBERT** will be used for deep learning-based classification.

---

## Model Evaluation

Model performance will be evaluated using standard classification metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

A comparative analysis will be conducted to evaluate the effectiveness of traditional machine learning approaches versus transformer-based models.

---

## Technologies and Tools

The implementation of this project will use the following technologies:

- Python
- Scikit-learn
- HuggingFace Transformers
- Pandas
- NumPy
- Matplotlib / Seaborn
- Jupyter Notebook
- GitHub for version control and collaboration

---

## Project Workflow

1. Dataset Collection  
2. Data Cleaning and Preprocessing  
3. Exploratory Data Analysis  
4. Feature Extraction  
5. Baseline Model Training (TF-IDF + ML Models)  
6. Transformer Model Training (BERT / DistilBERT)  
7. Model Evaluation and Performance Comparison  
8. Development of Final Prediction System  

---
