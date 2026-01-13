📊 Dynamic Pricing & Customer Sentiment Analytics
📌 Project Overview

This project analyzes pricing power and customer sentiment in e-commerce products by combining Natural Language Processing (NLP) with price elasticity modeling. The goal is to identify price-inelastic categories and uncover hidden dissatisfaction masked by high star ratings, enabling smarter pricing decisions.

🧠 Key Business Questions

Are high star ratings always aligned with positive customer sentiment?

Which product categories are price-inelastic and can tolerate price increases?

How can customer sentiment enhance pricing strategy beyond traditional metrics?

🛠️ Tech Stack

Python

Pandas, NumPy

NLTK (VADER Sentiment Analyzer)

Statsmodels (OLS Regression)

Matplotlib / Seaborn

🔍 Methodology
1. Data Cleaning & Feature Engineering

Standardized pricing, ratings, and volume metrics

Engineered discount percentage

Used rating count as a proxy for sales volume (with safeguards)

2. Sentiment Analysis (NLP)

Applied VADER to unstructured review text

Generated sentiment scores for each review

Detected “Rating Inflation”:

High star rating (≥ 4)

Negative sentiment score (< -0.05)

3. Price Elasticity Modeling

Used log–log OLS regression to estimate price elasticity

Modeled elasticity at the category level

Filtered statistically insignificant results to avoid misleading insights

4. Visual Analytics

Built a dual-axis chart comparing:

Price sensitivity (elasticity magnitude)

Average customer sentiment

Highlighted Top 20 high-impact categories

📈 Key Insights

Several categories show price inelastic behavior, indicating pricing power

Detected products with hidden dissatisfaction despite strong star ratings

Insights suggest potential 6–11% margin uplift through informed pricing adjustments

📂 Outputs

amazon_processed_with_sentiment.csv – cleaned data with sentiment scores

category_elasticity_summary.csv – elasticity & sentiment by category

elasticity_chart.png – visual summary for pricing decisions

🚀 Future Enhancements

Replace sales proxy with time-series demand data

Introduce causal pricing models

Integrate dynamic price simulation
