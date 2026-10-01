# User Stories

## 1. See overall sentiment
**As a** product manager, **I want** to see what share of reviews are positive, negative and neutral, **so that** I know how big the complaint problem is.

**Acceptance criteria**
- The notebook shows the percentage for each sentiment.
- Empty reviews are excluded and the total count is shown (37,427).

## 2. Find the unhappiest categories
**As a** product manager, **I want** categories ranked by negative-review share, **so that** I know where users are least satisfied.

**Acceptance criteria**
- Only categories with at least 300 reviews are ranked.
- The table shows review count and negative share for each category.
- The top 10 are shown, highest first.

## 3. Find the most-complained-about apps
**As a** product manager, **I want** individual apps ranked by negative-review share, **so that** I can study what the worst performers have in common.

**Acceptance criteria**
- Only apps with at least 50 reviews are ranked.
- The top 10 are shown with review count and negative share.

## 4. Understand what users complain about
**As an** engineering lead, **I want** negative reviews grouped by theme, such as bugs, updates and performance, **so that** I can see which technical problems hurt users most.

**Acceptance criteria**
- Each theme shows the share of negative reviews that mention it.
- Results appear in both a table and a bar chart.
- The theme keywords are visible in the notebook, so anyone can check or adjust them.

## 5. Understand payment and ad complaints
**As a** monetization lead, **I want** to see how often payments and ads come up in complaints, **so that** I can balance revenue against user frustration.

**Acceptance criteria**
- Payments and ads are separate themes.
- The findings explain how these themes relate to the most-complained-about apps.

## 6. Compare ratings with review text
**As a** product leader, **I want** to see where star ratings and complaint rates disagree, **so that** I don't rely on star ratings alone.

**Acceptance criteria**
- The findings compare at least one category's average rating with its negative-review share.
- The disagreement is explained in plain language.

## 7. Get clear next steps
**As a** product manager, **I want** prioritized recommendations tied to the findings, **so that** my team knows what to do first.

**Acceptance criteria**
-
