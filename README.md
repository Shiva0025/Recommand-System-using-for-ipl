# 🏏 IPL Fantasy Team Recommendation System

This project builds a **data-driven Fantasy Cricket Team Selector** using IPL (Indian Premier League) data (2008–2020). It combines **machine learning models** and **linear programming optimization** to recommend the best possible playing XI based on predicted batting, bowling, and fielding performance. (SEE PPT INSIDE FOR DETAILED INFO)

## 📌 Features

* **Data Cleaning & Feature Engineering**

  * Processes IPL ball-by-ball and match-level data
  * Computes batting, bowling, and fielding points (strike rate, economy rate, maiden overs, catches, run-outs, etc.)
* **Player Performance Prediction**

  * Uses **Linear Regression, Random Forest, XGBoost, CatBoost, and LSTM models**
  * Predicts future performance scores for players
* **Optimal Team Selection**

  * Uses **PuLP (Linear Programming)** to maximize team points under constraints (team size, roles, budget)
* **Visualization & Analysis**

  * Correlation plots for features
  * Model comparison using Mean Squared Error (MSE)

## 📊 Dataset

The project uses publicly available IPL data (2008–2020):

* **Matches Dataset:** Match details (teams, venue, date, winner)
* **Ball-by-Ball Dataset:** Ball-by-ball events including runs, wickets, extras

Dataset source: [IPL Data (2008-2020)](https://www.kaggle.com/manasgarg/ipl)

## 🧠 Approach

1. **Data Preprocessing**

   * Clean missing values
   * Engineer features for batting (strike rate), bowling (economy rate, wickets), and fielding (catches, run-outs)
2. **Model Training**

   * Train multiple regression models (Linear Regression, Random Forest, XGBoost, CatBoost, LSTM)
   * Evaluate models using MSE
3. **Optimization**

   * Define decision variables for player selection
   * Maximize predicted team score using **PuLP**
   * Apply constraints for team size (11 players) and role balance
4. **Output**

   * Recommended Playing XI with maximum expected score

## 🛠 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/ipl-fantasy-recommendation.git
cd ipl-fantasy-recommendation
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Dependencies include:

* `pandas`, `numpy`, `matplotlib`, `scikit-learn`
* `xgboost`, `catboost`, `pulp`, `tensorflow`

## 🚀 Usage

Run the Jupyter Notebook:

```bash
jupyter notebook rs_projectv5.ipynb
```

Or execute end-to-end training and team selection:

```bash
python main.py
```

You can modify:

* Number of matches considered for recent form
* Model used for prediction (Random Forest / CatBoost / LSTM)
* Team selection constraints (budget, roles)

## 📈 Results

* **CatBoost** and **LSTM models** achieved the lowest MSE for batting and bowling predictions
* The optimization step selects a team with maximum predicted score under constraints
* Visualizations show key factors influencing player points (strike rate, economy, consistency)

## 🏆 Example Output

| Player Name | Role   | Predicted Points |
| ----------- | ------ | ---------------- |
| Player 1    | Batter | 56.3             |
| Player 2    | Bowler | 49.8             |
| ...         | ...    | ...              |

**Total Predicted Team Score:** `X.Y`

---------------------------

