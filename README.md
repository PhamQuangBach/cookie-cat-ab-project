# Cookie Cats A/B Test. Does the Tutorial Gate Matter?

A full end-to-end A/B test analysis on player retention in a mobile puzzle 
game, from statistical testing to a business recommendation.

| | |
|---|---|
| **Dataset** | 90,189 players |
| **Method** | Bootstrap + Chi-squared |
| **Tools** | Python · Tableau |

**Recommendation:** Keep the gate at level 30. Moving it to level 40 led to a statistically significant drop in 7-day retention for mid-core players for a live game.

## Business context

Cookie Cats is a mobile puzzle game where players occasionally hit "gates", forced pauses that require waiting or paying to continue. The game team tested whether moving the first gate from level 30 to level 40 would improve early engagement. This analysis evaluates the experiment and provides a data-driven recommendation.

## Structure

- `notebooks/main.ipynb`: Full analysis with EDA, statistical tests, 
  and visuals
- `data/cookie_cats.csv`: Raw dataset from Kaggle
- `visuals/`: Exported charts used in the Tableau dashboard

## Key findings

- For mid-core player (players who played 30 - 100 rounds) only, Gate 30 outperformed gate 40 on 7-day retention by ~2.18 percentage points
- Bootstrap confidence intervals confirm the difference is not due to chance
- all other player segments for 7-day and 1-day retention showed a smaller, less conclusive gap between groups

## Links

- [Tableau Dashboard](https://public.tableau.com/app/profile/bach.pham3769/viz/ABTestAnalysisonPlayerRetention/Dashboard1)
- [Dataset on Kaggle](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)

## Running the analysis

```bash
pip install -r notebooks/requirements.txt
jupyter notebook notebooks/analysis.ipynb
```