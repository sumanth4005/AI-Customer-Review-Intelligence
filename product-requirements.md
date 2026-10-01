# Product Requirements 
# Product Requirements: Customer Review Intelligence

## Problem

App teams get thousands of user reviews but rarely read them in a structured way. Most teams watch the average star rating. That number hides *why* users are unhappy and can point the team at the wrong problems.

Product managers need a fast, repeatable way to answer three questions:
1. Where are users most unhappy?
2. What exactly are they complaining about?
3. What should we fix first?

## Goal

Turn raw review text into a short list of evidence-based priorities that a product team can act on.

## Users

| User | Need |
|---|---|
| Product manager | Decide what to fix or build next, backed by data |
| Engineering lead | Know which bugs and release issues hurt users most |
| Monetization / growth lead | Understand complaints about payments and ads |
| Leadership | See the overall health of user sentiment at a glance |

## Scope

**In scope**
- Overall sentiment split: positive, negative and neutral.
- Negative-review share by category and by app, with minimum sample sizes so small groups don't skew results.
- Complaint themes in negative reviews: bugs, payments, updates, ads, performance, login and support.
- Charts and tables a non-technical reader can follow.
- Written findings and prioritized recommendations.

**Out of scope for this version**
- Live data collection from app stores.
- Training a custom sentiment model. The dataset's labels are used as given.
- An interactive dashboard.

## Requirements

| # | Requirement | Priority |
|---|---|---|
| R1 | Load and clean app and review data in a repeatable notebook | Must |
| R2 | Report the overall share of positive, negative and neutral reviews | Must |
| R3 | Rank categories by negative-review share, only for categories with at least 300 reviews | Must |
| R4 | Rank apps by negative-review share, only for apps with at least 50 reviews | Must |
| R5 | Measure how often each complaint theme appears in negative reviews | Must |
| R6 | Chart category ratings and complaint themes | Should |
| R7 | Compare star ratings with review sentiment to show where they disagree | Should |
| R8 | Document limitations honestly | Must |

## Success metrics

- Every recommendation ties back to a specific number in the findings.
- A PM can read the README and findings in under 10 minutes and know the top three problems.
- Anyone can re-run the notebook from start to finish with no manual file uploads.

## Risks and assumptions

- **Old data (2018):** the patterns are useful for the method, but the specific apps have changed since.
- **Label quality:** sentiment labels came with the dataset and may misread sarcasm or mixed reviews.
- **Keyword themes are approximate:** they miss some complaints and can double-count others. An LLM-based tagger is the planned next step.
