# Project Alpha Strike: Leek Wars Strategic Intelligence Suite

[![Kaggle Dataset](https://img.shields.io/badge/Kaggle-Data_Collection-white?logo=kaggle)](https://www.kaggle.com/datasets/josephnehrenz/leek-wars-top-50-ai-builds-and-battle-logs)<br>
[![Kaggle Part 1](https://img.shields.io/badge/Kaggle-Part_1:_Meta_Decomposition-blue?logo=kaggle)](https://www.kaggle.com/code/josephnehrenz/project-alpha-strike-p1-elite-meta-decomposition)<br>
[![Kaggle Part 2](https://img.shields.io/badge/Kaggle-Part_2:_Tactical_Modeling-gold?logo=kaggle)](https://www.kaggle.com/code/josephnehrenz/project-alpha-strike-p2-modeling-the-point-of-no-return)

An end-to-end data engineering and machine learning ecosystem designed to decode the "Elite Meta" of the AI-programming game, **Leek Wars**. This project deconstructs the hardware (builds) and software (tactics) of the Top 50 global players using XGBoost, Random Forest, and SHAP interpretability.

---

## Project Architecture

The project is structured into three modular stages, moving from raw data extraction to predictive tactical modeling.

### 1. [Data Collection Engine](leek_wars_data_collection.ipynb)
**The "Factory":** A robust pipeline interfacing with the Leek Wars REST API.
- **Complexity:** Flattens deeply nested JSON battle logs into a 1.2M+ row tabular "Decision-Result" schema.
- **Engineered Features:** Mapping numeric equipment IDs to semantic names and tracking "State-at-Time" HP/TP/MP metrics.

### 2. [Part 1: Elite Meta Decomposition](part1_meta_decomp.ipynb)
**The "Hardware" Analysis:** Decodes the equipment and stat synergies of the Top 50 global entities.
- **Key Insight:** The discovery of the **"Spiky Tank"** — a hybrid build prioritizing *Agility* and *Savant Bulb* for retribution damage over pure mitigation.
- **Top Predictors:** Identified *Motherboard 3* and *Frequency* as the primary gatekeepers of the Top 10 rank.

### 3. [Part 2: Tactical Win-Prediction](part2_tactic_decomp.ipynb)
**The "Execution" Model:** A predictive engine that identifies the tactical triggers of victory.
- **The Point of No Return (PONR):** Model reveals that matches reach an 80% certainty threshold by **Turn 2.7**.
- **Metrics:** Achieves **88.7% test accuracy** in predicting match outcomes based on turn-by-turn "Strategic DNA."

---

## Strategic Findings

### The "Unbeatable" Blueprint (Build Meta)
| Synergy | Archetype | Interpretation |
| :--- | :--- | :--- |
| **Freq × EHP** | The First Word | High Frequency allows defensive setup before the first enemy strike. |
| **Agility × Savant** | The Nova-Assassin | High Agility scales "Damage Return," making every enemy attack a self-inflicted wound. |
| **Adrenaline × EHP** | The Infinite Turn | High HP acts as fuel to stay alive for repeated Adrenaline (extra TP) triggers. |

### Tactical Breakpoints (Execution Meta)
- **Opening Buff Threshold:** Achieving 5 specific core buffs in the opening turns is statistically mandatory for a winning probability profile.
- **TP Efficiency:** Leaving even 1–2 TP unspent is the most consistent precursor to "Probability Decay" in elite brackets.
- **Volatility Control:** Top 10 players minimize "Tug-of-War" scenarios, using control chips to ensure a smooth, upward win-probability climb.

---

## Technical Stack
- **Languages:** Python (Pandas, NumPy)
- **Machine Learning:** XGBoost, Random Forest, SHAP (Explainable AI)
- **Data Engineering:** REST API Integration, JSON Normalization, Time-Series Feature Engineering
- **Visualization:** Matplotlib, Seaborn

---

## Key Features & Insights

### Top Model Drivers (The "Hardware" Meta)
1. **Mobility Scaling** – _Agility_ and _MP_ are the strongest predictors of rank. The elite meta rejects "Slow Tanks" in favor of "Spiky Tanks" that punish attackers.
2. **Action Economy** – _Frequency_ and _Adrenaline_ determine turn priority and quantity. At Level 301, the game is won by the Leek that can cycle the most actions.
3. **Hardware Capacity** – _Motherboard 3_ serves as a binary gatekeeper; without the slot capacity for elite chip synergies, a Leek's rank is mathematically capped.

### Execution Meta (The "Software" Tactics)
1. **The 2.7 Turn Breakpoint** – 80% of match outcomes are determined before Turn 3. The "Opening 5 Buff" threshold is a critical indicator of victory.
2. **TP Efficiency** – Winners maintain near 100% TP expenditure. Leaving even 1-2 TP unspent is the most consistent precursor to a "Probability Decay."
3. **Volatility Control** – Elite players use "Suffocation Logic" (_Tranquilizer_/_Soporific_) to minimize tug-of-war scenarios and ensure a smooth win-probability climb.

---

## Value to the Player/Developer
1. **Strategic Optimization:** Provides a statistically verified blueprint for stat distribution and chip selection.
2. **Script Auditing:** Allows developers to test their AI scripts against a "Win Probability" model to find tactical leaks in their code.
3. **Explainable AI:** Uses SHAP waterfall plots to show exactly *why* a specific turn led to a loss, moving beyond simple trial-and-error.

---

## Project Structure
```text
leek_wars_ml_analysis/
├── leek_wars_data_collection.ipynb  # API Extraction & JSON Flattening
├── part1_meta_decomp.ipynb          # Hardware & Synergy Analysis
├── part2_tactic_decomp.ipynb        # Predictive Modeling & PONR Analysis
└── README.md                        # Project Documentation
```

---

## Contributing

Feel free to fork this project and submit pull requests for any improvements!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

*Built out of curiosity for the fun and appreciation of the Leek Wars website - a great product and a fantastic resource for beginning and seasoned programmers alike, featuring common structures shared by many languages and supported by a helpful community.*

**Explore the Game:** [Leek Wars](https://leekwars.com/)  
**Join the Fight:** [Referral Link](https://leekwars.com/godfather/Newton)
