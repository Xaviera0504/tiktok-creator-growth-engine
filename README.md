# TikTok Creator Growth Engine: Product Analytics Case Study
**Role:** Product Manager, Creator Growth  
**Objective:** Identify "High-Value" content signals to optimize the recommendation engine and increase creator retention.

---

## 1. The Business Problem
TikTok’s growth depends on a constant supply of high-quality content. However, new creators often churn if they don't see immediate, meaningful engagement. Views are a vanity metric; Shares and Downloads indicate true content value. 

**The Challenge:** How do we identify "Rising Stars" (unverified creators with high-intent engagement) so the product can boost them in the algorithm and keep them on the platform?

## 2. The Hypothesis
"If we evaluate content based on **'High-Intent Actions' (Shares + Downloads)** rather than just Likes or Views, we can identify high-quality creators faster, leading to higher long-term creator retention."

## 3. The Data Strategy
Using a dataset of ~19,000 TikTok videos, I am analyzing:
* **The Stickiness Ratio:** `(Shares + Downloads) / Views` to measure virality intent.
* **The Engagement Depth:** `(Comments + Likes) / Views` to measure community sentiment.
* **The "Hidden Gem" Identifier:** Finding unverified users whose Stickiness Ratio is in the top 5%.

## 4. Analysis & Code
* **[View the Jupyter Notebook Code Here](./notebooks/tiktok_growth_analysis.ipynb)**

## 5. Findings & Product Recommendation
**The Insight:** By engineering a "Stickiness Ratio" (`(Shares + Downloads) / Views`), we successfully identified a cohort of unverified creators who are generating disproportionately high-intent engagement compared to their view counts.

**The Product Feature:** I propose a **"Creator Pulse"** feature for the recommendation algorithm. When an unverified creator's video hits a Stickiness Ratio above our target threshold within its first 10,000 views, the algorithm automatically grants a 1.5x distribution multiplier on the For You Page (FYP).

**Business Impact:** 1. **Reduces Creator Churn:** Early algorithmic rewards keep new creators motivated to post.
2. **Improves Content Quality:** Trains the algorithm to prioritize videos that users actually want to share, rather than just passively watch.
