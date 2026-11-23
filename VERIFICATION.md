# Verification

Checked on 2026-11-23 during portfolio cleanup.

- All 22 notebook cells executed successfully in a separate local test copy using the supplied `student-mat.csv`.
- Dataset shape: 395 rows, 33 original columns. Dataset bytes are not included in this repository.
- Stratified holdout: 316 training rows and 79 test rows; random seed 42.
- Depth-4 decision tree holdout accuracy: 0.8481012658227848 (84.81%).
- Class support on holdout: advanced 15, remedial 26, standard 38.
- This rerun used Python 3.10.12, scikit-learn 1.7.2, pandas 2.3.3, NumPy 2.2.6. It is not a cross-version reproducibility guarantee.
- The public notebook remains output-free. No raw student previews, executed notebook or dataset is committed.

The target is a grade band derived from G3. G1 and G2 are predictors. The result is not evidence that teaching recommendations improve learning, and it is not an early-warning model before earlier grades are available. No cross-school validation, fairness audit or production deployment was performed.
