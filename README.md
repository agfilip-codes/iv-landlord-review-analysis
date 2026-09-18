# Isla Vista Landlord Review Analysis

Independent research project (LOREL Lab, UCSB) analyzing property management reviews across Isla Vista to surface patterns in tenant complaints and sentiment that aren't visible from browsing individual reviews.

## Goal

Isla Vista has a small number of large property management companies, and prospective tenants often rely on scattered reviews across Google, Yelp, and RateMyLandlord to judge them. This project aims to:

- Quantify how often specific complaint types (mold, deposits, maintenance response, communication, etc.) show up per landlord
- Compare sentiment patterns across landlords using text classification
- Identify time-based patterns in reviews, including unusual clustering of positive reviews that may suggest incentivized or coordinated posting
- Surface the words and phrases most associated with positive vs. negative sentiment for each landlord
- Eventually build a public-facing tool where prospective tenants can explore a landlord's review history and complaint breakdown before signing a lease

## Status

In progress. Current dataset: 1,000+ reviews collected across Google, Yelp, RateMyLandlord, and other sources, with defined inclusion criteria.

Preliminary modeling:
- Trained per-landlord Naive Bayes classifiers and a full-dataset logistic regression (TF-IDF + SGDClassifier) to classify review sentiment
- Extracted top predictive words per sentiment class per landlord (e.g., "mold," "rude," "deposit" trending negative; "helpful," "easy," "staff" trending positive)

## What's here

- `analysis.ipynb`: data loading, cleaning, per-landlord and full-dataset sentiment classification, and word-association analysis

## Planned next steps

- Complaint-category tagging (mold, deposits, maintenance, communication) to get more specific than just positive/negative
- Time-series analysis of review clustering
- Public web app for browsing landlord review summaries

## Notes on data

Reviewer usernames have been removed from published outputs to avoid publishing personal information tied to review text.#
