# Brand Social Sentiment & Emojis — Customer and Marketing Analytics

**Program:** MSc Data Science & Business Analytics — Bologna Business School
**Course:** Customer and Marketing Analytics (Team Assignment 2)
**Dataset:** 600 social media posts from three brands — FitPulse, LumoraBeauty and TechNest

---

## Project Overview

What makes a brand's social media post perform? This project analyses the text, tone and emojis of brand posts and links them to engagement (likes, comments and reposts).

The analysis answers five questions:

| # | Question | Approach |
|---|---|---|
| Q1 | How positive are the posts? | Transformer sentiment model (`cardiffnlp/twitter-roberta-base-sentiment-latest`) with VADER as a robustness check |
| Q2 | What are brands posting about? | Zero-shot classification into *Informative*, *Entertaining* or *Promotional* |
| Q3 | How do brands use emojis? | Paralinguistic / emoji feature extraction |
| Q4 | What drives engagement? | Regression models with sentiment, topic and emoji features |
| Q5 | Do engagement drivers differ across brands? | Brand-level models and interaction effects |

## Highlights

- Most posts are **Informative** (68.5%), followed by Promotional (24.0%) and Entertaining (7.5%).
- **FitPulse** is the most informative brand (72.5% of its posts), focused on educational fitness content.
- **More positive posts and more emojis both drive engagement**: +1 SD in sentiment means about +33% likes and +39% comments; +1 SD in emoji count about +15% likes and +22% comments. Both effects are significant for every brand.
- **Topic barely matters**: entertaining and promotional posts perform like informative ones, except promotional posts at TechNest.

Explore the [interactive dashboard](https://marialezapatag.github.io/dashboards/marketing.html) or see the full report in [`Brand Social Sentiment & Emojis.pdf`](Brand%20Social%20Sentiment%20%26%20Emojis.pdf).

## Repository Contents

```
├── Customer and Marketing analytics.ipynb   # Full analysis (Q0–Q5)
└── Brand Social Sentiment & Emojis.pdf      # Final report
```

## Tech Stack

Python · pandas · Hugging Face Transformers · PyTorch · VADER · TextBlob · emoji · statsmodels · scikit-learn · matplotlib · seaborn

## How to Run

1. Open the notebook in Jupyter or Google Colab (a GPU speeds up the transformer models).
2. Place the course dataset `Team Assignment 2 Data 2026.csv` next to the notebook. The dataset is not included in this repository.
3. Run the cells in order. The first run downloads the Hugging Face models.
