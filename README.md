# Brasileirão 2025 Analysis

An end-to-end data analysis of the 2025 Brazilian Série A (Brasileirão) season, built with Python and Jupyter Notebook.

The project turns raw CSV match data into insights about team performance, home advantage, scoring patterns, finishing efficiency, and matchday revenue.

## Highlights

- **Flamengo** won the 2025 title with **79 points**, pairing the best attack (78 goals) with the best defence (27 conceded).
- Home teams won **1 in 2** matches — more than double the away win rate.
- **2.52 goals per match** on average; **Kaio Jorge** (Cruzeiro) was top scorer with **21 goals**.
- Ball possession correlates positively with points (**r ≈ 0.59**), but does not guarantee wins.
- Flamengo also led matchday revenue as the home club.

## Repository Structure

```
.
├── datasets/                              # Raw CSV data (match info, stats, goals, cards)
├── notebooks/
│   ├── brasileirao_2025_analysis.ipynb    # Main analysis (English, portfolio-focused)
│   └── first.ipynb                        # Study-oriented analysis (Portuguese)
└── scripts/
    ├── build_portfolio_notebook.py        # Generates the portfolio notebook
    └── build_notebook.py                  # Generates the study notebook
```

## Data Sources

| File | Content |
|---|---|
| `campeonato-brasileiro-full.csv` | One row per match (date, teams, scoreline, venue, revenue, etc.) |
| `campeonato-brasileiro-estatisticas-full.csv` | Per-club, per-match statistics (shots, possession, fouls, etc.) |
| `campeonato-brasileiro-gols.csv` | One row per goal (scorer and minute) |
| `campeonato-brasileiro-cartoes.csv` | One row per card issued |

> **Note:** the cards dataset does not cover 2025 matches, so disciplinary analysis was excluded.

## Analysis Sections

1. Data sources and setup
2. Data overview and quality checks
3. Data cleaning and preparation
4. Filtering the 2025 season
5. Final standings computation (round-robin points system)
6. Home advantage
7. Goals analysis (top scorers, goal types, minute distribution)
8. Ball possession vs. points
9. Finishing and goal conversion
10. Matchday revenue by club
11. Conclusions and next steps

## Tech Stack

- Python 3
- pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/Voigtuwu/Brasileirao_20_25_Analysis.git
   cd Brasileirao_20_25_Analysis
   ```

2. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv .venv
   .venv\Scripts\activate   # Windows
   # source .venv/bin/activate  # macOS / Linux
   ```

3. Install the dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter nbformat
   ```

4. Run the notebook:
   ```bash
   jupyter notebook notebooks/brasileirao_2025_analysis.ipynb
   ```

The notebook auto-detects the `datasets/` folder, so it can be executed from either the project root or the `notebooks/` directory.