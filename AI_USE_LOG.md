# AI assistance and verification log

**Name:** Kseniia Mamushkina  
**Student ID:** 2026A8010351001  
**Assignment:** DS-A5 — Time-Series Rolling Evaluation Lab  
**AI tool:** ChatGPT (OpenAI)  

## Scope of AI assistance

AI assistance was extensive and included:

- Discussing feasible forecasting questions and public datasets.
- Locating HKBWS waterbird monitoring reports and assisting
  with extracting and combining monthly Black-faced Spoonbill
  counts into a derived CSV with source references.
- Drafting Python code for data validation, lag construction,
  expanding-window evaluation, baseline forecasts, Ridge
  regression, metrics, tables, and plots.
- Drafting and revising English notebook explanations.
- Drafting monitoring, retraining, and fallback procedures.
- Reviewing the notebook and preparing a PDF report.

## Advice adopted

The analysis uses a one-month forecast horizon, two lagged
predictors, and identical rolling forecast origins for all methods.
Preprocessing is refitted inside each Ridge training window.

## Student verification

I ran the analysis in Google Colab and inspected the displayed
validation results, forecasts, metrics, tables, and plots.

I independently spot-checked monthly counts across different
years against the source reports and found agreement.
This was a subset check, not an independent re-extraction
of all 60 values.

I reviewed worked examples and requested explanations of the
target, lag alignment, initial training size, and the distinction
between training observations and evaluated forecasts.

I also ran the environment-version cell in Colab and supplied
the resulting Python and package versions for documentation.

## Automated and AI-supported checks

The notebook's automated checks verified the input-file hash,
monthly continuity, absence of duplicates, valid integer counts,
date consistency, species, and study-area labels.

Temporal assertions checked that training outcomes and forecast
inputs were available under the stated month-end assumption.
StandardScaler was fitted within each training window.

These automated checks were implemented with AI assistance.

During notebook review, ChatGPT also reported a local sequential
execution check and a future-value perturbation check. The local
review used scikit-learn 1.8.0, whereas the saved Colab run used
1.6.1. Overall metrics agreed to the displayed precision.

## Remaining limitations

Historical internal availability, publication dates, and revision
histories were not established. Published counts are proxies
for the proposed operational records.

The monitoring and fallback procedures are proposals, not a
tested operational system. Two annual evaluation cycles do not
establish persistent drift or a statistically reliable difference
between forecasting methods.

Responsibility for the submitted analysis, interpretation,
and disclosure remains with the student.
