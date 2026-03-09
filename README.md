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

1. **Collect and preprocess real-world bug reports** from open-source software repositories, ensuring high-quality textual inputs for model training.  
2. **Design an NLP pipeline** capable of extracting meaningful features from unstructured bug report descriptions.  
3. **Implement traditional machine learning models** (e.g., TF‑IDF + SVM) for automated bug type and severity classification.  
4. **Develop and fine-tune transformer-based deep learning models** (e.g., DistilBERT) for improved contextual understanding and classification accuracy.  
5. **Evaluate and compare the performance** of traditional ML methods and pre-trained transformer models across both classification tasks.  
6. **Demonstrate the effectiveness of AI-driven automation** in enhancing the speed, consistency, and reliability of bug triaging processes.

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

#### b) Transformer-Based Embeddings (for Deep Learning Models)
- Uses pre-trained transformer models like **BERT** or **DistilBERT** to generate contextual embeddings from text.  
- Embeddings are used for deep learning-based classification.  
- A simple **Text-CNN** model is also trained on word embeddings for comparison.

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
5. Baseline Model Training (TF‑IDF with SVM and Logistic Regression)  
6. Transformer Model Training (BERT / DistilBERT)  
7. Model Evaluation and Performance Comparison  
8. Development of Final Prediction System  

---
