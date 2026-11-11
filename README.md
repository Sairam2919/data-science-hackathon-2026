# data-science-hackathon-2026
# H1N1 Vaccine Acceptance & Municipal Cost Optimization

An end-to-end data science pipeline predicting H1N1 vaccine acceptance (2009 pandemic survey data). Beyond standard ROC-AUC metrics, models are optimized against a **custom municipal financial cost function** ($500 vaccine baseline vs. $25,000 hospitalization risk).

---

## Economic Logic & Cost Function
Because severe hospitalization ($25,000) is 50x more costly than a wasted vaccine ($500), our pipeline lowers decision thresholds ($\tau$) to maximize **Recall (~99%+)**, minimizing overall public health expenditure and preventing severe outbreaks.

---

## Key Pipeline Steps
1. **Feature Engineering:** Created composite indicators (`total_behavioral_precautions`, `risk_concern_score`, `total_household_size`).
2. **Preprocessing:** Robust imputation (Median for numeric, Mode for categorical) + One-Hot Encoding via Scikit-Learn `ColumnTransformer`.
3. **Model Benchmarking:** Evaluated 5 classifiers using **5-Fold Stratified Cross-Validation** (~0.82+ ROC-AUC).
4. **Export:** Generated and verified 5 unique test submission CSVs (`challenge_submission_group_1_order_1.csv` through `_5.csv`).

---

