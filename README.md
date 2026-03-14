📈 Crypto Market Microstructure & Behavioral Analysis
Uncovering Algorithmic Trading Patterns and Predicting Trade Success using Machine Learning

📊 Executive Summary
This project analyzes a high-frequency, tick-level dataset of 184,263 cryptocurrency trades executed on the Hyperliquid exchange during a highly volatile 6-day market window. By merging execution data with macroeconomic sentiment (Bitcoin Fear & Greed Index), this project tests classical behavioral finance theories (FOMO, Disposition Effect) against hard quantitative data.

Using a combination of Descriptive Analytics, Unsupervised Clustering (K-Means), and Supervised Machine Learning (XGBoost), the analysis reveals that this specific market environment was dominated by algorithmic scalpers exhibiting ruthless risk management, directly contradicting typical human trading psychology.

🧠 Key Discoveries & Quantitative Insights
1. The "Smart Money" Paradox (Asymmetric Risk)
Amateur traders often seek a high win rate. This data proves that professional profitability relies on risk asymmetry, not win probability.

The overall portfolio maintained a 42.0% win rate but generated exponential cumulative PnL.

K-Means Clustering identified a "Smart Money" cohort that won only 37% of their trades but generated $768k in profit, compared to the "Retail Crowd" who won 69% of the time but generated half the profit.

2. Myth-Busting Behavioral Finance
Classical theories suggest retail traders hold losers too long (Disposition Effect) and buy the top (FOMO). The data definitively disproved this for this dataset:

Strict Stop-Loss Execution: Retail traders averaged a $37.90 win but only a $4.36 loss (a 1:9 Loss-to-Win ratio). Whales averaged a $1,600 win against a $219 loss.

The Inference: Humans do not take $4 losses. This mathematical signature strongly indicates the presence of High-Frequency Trading (HFT) bots and algorithmic scalpers executing hard stop-losses the millisecond a trade turns against them.

3. Predictive Modeling (Alpha Generation)
An XGBoost Classifier was trained to predict whether a trade would result in a win or loss based purely on behavioral features (Leverage, Position Size, Trade Direction, Market Sentiment).

Accuracy: The model achieved a statistically significant 66.06% accuracy in predicting trade outcomes before they closed.

SHAP Explainability:  SHAP value analysis mathematically proved that high leverage was the single strongest predictor of a losing trade, while trading with the macroeconomic trend (Shorting during "Fear") was the strongest predictor of a win.

🛠️ Technical Architecture
Data Engineering: Time-series alignment of Unix epoch millisecond tick data with daily macroeconomic sentiment classifications using Pandas.

Descriptive Visualizations: Advanced financial charting (Violin plots, Cumulative PnL curves, PnL distributions) using Matplotlib and Seaborn.

Unsupervised ML: Feature scaling and K-Means Clustering (scikit-learn) to profile and segment trader accounts into distinct behavioral cohorts.

Predictive ML: XGBoost classification to predict binary trade outcomes (is_win).

Explainable AI: SHAP (SHapley Additive exPlanations) to interpret the machine learning model and quantify feature importance.

🚀 How to Run the Analysis
Clone this repository.

Ensure you have the required libraries installed:

Bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap
Place the Hyperliquid_Trades.csv and Fear_Greed_Index.csv files in the root directory.


👨‍💻 Author
Suman Patel
Quantitative Data Analyst / Data Scientist
