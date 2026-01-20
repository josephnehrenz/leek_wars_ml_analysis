# Project Alpha Strike: Leek Wars Strategic Meta-Analysis

Project Alpha Strike is a comprehensive data engineering and machine learning ecosystem designed to decompose the "Elite Meta" of the AI-programming game, **Leek Wars**. This repository tracks the full lifecycle of the project, from raw API extraction to turn-based win-probability modeling.

---

## 🚀 Project Architecture

The analysis is divided into three modular stages, each represented by a dedicated notebook:

### 1. [Data Collection Engine](leek_wars_data_collection.ipynb)
**The "Factory":** A robust extraction pipeline that interfaces with the Leek Wars REST API.
* **Key Features:** JSON flattening, session management, and rate-limit handling.
* **Output:** Generates `top_builds.csv` (entity meta) and `leek_ai.csv` (1.2M+ rows of turn-by-turn logs).

### 2. [Part 1: Elite Meta Decomposition](part1_meta_decomp.ipynb)
**The "Hardware" Analysis:** An investigation into the equipment choices of the Top 50 global players.
* **Objective:** Identifying dominant weapon/chip archetypes and stat-distribution clusters.
* **Visuals:** Equipment frequency heatmaps and stat-correlation matrices.

### 3. [Part 2: Tactical Win-Prediction](part2_tactic_decomp.ipynb)
**The "Logic" Model:** A machine learning approach to predicting battle outcomes in real-time.
* **Model:** Random Forest Classifier trained on "Strategic DNA" features (HP Deltas, Poison Velocity, Momentum).
* **Interpretability:** Utilizes **SHAP (SHapley Additive exPlanations)** to identify the "Point of No Return" (PONR) in high-level matches.

---

## 📊 Dataset Insights
The data powering this analysis consists of:
* **Entity Profiles:** Detailed stats for the Top 50 Leeks (Cores, RAM, Frequency, and Loadouts).
* **High-Agency Logs:** A refined "Decision-Result" schema that tracks intent rather than just raw damage logs.

| Feature | Description |
| :--- | :--- |
| **Temporal Logic** | Strict index partitioning to prevent "Future Leakage" in models. |
| **Perspective Alignment** | Pairwise mirror systems to calculate relative advantage between opponents. |

---

## 🛠️ Usage
1. **Extraction:** Run `leek_wars_data_collection.ipynb` (requires a valid Leek Wars session token).
2. **Analysis:** Explore the `part1` and `part2` notebooks to view the meta-analysis and model training.
3. **Data:** For users without an API key, the processed datasets are hosted on **[Kaggle: Project Alpha Strike](https://www.kaggle.com/datasets/josephnehrenz/leek-wars-top-50-ai-builds-and-battle-logs)**.

---

## 📈 Key Findings
* Identified the specific turn-count where HP advantage becomes mathematically insurmountable.
* Determined the SHAP global importance of "Status Effect Saturation" vs. "Raw Damage."
