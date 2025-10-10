# ML2 — Classification Task: Predicting Tax Avoidance Categories

This repository contains a **ready-to-run Jupyter Notebook** for the extra-points assignment.

## How to use
1. Put your data files into `data/`:
   - `data/train_fe.csv`
   - `data/test_fe.csv`

2. Open the notebook: `ml2_tax_avoidance_classification.ipynb`  
   **Run all cells top-to-bottom.**

3. Outputs:
   - Model selection based on **Macro F1** (primary metric).
   - Final evaluation on the test set: **Accuracy, per-class Precision/Recall/F1, Confusion Matrix**.
   - Best model saved to `models/best_model.pkl` (and `models/preprocessor.pkl` if used).

## Repo layout
```
ML2-tax-avoidance/
├── ml2_tax_avoidance_classification.ipynb
├── data/
│   ├── train_fe.csv        # <-- place here
│   └── test_fe.csv         # <-- place here
├── models/
│   ├── .gitkeep
└── README.md
```

## Notes
- Target classes from ETR thresholds (per instructions):
  - **Class 0 (Low Tax Avoidance):** ETR > 0.25
  - **Class 1 (Medium Tax Avoidance):** 0.15 < ETR ≤ 0.25
  - **Class 2 (High Tax Avoidance):** ETR ≤ 0.15
- The notebook uses **TimeSeriesSplit** for CV, **GridSearchCV** for tuning, and compares **Logistic Regression**, **KNN**, and **SVC**.
