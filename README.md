# The Illusion of Similarity: Causal AI vs. Traditional Analytics

This repository demonstrates how traditional data dashboards can mislead business stakeholders, and how **Causal AI** (specifically mediation analysis) can uncover the true drivers of customer retention. 

## Overview
We present a classic business dilemma: **Does cross-selling more products actually drive customer loyalty and reduce churn, or are we simply observing natural customer behavior?**

To explore this, the code simulates a scenario comparing two companies (or customer segments). On the surface, a traditional dashboard comparing churn rates shows that cross-selling from 1 to 3 products is highly effective for both. However, beneath the surface, the mechanics of their loyalty—measured via an **Implicit Association Test (IAT)** score—are fundamentally different.

* **Company A (Self-Selection):** Selling more products does *not* cause a reduction in churn. Inherently loyal customers simply tend to buy more products and churn less. The dashboard shows a massive false positive.
* **Company B (Product Effect):** The cross-selling strategy genuinely works. Acquiring more products directly increases the customer's IAT loyalty score, which in turn causes a significant drop in churn.

## Evaluation Techniques
This project compares three analytical approaches to highlight the "dashboard illusion":

1.  **Traditional Analytics (Naive Comparison):** Comparing observed means. This standard dashboard view completely misses the hidden behavioral variables and recommends expensive cross-selling for both groups.
2.  **Causal AI (Implemented):** Using Double Machine Learning (DML) and Sequential G-Computation. This approach separates the **Total Effect (TE)** into the **Natural Direct Effect (NDE)** and the **Natural Indirect Effect (NIE)** (the loyalty gained specifically via the IAT score).
3.  **LLM-Assisted Evaluation (Planned):** Testing how Large Language Models interpret raw vs. causally-adjusted data to provide automated business recommendations.

## Getting Started

### Prerequisites
You will need Python 3.8+ and the following libraries installed:
```bash
pip install numpy pandas scipy seaborn matplotlib scikit-learn lightgbm econml
