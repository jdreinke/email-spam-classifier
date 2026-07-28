# Email Spam Classifier - Text Classification Project

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Full%20Notebook-orange.svg)
![ML](https://img.shields.io/badge/Machine%20Learning-Classification-green.svg)

---

## Overview

This project trains and evaluates logistic regression classifier models to create an email spam filter that can automatically identify spam messages in incoming emails . The goal is to deploy a model that accurately distinguishes between legitimate "ham" messages and unwanted "spam" messages.

---

## Key Findings

- **Optimal Model:** The Bigram model with standard threshold achieved the best performance for this use case
- **False Positive Reduction:** Successfully identified all ham messages with the least amount of false positives 
- **Deployment Ready:** Given the results, comfortable deploying this model as a basic spam filter 

> *Most Important Insight: The Bigram model correctly identified all legitimate (ham) messages while minimizing false positives - critical for ensuring important emails aren't accidentally filtered*

---

## Tech Stack

| Category | Tools & Libraries |
|----------|------------------|
| Language | Python 3.x |
| Data Processing | pandas, NumPy |
| Visualization | matplotlib, seaborn |
| Text Vectorization | CountVectorizer, TfidfVectorizer |
| Machine Learning | scikit-learn (LogisticRegression, DummyClassifier) |
| Evaluation Metrics | accuracy_score, precision_score, recall_score, f1_score, confusion_matrix |

---

## Project Structure

```
email-spam-classifier/
├── notebooks/
│   └── Email Spam Classifier.ipynb    # Main analysis notebook
├── data/
│   └── spam.csv                       # Training and test data
├── requirements.txt                   # Python dependencies
├── README.md                          # This file
├── LICENSE                            # License
└── .gitignore
```

---

## Getting Started

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Jupyter Notebook/JupyterLab

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/email-spam-classifier.git
   cd email-spam-classifier
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn numpy cattrs
   ```

4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

5. Open `Email Spam Classifier.ipynb` to run the analysis

---

## Dataset Information

**Dataset Characteristics:**
- **Type:** Text classification (spam vs. ham)
- **Class Distribution:** Unbalanced dataset 
- **Baseline Accuracy:** 87% accuracy achievable with random "ham" guess 

**Data Preprocessing:**
- Text vectorization using CountVectorizer and TfidfVectorizer
- Bigram feature extraction for improved model performance
- Train/test split for model evaluation

---

## Model Performance & Evaluation

### Metrics Used
| Metric | Description |
|--------|-------------|
| **Accuracy** | Overall correctness rate |
| **Precision** | True positive rate (spam correctly identified) |
| **Recall** | Ability to identify all spam messages  |
| **F1 Score** | Harmonic mean of precision and recall  |
| **Confusion Matrix** | Detailed breakdown of predictions |

### Key Results
The Bigram model with standard threshold was selected as optimal because it:
- Correctly identified all ham (legitimate) messages 
- Minimized false positives (important emails incorrectly marked as spam) 
- Balanced the trade-off between catching spam and preserving legitimate communications 

---

## Methodology

1. **Data Loading & Exploration:** Import libraries and load dataset, then inspect to ensure understanding before training models 
2. **Text Vectorization:** Convert text to numerical features using CountVectorizer and TfidfVectorizer
3. **Model Training:** Train logistic regression classifier models with unigram and bigram features
4. **Evaluation:** Compare performance across different configurations (unigram vs. bigram) using recall, F1 score, and other metrics 
5. **Threshold Selection:** Choose optimal threshold based on business requirements (minimize false positives)

---

## Limitations & Future Work

**Current Limitations:**
- Dataset is very small, limiting model generalizability 
- Unbalanced class distribution may affect real-world performance 
- Model trained on limited historical data

**Future Improvements:**
- Train the model on a larger dataset for better generalization 
- Implement A/B testing framework to validate in production
- Add ensemble methods (Random Forest, XGBoost) for comparison
- Incorporate real-time data pipeline for continuous learning
- Expand feature engineering with additional text features

---

## What You'll Learn From This Project

- Text classification fundamentals using scikit-learn
- Handling unbalanced datasets in machine learning
- Feature extraction techniques (CountVectorizer, TfidfVectorizer)
- Model evaluation metrics and their business implications
- Making trade-off decisions based on use case requirements

---

## Contact & Portfolio

- **GitHub:** [@jdreinke](https://github.com/jdreinke)
- **LinkedIn:** in/justinreinke
- **Email:** justinreinke@icloud.com

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

*Last updated: July 2026*