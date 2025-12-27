# Stock Movement Prediction Using News Sentiment and OHLCV Data

## Overview
This project focuses on predicting **next-day stock price direction 
(Up/Down)** by combining:
- Historical market data (OHLCV)
- Financial news sentiment features

The goal is to evaluate whether incorporating sentiment information 
improves predictive performance compared to traditional technical 
indicators alone.

---

## Data Sources
- **Financial News**: 5,842 articles  
- **Stock Market Data (OHLCV)**: 1,259 rows  
- After cleaning and alignment:
  - 1,258 valid stock rows
  - Final dataset: 1,255 samples

---

## Feature Engineering
The final feature set consists of **13 features**, including:

### Technical Indicators
- Moving Averages: MA5, MA20, MA5_ratio  
- Momentum & Volatility: RSI, volatility_5  
- Price-based features: price_range  

### Lagged Features
- close_lag1  
- volume_lag1  

### Sentiment Features
- daily_sentiment  
- sentiment_lag1  

All features were normalized using **StandardScaler**.

---

## Target Variable
- **Binary classification**
  - `1` → Next-day price goes up
  - `0` → Next-day price goes down  
- Dataset balance: ~53% Up / 47% Down  
- **Chronological split**:
  - Train: 70%
  - Validation: 15%
  - Test: 15%

---

## Models Evaluated
- Logistic Regression (baseline)
- Support Vector Machine (RBF kernel)
- XGBoost
- LSTM (deep learning)

---

## Results
| Model | Accuracy | F1-score |
|------|----------|----------|
| Logistic Regression | 0.413 | 0.165 |
| **SVM (RBF)** | **0.624** | **0.769** |
| XGBoost | 0.497 | 0.554 |
| LSTM | 0.374 | 0.051 |

**Best model:** Support Vector Machine (RBF)  
- Achieved the highest F1-score
- Demonstrated strong performance on non-linear tabular data

---

## Key Findings
- SVM outperformed deep learning models on structured tabular data
- Sentiment features contributed to performance improvement
- Classical ML models can outperform neural networks in small-to-medium 
datasets

---

## Paper Status
This project is documented in an **IEEE-format conference paper**.

**Status:** *Under Review*  
(The paper has been submitted to an IEEE conference and is currently under 
peer review.)

> The final published version (if accepted) will be linked here once 
available.

---

## Repository Contents
- `ML_Project_All_Phase.ipynb` – Full pipeline and experiments
- `cleaned_news.csv` – Cleaned news sentiment data
- `cleaned_stock.csv` – Cleaned OHLCV data
- `system-diagram.png` – Project pipeline diagram
- `Presentation ML.pdf` – Project presentation (PDF version)
- `.gitignore` – Ignored files configuration

---

## How to Run
```bash
pip install -r requirements.txt
# Stock Movement Prediction Using News Sentiment and OHLCV Data

## Overview
This project focuses on predicting **next-day stock price direction 
(Up/Down)** by combining:
- Historical market data (OHLCV)
- Financial news sentiment features

The goal is to evaluate whether incorporating sentiment information 
improves predictive performance compared to traditional technical 
indicators alone.

---

## Data Sources
- **Financial News**: 5,842 articles  
- **Stock Market Data (OHLCV)**: 1,259 rows  
- After cleaning and alignment:
  - 1,258 valid stock rows
  - Final dataset: 1,255 samples

---

## Feature Engineering
The final feature set consists of **13 features**, including:

### Technical Indicators
- Moving Averages: MA5, MA20, MA5_ratio  
- Momentum & Volatility: RSI, volatility_5  
- Price-based features: price_range  

### Lagged Features
- close_lag1  
- volume_lag1  

### Sentiment Features
- daily_sentiment  
- sentiment_lag1  

All features were normalized using **StandardScaler**.

---

## Target Variable
- **Binary classification**
  - `1` → Next-day price goes up
  - `0` → Next-day price goes down  
- Dataset balance: ~53% Up / 47% Down  
- **Chronological split**:
  - Train: 70%
  - Validation: 15%
  - Test: 15%

---

## Models Evaluated
- Logistic Regression (baseline)
- Support Vector Machine (RBF kernel)
- XGBoost
- LSTM (deep learning)

---

## Results
| Model | Accuracy | F1-score |
|------|----------|----------|
| Logistic Regression | 0.413 | 0.165 |
| **SVM (RBF)** | **0.624** | **0.769** |
| XGBoost | 0.497 | 0.554 |
| LSTM | 0.374 | 0.051 |

**Best model:** Support Vector Machine (RBF)  
- Achieved the highest F1-score
- Demonstrated strong performance on non-linear tabular data

---

## Key Findings
- SVM outperformed deep learning models on structured tabular data
- Sentiment features contributed to performance improvement
- Classical ML models can outperform neural networks in small-to-medium 
datasets

---

## Paper Status
This project is documented in an **IEEE-format conference paper**.

**Status:** *Under Review*  
(The paper has been submitted to an IEEE conference and is currently under 
peer review.)

> The final published version (if accepted) will be linked here once 
available.

---

## Repository Contents
- `ML_Project_All_Phase.ipynb` – Full pipeline and experiments
- `cleaned_news.csv` – Cleaned news sentiment data
- `cleaned_stock.csv` – Cleaned OHLCV data
- `system-diagram.png` – Project pipeline diagram
- `Presentation ML.pdf` – Project presentation (PDF version)
- `.gitignore` – Ignored files configuration

---

## How to Run
```bash
pip install -r requirements.txt
:
ML_Project_All_Phase.ipynb


Team
(Will be added after paper review decision)

Disclaimer
This project is for academic and research purposes only and does not 
constitute financial or investment advice
