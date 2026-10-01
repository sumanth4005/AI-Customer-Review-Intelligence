# AI Customer Review Intelligence 
 
AI Product Analyst project for analyzing customer reviews, sentiment, complaints, and product priorities. 
# AI Customer Review Intelligence

I analyzed **37,427 Google Play user reviews** to find out where users are unhappy, what they complain about, and what a product team should do about it.

## Key results

- **22% of reviews are negative**, roughly 1 in 5.
- **Games get the most complaints:** 36% of game reviews are negative, against 22% overall.
- **All 10 of the most-complained-about apps are free casual games**, including three Candy Crush titles at 52–60% negative.
- **Bugs and payments are tied as the top complaint themes**, each in 12% of negative reviews. Updates (10%) and ads (9.5%) follow.
- **Star ratings and review text disagree:** Dating has the lowest average rating but only average complaints.

## Repository contents

| File | What's in it |
|---|---|
| [`product-requirements.md`](product-requirements.md) | The problem, goals, scope and success metrics |
| [`user-stories.md`](user-stories.md) | Who uses the analysis and what they need, with acceptance criteria |
| [`review_analysis.ipynb`](review_analysis.ipynb) | The analysis in Python (pandas, matplotlib), with charts |
| [`findings.md`](findings.md) | What the data shows, with tables and limitations |
| [`recommendations.md`](recommendations.md) | Five prioritized product recommendations, with how to measure each |

## Data

The [Google Play Store Apps dataset](https://www.kaggle.com/datasets/lava18/google-play-store-apps) on Kaggle, scraped in 2018. It has two files:
- `googleplaystore.csv`: about 9,600 apps with category, rating and installs.
- `googleplaystore_user_reviews.csv`: user reviews with a sentiment label.

## Method

1. Load both files and clean the app data: remove duplicates and convert installs, price and review counts to numbers.
2. Measure the overall sentiment split.
3. Join reviews to app categories and calculate the negative-review share by category and by app, with minimum sample sizes.
4. Tag negative reviews by complaint theme using keyword matching.
5. Turn the results into findings and prioritized recommendations.

## Tools

Python, pandas, matplotlib, Google Colab, Git and GitHub.

## Limitations and next steps

- The data is from 2018, so a next step would be re-running the analysis on recent reviews.
- Sentiment labels came with the dataset and weren't checked by hand.
- Keyword theme matching missed at least 40% of negative reviews. A next step would be tagging themes with an LLM and checking its accuracy against a hand-labeled sample.
