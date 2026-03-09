# AI-Driven Bug Report Classification and Severity Prediction

## Abstract

Software maintenance teams rely heavily on bug reports to identify defects, prioritize issues, and plan corrective actions. However, large-scale software projects generate thousands of unstructured bug reports, making manual triaging slow, inconsistent, and resource-intensive.  

This project proposes an **AI-driven Bug Report Detector** that classifies bug reports along two critical dimensions: **bug type** (e.g., functional, UI, performance) and **severity level** (e.g., minor, major, critical). Using **Natural Language Processing (NLP)** and machine learning techniques, the system analyzes textual bug reports to predict both the type and severity of each issue.  

The goal is to support developers by **improving bug triaging efficiency**, enabling faster prioritization of defects, reducing workload, and enhancing overall software maintenance workflows.

---

## Motivation

Large-scale software systems generate thousands of bug reports during development and maintenance. These reports vary widely in structure, detail, and quality, making **manual triaging time-consuming and error-prone**. Developers must read each report, determine the type of issue, and assign an appropriate severity level—tasks that require significant domain expertise and can delay defect resolution.  

Automating this process can **reduce workload, improve response times, and ensure consistent triaging decisions**. Advances in NLP, particularly **transformer-based models** like BERT and DistilBERT, allow intelligent systems to understand the context and semantics of bug report text, enabling more accurate and scalable classification of bug types and severity levels.

---

## Problem Statement

Bug reports submitted to issue-tracking systems contain **unstructured textual descriptions** that must be manually analyzed to determine both the type and severity of the issue. As software repositories grow, the volume of reports increases rapidly, making manual triaging:

- **Inefficient**  
- **Inconsistent**  
- **Difficult to scale**

This results in delays in identifying critical defects and increases the maintenance burden on development teams.

This project aims to develop a **machine learning system** that automatically predicts:

1. **Bug Category** – Identifying the nature of the defect (e.g., UI bug, performance issue, crash, security vulnerability).  
2. **Bug Severity Level** – Determining the urgency of the issue (e.g., critical, major, minor, trivial).  

Automating these tasks will **improve efficiency, consistency, and accuracy** in bug management for modern software engineering environments.

---

## Research Objectives

The primary objectives of this project are:

1. **Collect and preprocess real-world bug reports** from open-source software repositories, ensuring high-quality textual inputs for model training.  
2. **Design an NLP pipeline** capable of extracting meaningful features from unstructured bug report descriptions.  
3. **Implement traditional machine learning models** (e.g., TF‑IDF + SVM) for automated bug type and severity classification.  
4. **Develop and fine-tune transformer-based deep learning models** (e.g., DistilBERT) for improved contextual understanding and classification accuracy.  
5. **Evaluate and compare the performance** of traditional ML methods and pre-trained transformer models across both classification tasks.  
6. **Demonstrate the effectiveness of AI-driven automation** in enhancing the speed, consistency, and reliability of bug triaging processes.
7. **Evaluate** how traditional machine learning models (such as Logistic Regression, SVM) compare with transformer‑based pretrained models (such as                  BERT/DistilBERT) in terms of accuracy, robustness, and generalization for bug report classification and severity prediction.

---

## Dataset

This project uses the **50K Bug Dataset** from Kaggle, which contains real-world bug reports collected from issue tracking systems. These reports include textual descriptions and labels that help categorize software defects.

### Dataset Source

- **Dataset Name:** 50K Bug Dataset  
- **Platform:** Kaggle  
- **Access Link:** [Download Dataset](https://www.kaggle.com/datasets/mirzayasirabdullah07/50k-bug-dataset?resource=download)

### Dataset Features

The dataset includes the following key fields:

- **title:** A short summary of the bug.  
- **description:** A detailed explanation of the issue reported by the user or developer.  
- **bug_category:** The type of bug, such as UI bug, performance issue, security vulnerability, or crash.  
- **severity:** Indicates how critical the bug is, e.g., low, medium, high, or critical.

### How the Dataset is Used

In this project:

- **Text Input Features:**  
  The **title** and **description** fields are combined to create the textual input for the models.

- **Bug Classification Task:**  
  The **bug_category** field is used as the **target label** for classifying the type of bug.

- **Severity Prediction Task:**  
  The **severity** field is used to train models to **predict how critical a bug is**.
  
---

## Methodology

The proposed system follows a structured machine learning pipeline for bug report classification and severity prediction.

### 1. Data Preprocessing
- The **title** and **description** of each bug report are combined into a single text field.  
- The text is cleaned by:
  - Lowercasing  
  - Removing punctuation  
  - Removing stopwords  
  - Tokenizing  
- These steps ensure the input is consistent and ready for feature extraction.

### 2. Feature Representation
Two feature extraction approaches are used:

#### a) TF-IDF Representation (for Traditional ML Models)
- Converts the cleaned text into numerical vectors using **TF-IDF**.  
- These vectors are used to train traditional models such as:
  - **Support Vector Machines (SVM)**  
  - **Logistic Regression**  

#### b) Deep Learning Models
- **Text-CNN:** Trained on word embeddings to capture local patterns in text.  
- **Transformer-Based Models (BERT / DistilBERT):** Pre-trained transformers generate contextual embeddings and are fine-tuned for classification.  

---

## Model Evaluation

- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  

Comparative analysis: traditional ML vs Deep Learning Models.

---

## Technologies and Tools

The project implementation uses the following technologies:

- Python  
- Scikit-learn  
- HuggingFace Transformers  
- Pandas  
- NumPy  
- Matplotlib / Seaborn  
- Jupyter Notebook  
- GitHub  

---

## Project Workflow

1. Dataset Collection  
2. Data Cleaning and Preprocessing  
3. Exploratory Data Analysis (EDA)  
4. Feature Extraction  
5. Baseline Model Training (TF‑IDF + SVM / Logistic Regression)  
6. Deep Learning Model Training (Text-CNN, BERT / DistilBERT)  
7. Model Evaluation and Performance Comparison  
8. Development of Final Prediction System
---

System Architecture

The proposed system follows a structured pipeline for automated bug classification and severity prediction.
Bug Report Input
Raw bug reports containing the title and description are provided as input.

Text Preprocessing
The text is cleaned through lowercasing, punctuation removal, stopword removal, and tokenization.

Feature Extraction
TF-IDF vectors are generated for traditional machine learning models.
Transformer embeddings are used for deep learning models.

Model Training
The system trains multiple models including:
Logistic Regression
Support Vector Machines (SVM)
Text-CNN
DistilBERT

Prediction
The trained models predict:
Bug Category
Severity Level

Evaluation
Model performance is evaluated using classification metrics.

----

Future Work
Future improvements to the system may include:
Integration with real issue-tracking systems such as GitHub and Jira
Development of a web interface for real-time bug prediction
Training larger transformer models such as BERT-Large
Multi-label classification for complex bug reports
Automatic detection of duplicate bug reports
