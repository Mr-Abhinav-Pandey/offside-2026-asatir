# OffSide 2026 Football Analytics Challenge

## Team <Team Name>

### Team Members

* Abhinav
* <Teammate Name>

---

## Overview

This repository contains our solution for the **OffSide 2026 Football Analytics Challenge**, organized by IEEE Computer Society MUJ.

The objective of the competition is to predict whether a player will score at least one goal in a football match using player profiles, market intelligence, match context, and advanced football analytics features.

The challenge dataset contains over **1.88 million player-match observations**, spanning multiple competitions, teams, and seasons.

---

## Problem Statement

Given historical football data and player attributes, predict the probability that a player scores at least one goal in a match.

### Target Variable

`scored_flag`

* 0 → Player did not score
* 1 → Player scored at least one goal

### Evaluation Metric

Average Precision (AP)

The competition uses AP because goal-scoring events are relatively rare, making the dataset highly imbalanced.

---

## Dataset Summary

* Total Records: 1,885,448+
* Features: 60+
* Players: 47,690
* Teams: 299
* Competitions: 67

### Major Feature Groups

#### Player Profile

* Age
* Height
* Preferred Foot
* Position
* Nationality

#### Market Intelligence

* Market Value
* Peak Market Value
* Value Ratios
* Market Value Tier

#### International Experience

* International Caps
* International Goals
* Goal per Cap

#### Advanced Analytics

* Expected Goals (xG)
* Expected Assists (xA)
* Non-Penalty xG
* xGChain
* xGBuildup

#### Match Context

* Competition Type
* Country
* Stadium
* Attendance
* Home/Away Status

---

## Approach

### 1. Data Preprocessing

* Missing value handling
* Data type correction
* Categorical feature processing
* Feature consistency checks
* Memory optimization

### 2. Feature Engineering

Created and analyzed features based on:

* Market value dynamics
* Age and experience
* Positional information
* Playing time
* Advanced analytics metrics
* Goal-scoring indicators
* Match participation characteristics

### 3. Validation Strategy

To avoid data leakage and ensure robust evaluation:

* Group-based cross validation
* Stratified target distribution monitoring
* Fold-wise AP tracking

### 4. Models Used

#### CatBoost

* Native categorical handling
* Robust performance on tabular data
* Fast experimentation cycle

#### LightGBM

* Gradient boosting framework
* Efficient training on large datasets
* Feature importance analysis

#### Ensemble

* Weighted averaging of model predictions
* Improved leaderboard stability

---

## Repository Structure

```text
.
├── data/
├── notebooks/
├── src/
├── submissions/
├── ppt/
├── README.md
└── requirements.txt
```

---

## Reproducibility

### Installation

```bash
pip install -r requirements.txt
```

### Training

```bash
python src/train.py
```

### Inference

```bash
python src/inference.py
```

---

## Results

| Model    | Validation AP |
| -------- | ------------- |
| CatBoost | TBD           |
| LightGBM | TBD           |
| Ensemble | TBD           |

---

## Key Insights

* Expected Goals (xG) is among the strongest predictors of future scoring.
* Player role and position significantly influence scoring probability.
* Market value captures long-term player quality and performance.
* Playing time and starting status are critical indicators.
* Advanced analytics provide stronger signals than traditional statistics alone.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* CatBoost
* LightGBM
* Matplotlib
* Seaborn

---

## Competition

OffSide 2026 Football Analytics Challenge

Organized by IEEE Computer Society MUJ

---

## Acknowledgements

We thank the organizers for providing a comprehensive football analytics dataset and an engaging machine learning challenge that combines sports analytics with predictive modeling.
