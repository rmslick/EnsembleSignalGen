
# Financial Trading Signal Classification Algorithm

## Overview
This algorithm uses a combination of advanced machine learning techniques and feature engineering to classify trading signals (Buy, Sell) based on historical market data and financial indicators. It integrates technical indicators, market sentiment, and earnings data to provide robust and actionable predictions. 

### Key Features:
1. **Data Integration**:
   - Historical stock data (price, volume, returns).
   - Market-level data (e.g., S&P 500 returns, VIX changes).
   - Earnings data, including EPS and revenue surprises.

2. **Feature Engineering**:
   - Technical indicators: RSI, SMA Crossover, VWMA, and more.
   - Nonlinear interactions: Polynomial expansions and feature multiplications.
   - Relative strength indicators and trend-based signals.

3. **Machine Learning**:
   - Hyperparameter-optimized ensemble models (Random Forest, Gradient Boosting, LightGBM).
   - Ensemble Voting Classifier to aggregate predictions for improved accuracy.

4. **Handling Imbalances**:
   - SMOTE (Synthetic Minority Over-sampling Technique) ensures balanced datasets for training.

### Training Results
#### Latest Classification Report:
```
              precision    recall  f1-score   support

          -1       0.79      0.78      0.78       317
           1       0.77      0.79      0.78       309

    accuracy                           0.78       626
   macro avg       0.78      0.78      0.78       626
weighted avg       0.78      0.78      0.78       626
```

#### Latest Confusion Matrix:
```
[[246  71]
 [ 66 243]]
```

### Usage
1. **Data Preparation**:
   - Fetch stock, market, and earnings data using integrated APIs.
   - Ensure sufficient historical data for feature engineering.

2. **Training and Testing**:
   - Split data into training and testing sets.
   - Train ensemble models with optimized hyperparameters.

3. **Evaluation**:
   - Generate classification reports and evaluate precision, recall, and F1-score.
   - Assess feature importance and refine features iteratively.

4. **Deployment**:
   - Use the trained ensemble model for real-time or batch prediction of trading signals.

### Future Improvements
- Incorporating sentiment analysis and macroeconomic indicators.
- Expanding features with earnings release sentiment and market conditions.
- Exploring deep learning architectures for sequential pattern recognition.

---

## Requirements
- Python 3.x
- Libraries: `pandas`, `numpy`, `scikit-learn`, `lightgbm`, `imblearn`, `yfinance`, `ta`
- API Keys for data sources (e.g., Alpha Vantage, Financial Modeling Prep).

---

## Disclaimer
This algorithm is for educational and research purposes only. Trading involves substantial risk, and past performance does not guarantee future results.
