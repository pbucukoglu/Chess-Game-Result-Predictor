# Chess Game Result Predictor

This project predicts the outcome of a chess game—whether White wins, Black wins, or the game ends in a draw—using machine learning classification techniques.

## 📌 Overview
- The dataset is sourced from Kaggle and consists of **17,700** chess games after preprocessing.
- Features include player ratings, game type (rated/unrated), number of moves, and opening codes.
- Machine learning models used: **Logistic Regression, k-Nearest Neighbors (kNN), Random Forest, Support Vector Machines (SVM)**.
- Achieved a maximum accuracy of **61%**, which aligns with similar studies.
- Predicting **draws** remains a significant challenge due to dataset imbalance and the lack of detailed positional data.

## 🔍 Dataset
- **Source**: [Kaggle Chess Game Dataset](https://www.kaggle.com/datasets/datasnaek/chess)
- **Size**: 20,000 games (reduced to 17,700 after cleaning)
- **Selected Features**:
  - **White/Black Player Rating**
  - **Rating Difference**
  - **Number of Moves**
  - **Opening Code (ECO)**

- **Excluded Features**:
  - Move sequences (board state analysis was out of scope)
  - Time control information
  - Player IDs

## 📊 Model Performance
| Model                 | Accuracy | Draw Prediction F1-score |
|-----------------------|----------|--------------------------|
| k-Nearest Neighbors  | 59%      | 0.00                     |
| Logistic Regression  | 61%      | 0.02                     |
| Random Forest        | 61%      | 0.04                     |
| Support Vector Machines | 61%  | 0.00                     |

- Draws were the hardest to predict due to class imbalance.
- Class weighting and oversampling techniques were tested but had limited success.

## ⚙️ Installation & Usage
### Prerequisites
- Python 3.8+
- Jupyter Notebook
- Required libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

### Setup
1. Clone this repository:
   ```sh
   git clone https://github.com/pbucukoglu/chess-game-result-predictor.git
   cd chess-game-result-predictor
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the notebook:
   ```sh
   jupyter notebook ChessGameResultPredictor.ipynb
   ```

## 📖 Project Structure
```
📂 chess-game-result-predictor
│── 📄 ChessGameResultPredictor.ipynb   # Jupyter Notebook with the analysis
│── 📄 README.md                        # Project documentation
│── 📂 data/                             # Dataset (if needed)
│── 📂 models/                           # Saved models
│── 📄 requirements.txt                   # Required Python packages
```

## 🔥 Future Work
- Integrating **deep learning** for move sequence analysis.
- Addressing **draw prediction** with additional board state features.
- Experimenting with **ensemble methods** to improve accuracy.

## 📜 References
1. Drezewski & Wator (2021) - Chess outcome prediction using deep learning.
2. Mujagić et al. (2024) - Machine learning techniques for chess performance analysis.
3. Thabtah et al. (2020) - Elo-based chess game result predictions.
