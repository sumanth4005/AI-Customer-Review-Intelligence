# Findings

## Data

- **Source:** Google Play Store Apps dataset on Kaggle (lava18). It was scraped from Google Play in 2018.
- **Reviews analyzed:** 37,427 user reviews with text, after dropping empty rows.
- **App details:** about 9,600 unique apps, with category, rating and installs.
- **Sentiment labels:** each review comes with a Positive / Negative / Neutral label from the dataset. I did not label reviews myself.
- **Analysis:** done in Python (pandas) in Google Colab. See `review_analysis.ipynb`.

## 1. About 1 in 5 reviews is a complaint

| Sentiment | Share of reviews |
|---|---|
| Positive | 64.1% |
| Negative | 22.1% |
| Neutral | 13.8% |

Most reviews are positive, but 22% negative is a big enough base to dig into: more than 8,000 complaints.

## 2. Games get far more complaints than anything else

Negative share by category (categories with at least 300 reviews):

| Category | Reviews | Negative share |
|---|---|---|
| Game | 6,678 | **36.1%** |
| Social | 741 | 28.2% |
| Family | 2,009 | 27.5% |
| News & Magazines | 1,040 | 26.5% |
| Entertainment | 1,264 | 25.2% |
| Video Players | 331 | 25.1% |
| Sports | 1,479 | 22.8% |
| Finance | 1,435 | 22.3% |
| Travel & Local | 1,692 | 21.7% |
| Dating | 1,715 | 21.0% |

- Games are the largest category in the review data and also the most negative. More than 1 in 3 game reviews is a complaint, against 22% overall.
- Social
