# Phishing Website Detection – Research Project

## Introduction
Phishing websites are fake sites designed to look like trusted platforms such as banks, e-commerce portals, or social media pages. Their goal is to trick people into sharing sensitive information like passwords or credit card details.

The purpose of this project is to explore whether machine learning can be used to automatically identify phishing websites and distinguish them from legitimate ones.

## Problem Statement
Phishing is a serious and growing issue because:

- Fake websites are often almost identical to real ones.  
- New phishing sites appear daily, making manual detection nearly impossible.  
- Users can be easily misled, leading to financial loss or identity theft.  

**Research question:** Can we use machine learning techniques to detect phishing sites with high accuracy?

## Approach
The project followed these main steps:

1. **Data Collection:** A dataset of websites labeled as phishing or legitimate, with 28 features such as URL length, use of HTTPS, and presence of suspicious symbols.  
2. **Exploratory Data Analysis (EDA):** Studied patterns in the dataset to understand which features help differentiate phishing from safe websites.  
3. **Feature Selection:** Used Random Forest to rank feature importance and selected the most significant predictors.  
4. **Model Training:** Trained and tested multiple models, including Logistic Regression, Decision Tree, Random Forest, Naive Bayes, Support Vector Machine, and Gradient Boosting.  
5. **Model Evaluation:** Evaluated models using accuracy, precision, recall, and F1-score.  

## Results
The best performing models were:

| Model                  | Accuracy | Precision | Recall | F1-score |
|-------------------------|----------|-----------|--------|----------|
| Random Forest (Bagging) | 89.6%    | 0.90      | 0.90   | 0.90     |
| Gradient Boosting       | 89.4%    | 0.89      | 0.89   | 0.89     |
| Support Vector  (SVC)   | 88.9%    | 0.89      | 0.89   | 0.89     |

Other models such as Logistic Regression and Naive Bayes achieved accuracies in the range of 82–84%.

**Key insight:** Ensemble methods like Random Forest and Gradient Boosting provided the most reliable results for phishing detection.

## How to Run the Project
To reproduce the results locally:

```bash
git clone https://github.com/your-username/PhishingResearch.git
cd PhishingResearch
pip install -r requirements.txt    # if requirements.txt is present
jupyter notebook PhishingResearch.ipynb
