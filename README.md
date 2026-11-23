# Twitter Data Analysis Project

## Overview
This project analyzes Twitter data to explore its correlation with pricing trends through data scraping, cleansing, sentiment analysis, and regression modeling. The insights aim to inform pricing strategies and market trends.

## Start with an offline check

Use the [swarm-ready handoff](SWARM_READY.md#verification-starting-point) to
check the three R scripts without installing analysis packages, sourcing the
scripts, or contacting providers. This is a historical analysis, not a
self-contained reproducible pipeline: later stages expect objects from the
original R workspace. The acquisition script is not a local smoke test.

## Features
- **Historical acquisition**: Example Twitter and Bitcoin-price collection code; current provider access has not been verified.
- **Data Cleansing**: Preprocess data for analysis.
- **Sentiment Analysis**: Gauge public opinion.
- **Statistical Modeling**: Identify correlations with pricing.
- **Data Visualization**: Visualize findings.

## R Script Descriptions

### 1TwitterAndPriceScrapeBeta.R
Historical acquisition script for tweets via `rtweet` and hourly Bitcoin prices via CryptoCompare. Its top-level code attempts authenticated collection and writes files, so do not source it for verification.

### 2TwitterDataCleansingAndSentimentAnalysis.R
Exploratory cleaning and sentiment analysis using `sentimentr`. It expects tweet and price objects already present in the R workspace and sketches the construction of `FinalData` for modeling.

### 3RunningCorrelationAndRegression.R
Fits a linear model and plots correlations when a prepared `FinalData` is available. The model uses `price` as the response and `volume`, `n`, `Agreement`, and `sentiment` as predictors.

## Future Work
- Integrate additional data sources for richer analysis.
- Implement machine learning for advanced sentiment analysis.
- Develop a web application for real-time insights.

## Acknowledgments
Thanks to the developers of R packages used in this project, including `tidyverse`, `rvest`, and `ggplot2`.

## Badges
![License](https://img.shields.io/badge/license-MIT-blue)

## Contact
For inquiries or collaboration, reach out via my GitHub profile: [Kohnnn](https://github.com/Kohnnn).
