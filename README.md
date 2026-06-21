# 🛒 E-Commerce Purchase Intention Prediction

Predicting whether an online shopping session ends in a purchase, using browsing-behaviour data and six classification models.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Scikit--learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-blue?style=flat)
![RapidMiner](https://img.shields.io/badge/RapidMiner-grey?style=flat)

## 📌 Overview
Online retailers can't ask shoppers "are you going to buy this?" — but their clickstream tells you anyway. This project uses session-level browsing data (page types visited, time spent, bounce/exit rates, special-day proximity, etc.) to predict purchase intent, and compares how different model families perform on an imbalanced classification problem.

## 📊 Dataset
- **Source:** UCI Machine Learning Repository — Online Shoppers Purchasing Intention Dataset
- **Size:** 12,330 sessions, 18 features
- **Target:** `Revenue` (purchase made: True/False) — imbalanced, ~85% no-purchase

## 🛠️ Tools & Technologies
Python (pandas, scikit-learn, XGBoost), RapidMiner (used for a parallel data-mining workflow), Jupyter Notebook

## 🔍 Approach
1. EDA on session attributes: page duration, bounce rate, exit rate, traffic type, visitor type, weekend/special-day effects
2. Preprocessing: encoding categorical features, handling class imbalance
3. Trained and compared 6 classifiers: Logistic Regression, Decision Tree, Random Forest, MLP, SVM, XGBoost
4. Evaluated using Accuracy, Precision, Recall, F1, and ROC-AUC (Accuracy alone is misleading on imbalanced data)

## 📈 Results

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---|---|---|---|---|
| **Random Forest** | **90.1%** | 0.736 | 0.563 | 0.638 | **0.916** |
| MLP Classifier | 88.5% | 0.65 | 0.52 | 0.58 | – |
| XGBoost | 89.0% | 0.67 | 0.56 | 0.61 | – |
| SVM | 88.0% | 0.71 | 0.43 | 0.53 | – |
| Logistic Regression | 88.3% | 0.764 | 0.356 | 0.486 | 0.865 |
| Decision Tree | 85.2% | 0.522 | 0.529 | 0.525 | 0.720 |

Random Forest came out on top on both overall accuracy and ROC-AUC, with the best balance of precision and recall on the minority (purchase) class.

## 📁 Repository Contents
| File | Description |
|---|---|
| `Data_Mining_final_code.ipynb` | Full Python pipeline (EDA → modeling → evaluation) |
| `data mining.rmp` | RapidMiner workflow |
| `online_shoppers_intention.csv` / `data mining .csv` | Dataset |
| `Presentation - Data Mining.pptx` | Project presentation |
| `Ecommerce purchase Intention prediction...pdf` | Full report |

## 👤 Author
**Harsanbruno Maria Joseph Esuraj** — MSc Data Analytics, Dublin Business School
[LinkedIn](https://linkedin.com/in/harsanbruno) · [GitHub](https://github.com/harsanbruno2003-glitch)
