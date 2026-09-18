# AgroShield: AI-Powered Counterfeit Agricultural Input Detection

## 📌 Project Overview
**AgroShield** is an AI-powered mobile application designed to protect smallholder farmers in Kenya from counterfeit agricultural inputs (seeds, fertilizers, and pesticides)[cite: 2]. By leveraging computer vision and transfer learning models, AgroShield enables real-time verification of product packaging authenticity directly at the point of sale[cite: 1, 2].


---

## 👥 Team Members
| Name | Student ID |
| :--- | :--- |
| **Moses Mugo** | 190027 |
| **Barak Makedi** | 165767 |
| **Alfred peter** | 190285 |

---

## 📊 Deliverable 1: Dataset Exploration Summary

Because public, ready-made datasets of fake Kenyan agricultural packaging do not currently exist, our methodology uses related open-source packaging and e-commerce image datasets for initial pre-training and pipeline development[cite: 1].

### Open-Source Candidate Datasets

| Dataset Name | Source | Description / Context | Expected Output Variable |
| :--- | :--- | :--- | :--- |
| **Ecommerce Counterfeit Products Dataset** *(Selected)* | Kaggle | E-commerce product packaging images for general counterfeit detection[cite: 1]. Serves as a primary baseline for packaging signal detection[cite: 1]. | `is_counterfeit` (`0 = Authentic`, `1 = Counterfeit`) |
| **Fake vs Real Medicine Dataset** | Kaggle | High-resolution images of authentic vs. counterfeit medicine packaging[cite: 1]. Structurally similar to regulated agro-inputs[cite: 1]. | `label` (`0 = Real`, `1 = Fake`)[cite: 1] |
| **Real and Fake Images Dataset** | Kaggle | Image forensics and manipulation detection dataset[cite: 1]. | `label` (`0 = Original`, `1 = Manipulated`)[cite: 1] |
| **LogoDet-3K** | Kaggle | Large-scale logo detection dataset with 3,000+ classes[cite: 1]. | `logo_class` (Brand authentication label)[cite: 1] |
| **V2 Plant Seedlings Dataset** | Kaggle | Seedling image classification across 12 crop/weed species[cite: 1]. | `species` (Plant/seed species identifier)[cite: 1] |

---

## 🔍 Selected Dataset & Exploratory Analysis

For this deliverable, we conducted exploratory data analysis on metadata structured after the **Ecommerce Counterfeit Products Dataset** using Google Colab[cite: 1, 3].

### Notebook Summary (`Ecommerce_Counterfeit_Products_Dataset_Exploration.ipynb`)
The primary exploratory notebook addresses all required analytical tasks in individual cells[cite: 3]:

* **Question 3a (Rows & Columns):** Identified total dataset dimensions (`df.shape`)[cite: 3].
* **Question 3b (Data Types):** Verified feature schema and data types using `df.dtypes`[cite: 3].
* **Question 3c (Dataset Completeness):** Checked for null or missing values across all columns[cite: 3].
* **Question 3d (Data Slicing & Concatenation):** Extracted the first 15 rows and last 20 rows, merging them into a unified sample DataFrame (`df_sample`)[cite: 3].

---

## 📁 Repository Structure
```text
SemProject_MLEngine/
│
├── README.md                                                     # Project overview and dataset documentation
└── Ecommerce_Counterfeit_Products_Dataset_Exploration.ipynb      # Deliverable 1 Colab exploration notebook
