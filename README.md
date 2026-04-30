<div align="center">

# 💰 Multiple Linear Regression — Income Prediction

### Predicting income from age and experience using 5 ML models

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4-orange?logo=scikitlearn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

</div>

---

## 📖 Overview

This project explores **multiple linear regression** by predicting a person's **income** based on their **age** and **years of experience**.

It trains and compares **5 different machine learning models** to find which one fits the data best — and walks through the full ML workflow with detailed explanations in every step.

> 🎯 **Best result:** Linear Regression achieved an **R² score of 0.94** — explaining 94% of the variance in income.

---

## 🚀 Quick Start

### Prerequisites
- Python 3.10 or higher
- pip (Python package manager)
- Jupyter Notebook

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Gautam-Santosh/Multiple-Linear-Regression.git
cd Multiple-Linear-Regression

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter
jupyter notebook
```

Then open `Multiple_Linear_Regression_documented.ipynb` and run all cells. ✅

---

## 🧠 Models Compared

| # | Model | Type | Best For |
|---|-------|------|----------|
| 1 | **Linear Regression** ⭐ | Linear | Data with linear relationships |
| 2 | **Random Forest** | Ensemble | Non-linear patterns, larger datasets |
| 3 | **Decision Tree** | Tree-based | Quick interpretable predictions |
| 4 | **Support Vector Regression (SVR)** | Kernel-based | Complex boundaries (needs scaling) |
| 5 | **Gaussian Naive Bayes** | Probabilistic | Classification only (tested for comparison) |

---

## 📊 Results

| Model | R² Score | Verdict |
|-------|---------:|---------|
| 🥇 **Linear Regression** | **0.94** | Excellent ✅ |
| 🥈 **Random Forest** | 0.68 | Decent |
| 🥉 **Decision Tree** | 0.30 | Poor |
| ❌ Naive Bayes | -1.37 | Wrong tool for regression |
| ❌ SVR | -4.59 | Needs feature scaling |

### 🎯 Key Insight

> **Match the algorithm to the problem.**
> Income vs experience is a **linear relationship** → simple Linear Regression wins easily.
> Complex models (Random Forest, SVR) need more data and tuning to shine.

---

## 📁 Project Structure

```
Multiple-Linear-Regression/
│
├── 📓 Multiple_Linear_Regression_documented.ipynb   # Main notebook (with explanations)
├── 📄 README.md                                     # This file
├── 📦 requirements.txt                              # Python dependencies
├── 🚫 .gitignore                                    # Files Git should ignore
│
├── 📂 data/
│   └── multiple_linear_regression_dataset.csv      # Training data (20 rows × 3 cols)
│
└── 📂 models/                                       # Trained & saved models
    ├── lr.pkl       # Linear Regression
    ├── rf.pkl       # Random Forest
    ├── dt.pkl       # Decision Tree
    ├── svr.pkl      # Support Vector Regression
    └── gnb.pkl      # Gaussian Naive Bayes
```

---

## 🛠️ Workflow

```mermaid
graph LR
    A[Load Data] --> B[Explore]
    B --> C[Split Train/Test]
    C --> D[Train 5 Models]
    D --> E[Evaluate with R²]
    E --> F[Save Best Model]
    F --> G[Make Predictions]
```

### Step-by-step breakdown

| Step | Action | Tool |
|------|--------|------|
| 1 | Load CSV into a DataFrame | `pandas` |
| 2 | Check shape, columns, sample rows | `pandas` |
| 3 | Split into features (X) and target (y) | `sklearn.model_selection` |
| 4 | Train 5 different ML models | `sklearn` |
| 5 | Measure accuracy with R², MAE, MSE | `sklearn.metrics` |
| 6 | Save trained models as `.pkl` files | `joblib` |
| 7 | Visualize predictions and scores | `matplotlib`, `seaborn` |
| 8 | Load best model & predict on new data | `joblib` |

---

## 📦 Dataset

A small dataset of **20 individuals** with three features:

| Column | Description | Type |
|--------|-------------|------|
| `age` | Age in years | int |
| `experience` | Years of work experience | int |
| `income` | Annual income (target variable) | int |

### Sample data

| age | experience | income |
|----:|-----------:|-------:|
| 25 | 1 | 30,450 |
| 30 | 3 | 35,670 |
| 47 | 2 | 31,580 |
| 32 | 5 | 40,130 |
| 43 | 10 | 47,830 |

---

## 🧰 Tech Stack

- **Language:** Python 3.10+
- **Data handling:** pandas, numpy
- **ML algorithms:** scikit-learn
- **Visualization:** matplotlib, seaborn
- **Model persistence:** joblib
- **Environment:** Jupyter Notebook

---

## 📈 Sample Visualizations

The notebook includes:

- 📉 **Line plot** — R² score across all 5 models
- 📊 **Bar chart** — color-coded model comparison (green = good, red = bad)
- 🎯 **Scatter plot** — actual vs predicted income values

---

## 🔮 Future Improvements

- [ ] Apply **feature scaling** (StandardScaler) to fix SVR performance
- [ ] Use **cross-validation** instead of single train/test split (better for small data)
- [ ] Try **hyperparameter tuning** with GridSearchCV
- [ ] Add more features (education level, industry, location)
- [ ] Test on a larger dataset (1000+ rows)
- [ ] Deploy the best model as a **Flask/FastAPI web app**

---

## 📚 What I Learned

- ✅ The full ML workflow from data loading to deployment
- ✅ How to compare multiple models with R², MAE, MSE
- ✅ When to use linear vs non-linear algorithms
- ✅ How to save/load trained models with `joblib`
- ✅ The importance of matching the **algorithm to the data**
- ✅ Why small datasets favor simpler models

---

## 🤝 Contributing

Suggestions, improvements, and pull requests are welcome! Feel free to:

1. ⭐ **Star** this repo if you found it helpful
2. 🍴 **Fork** it to experiment on your own
3. 🐛 **Open an issue** if you spot a bug or have ideas

---

## 📬 Contact

**Gautam Santosh**

- GitHub: [@Gautam-Santosh](https://github.com/Gautam-Santosh)

---

<div align="center">

⭐ **If this project helped you, give it a star!** ⭐

*Made with ❤️ and lots of debugging*

</div>
