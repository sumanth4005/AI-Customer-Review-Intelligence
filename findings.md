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
- Social and Family (which includes many kids' games) come next. The top three categories are all entertainment-driven.

## 3. The most-complained-about apps are all casual games

Apps with at least 50 reviews, ranked by negative share:

| App | Reviews | Negative share |
|---|---|---|
| Candy Crush Jelly Saga | 73 | 60.3% |
| Be A Legend: Soccer | 98 | 60.2% |
| Cooking Fever | 135 | 58.5% |
| Candy Crush Soda Saga | 166 | 57.8% |
| Angry Birds Classic | 273 | 53.8% |
| Candy Crush Saga | 240 | 52.5% |
| Agar.io | 136 | 48.5% |
| 8 Ball Pool | 219 | 48.4% |
| Homescapes | 52 | 48.1% |
| Bad Piggies | 77 | 48.1% |

- Every app in the top 10 is a free-to-play casual game.
- The Candy Crush franchise appears three times. That points to the business model, not a single bad app.
- Most of these games are hugely popular, so this isn't just users disliking the game. People keep playing and complain about specific things.

## 4. What people complain about

Share of negative reviews that mention each theme (keyword matching):

| Theme | Share of negative reviews |
|---|---|
| Bugs / crashes | 12.1% |
| Payments | 12.1% |
| Updates | 9.8% |
| Ads | 9.5% |
| Slow / battery | 7.4% |
| Login / account | 5.8% |
| Support | 3.9% |

- **Bugs and payments are tied for first.** Payments complaints are as common as crash complaints, which is unusual and lines up with the casual games above, where in-app purchases are central.
- **Updates come third.** Users often say an update broke something or made the app worse, so releases themselves are a source of complaints.
- **Ads (9.5%)** are close behind. These are mostly free apps, where ads pay the bills.
- **Support is rarely mentioned (3.9%).** Users complain about the product itself, not about getting help.

## 5. A low rating doesn't always mean more complaints

Dating has the **lowest average app rating** of any category (about 3.97), but only **21% negative reviews**, about the overall average. Games are the reverse: a middling rating (about 4.25) but the highest complaint rate (36%).

Star ratings and review text tell different stories. Looking at only one of them would point a team at the wrong problems.

## Limitations

- **Old data:** the reviews are from 2018. The specific apps have changed since, but the patterns are still useful as a method example.
- **Sentiment labels came with the dataset** and weren't checked by hand. Some sarcastic or mixed reviews are probably mislabeled.
- **Theme matching is keyword-based.**
  - A review can count toward more than one theme.
  - At least 40% of negative reviews don't match any theme.
  - A next step would be grouping complaints with an LLM or topic modeling.
- **Small samples for some apps:** a few apps in the top 10 have only 50–100 reviews.
- **Category matching:** reviews were joined to categories by app name, and a small number of reviews didn't match an app.
