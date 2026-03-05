# AI-Driven Bug Report Classification and Severity Prediction

## Abstract
Modern software development environments generate a large volume of bug reports through issue tracking systems such as GitHub, Bugzilla, and Jira. These reports typically contain unstructured natural language descriptions of software defects. Developers must manually analyze each report to determine the nature of the issue and its urgency, which can significantly slow down the bug triaging process.

This project proposes an Artificial Intelligence-based system for automatically classifying bug reports using Natural Language Processing (NLP) and machine learning techniques. The proposed system will analyze textual bug reports and predict both the **type of bug** and the **severity level** of the reported issue. The goal is to support developers by improving bug triaging efficiency and enabling faster prioritization of software defects.

---

## Motivation
Large-scale software systems receive thousands of issue reports during development and maintenance. Manual classification of these reports into appropriate categories and severity levels requires significant human effort and domain expertise. Automating this process can reduce developer workload and improve software maintenance workflows.

Recent advances in NLP and transformer-based language models provide an opportunity to develop intelligent systems capable of understanding textual bug reports and automatically extracting meaningful insights.

---

## Problem Statement
Bug reports submitted to issue tracking systems contain textual descriptions that must be manually analyzed by developers to determine the type and severity of the issue. As software repositories grow, the number of reports increases rapidly, making manual triaging inefficient.

This project aims to develop a machine learning system that automatically predicts:

1. **Bug Category** – identifying the nature of the defect (e.g., UI bug, performance issue, crash bug, security vulnerability).
2. **Bug Severity Level** – determining the urgency of the issue (e.g., critical, major, minor, trivial).

Automating these tasks can significantly improve the efficiency of bug management in software engineering environments.

---

## Research Objectives

The primary objectives of this project include:

- Collect and preprocess real-world bug report datasets from open-source repositories.
- Develop an NLP pipeline to process textual bug reports.
- Implement machine learning models for automated bug classification.
- Predict bug severity levels based on textual descriptions.
- Compare the performance of traditional machine learning models and transformer-based deep learning models.

---

## Dataset

The project will utilize publicly available bug report datasets from open-source software repositories such as:

- **GitHub Issues Dataset**
- **Mozilla Bugzilla Repository**
- **Eclipse Bug Repository**

These datasets typically contain the following information:

- Bug title or summary
- Bug description
- Component or module information
- Priority or severity level
- Issue labels or tags

For the purpose of this project:

- The **bug title and description will be combined to create the textual input features**.
- **Component or label fields will be used to identify bug categories**.
- **Severity or priority fields will be used to determine bug severity levels**.

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

## Model Development

Two categories of models will be implemented and compared.

### Traditional Machine Learning Models

- Logistic Regression
- Naive Bayes
- Support Vector Machines

These models will serve as baseline classifiers.

### Transformer-Based Deep Learning Models

- BERT (Bidirectional Encoder Representations from Transformers)
- DistilBERT

Transformer models capture contextual relationships in natural language and are expected to improve classification performance.

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

## Example Prediction

**Input Bug Report**

Application crashes when uploading large image files.

**Predicted Output**

Bug Category: Crash Bug  
Severity Level: Critical

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

## Repository Structure
