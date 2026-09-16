# Week 4 — Model Selection and Evaluation Plan

**Project:** Spam Email Prediction using Machine Learning
**Role:** Python Specialist Intern (Data Science)
**Deliverable:** `Week4_Model_Selection_and_Evaluation_Plan.docx`

## Purpose

Move from features to a defensible final model, with an evaluation plan built around the real cost
of errors in a spam filter, not raw accuracy.

## What This Week Covers

- **Model Selection Criteria** — weighted criteria for choosing an algorithm, and the data
  characteristics (short, sparse, imbalanced text) that constrain the choice.
- **Candidate Algorithms** — a majority-class baseline, Multinomial Naive Bayes, Logistic Regression,
  Linear SVM, Random Forest, and Gradient Boosting as a supplementary candidate, plus a section on
  approaches that were rejected and why.
- **Evaluation Metrics** — the confusion matrix, a metric hierarchy, and an explicit argument for
  demoting accuracy given class imbalance (precision on the spam class is prioritised, since a false
  positive — a real message marked spam — is costlier than a missed spam message).
- **Validation Strategy** — a three-way train/validation/test split, stratified k-fold
  cross-validation, learning and validation curves, and a cross-corpus generalisation test against
  the Enron-Spam dataset.
- **Hyper-parameter Tuning** — search spaces per algorithm and the search strategy used.
- **Decision Threshold Optimisation** — making the precision/recall trade-off an explicit, tunable
  choice rather than leaving the default 0.5 threshold.
- **Error Analysis** — a procedure for reviewing misclassifications, anticipated error patterns, and
  model interpretation.
- **Deployment, Monitoring and Retraining** — model persistence, concept drift, and known
  limitations.
- **Final Model Selection Process** — the decision procedure, expected outcome, and a final reporting
  template.

## Key Decision

Accuracy is deliberately treated as a secondary metric. The primary criterion is precision on the
spam class, because in this domain a false positive is far more costly than a false negative, and the
whole evaluation plan — metrics, threshold tuning, error analysis — is built around that priority.

## Before Submitting

Fill in `[Your Name]` and the submission date placeholders. If the table of contents appears blank,
click inside it and press **F9** (or right-click → Update Field) in Microsoft Word.
