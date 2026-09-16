# Week 2 — Data Cleaning and Transformation

**Project:** Spam Email Prediction using Machine Learning
**Role:** Python Specialist Intern (Data Science)
**Deliverable:** `Week2_Data_Cleaning_and_Transformation.docx`

## Purpose

Turn the raw SMS Spam Collection text into a clean, leakage-free, model-ready feature matrix.

## What This Week Covers

- **Data Quality Assessment** — a structural audit of the raw data, catalogue of expected quality
  issues (duplicates, encoding artefacts, label noise), and a note on why classic outlier-removal
  doesn't apply to short text messages.
- **The Cleaning Pipeline** — a seven-step process:
  1. Structural clean-up
  2. Duplicate removal, missing values and label-conflict resolution
  3. Feature extraction *before* stripping (so signal like punctuation counts and message length is
     captured before it's normalised away)
  4. Text normalisation (case-folding, punctuation, whitespace)
  5–7. Tokenisation, stop-word handling and lemmatisation
- **Transformation Strategy** — a two-block feature design: TF-IDF text features (Block A) and scaled
  structural features (Block B), with a discussion of normalisation vs. standardisation and how class
  imbalance is handled.
- **Splitting Strategy and Leakage Prevention** — a leakage checklist and the decision to encapsulate
  every transformation inside a single scikit-learn `Pipeline`, fitted only on training folds.
- **Validation of the Cleaning Process** — before-and-after reporting and manual spot checks to
  confirm the pipeline behaves as intended.
- **Deliverables** — the concrete artefacts this stage produces (cleaned dataset, fitted
  transformers, cleaning report).

## Key Decision

All cleaning and feature-engineering steps are encapsulated in one `Pipeline` object rather than run
as ad-hoc scripts, so the exact same transformations apply identically to training and test data with
zero risk of information leakage.

## Before Submitting

Fill in `[Your Name]` and the submission date placeholders. If the table of contents appears blank,
click inside it and press **F9** (or right-click → Update Field) in Microsoft Word.
