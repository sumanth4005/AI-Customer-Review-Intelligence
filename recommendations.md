# Recommendations

These recommendations are for a product team working on a free-to-play mobile game. That's where the complaints are concentrated (see `findings.md`). Each one ties back to a specific finding.

## 1. Fix how in-app purchases feel, not just how they work

**Why:** payments complaints (12.1% of negative reviews) are as common as crash complaints. Every app in the top 10 for complaints is a free-to-play game.

**What to do:**
- Read a sample of payment-related negative reviews and sort them into buckets: price too high, pay-to-win, unclear charges, failed purchases, refund problems.
- Fix the clear failures first, such as charges that don't deliver items and confusing purchase screens.
- Test whether the game stays winnable without paying, and track how many levels players get stuck on before they pay or quit.

**Measure:** share of negative reviews mentioning payments, refund requests, and day-7 / day-30 retention for players who never pay.

## 2. Treat every update as a risk to ratings

**Why:** about 1 in 10 negative reviews mentions an update, and bugs and crashes are tied for the top complaint.

**What to do:**
- Roll out updates to a small share of users first (staged rollout), and stop the rollout if crash rates or negative reviews jump.
- Track negative-review share for 7 days after each release as a standard release health check.
- Add a short "what changed" note in the app, so users know why things look different.

**Measure:** crash-free sessions, and negative-review share in the week after each release compared with the week before.

## 3. Cap ad load in free apps

**Why:** ads appear in 9.5% of negative reviews, mostly for free apps that rely on ads for revenue.

**What to do:**
- Set a maximum number of ads per session, and never show an ad right after a player loses.
- Offer an ad-free option at a low price. Some users who complain about ads would pay to remove them.
- A/B test lighter ad frequency and compare revenue per user against retention.

**Measure:** ad-related complaint share, session length, and total revenue (ads plus ad-free purchases) per user.

## 4. Watch review text, not just star ratings

**Why:** Dating has the lowest average rating but an average complaint rate, while Games has a middling rating but the highest complaint rate. Ratings alone point to the wrong problems.

**What to do:**
- Set up a simple weekly review dashboard: negative share, top complaint themes, and changes from the previous week.
- Flag any theme that jumps more than a set amount week over week, so the team can respond before the star rating drops.

**Measure:** time from a complaint spike to a fix shipped.

## 5. Improve the theme tagging before scaling this up

**Why:** keyword matching missed at least 40% of negative reviews, and some reviews match several themes.

**What to do:**
- Use an LLM to tag each negative review with a theme. Check its accuracy against 200 reviews tagged by hand.
- Add themes that keywords missed, such as difficulty, gameplay changes and missing features.
- Re-run the analysis on recent reviews, since this dataset is from 2018.

**Measure:** agreement between the LLM tags and the hand-tagged sample, and the share of negative reviews left untagged.

## Priority

| # | Recommendation | Impact | Effort |
|---|---|---|---|
| 1 | Fix in-app purchase experience | High | Medium |
| 2 | Safer update releases | High | Low |
| 3 | Cap ad load | Medium | Low |
| 4 | Weekly review-text dashboard | Medium | Low |
| 5 | Better theme tagging with an LLM | Medium | Medium |

Start with **#2 and #3**: they're low effort and protect ratings right away. Then take on **#1**, which addresses the biggest complaint driver.
