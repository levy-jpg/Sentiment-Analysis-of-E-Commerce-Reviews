# Sentiment Analysis of E-Commerce Reviews

This repository explores sentiment analysis of e-commerce product reviews, with a focus on how different natural language processing approaches interpret human expression, ambiguity, and uncertainty in real-world text.

Rather than optimising purely for accuracy, the project emphasises evaluation choices, robustness, and trade-offs between model complexity, interpretability, and performance. The work examines how classical NLP methods can remain effective for sentiment classification despite the growing use of large language models in industry.

## Overview

Customer reviews are often informal, emotional, and noisy. They frequently contain spelling variations, sarcasm, mixed sentiment, and ambiguous language, particularly when expressing neutral opinions. This project investigates how different modelling choices respond to these challenges when classifying reviews into positive, neutral, and negative sentiment.

Multiple models are implemented and compared, starting from strong linear baselines and progressing towards optimised and combined approaches.

## Approach

The project includes:

- Text preprocessing and feature extraction using TF-IDF
- Word-level and character-level n-gram representations
- Classical machine learning models including Logistic Regression, Linear SVM, and Complement Naive Bayes
- Hyperparameter optimisation using randomised search
- Probability calibration and class-specific threshold tuning
- A soft-voting ensemble to examine stability and confidence aggregation
- Evaluation using macro-averaged precision, recall, and F1-score
- Statistical comparison of models using McNemar’s test
- Learning curves to analyse generalisation behaviour

All experiments are implemented in a single Jupyter notebook for clarity and reproducibility.

## Key Observations

Some key insights from this exploration include:

- Character-level representations can be particularly robust to noisy and informal text
- Macro-averaged metrics are essential when evaluating sentiment models with ambiguous or imbalanced classes
- Small performance gains from ensembling often come with increased complexity, highlighting trade-offs relevant to real-world deployment
- Classical models remain competitive for sentiment analysis tasks where interpretability, efficiency, and cost matter

## Repository Structure

- `Sentiment_Analysis.ipynb`: Main notebook containing the full pipeline, experiments, and analysis
- Parquet datasets used for training and evaluation

The notebook is intended to be read top-to-bottom and renders directly on GitHub.

## Future Directions

Potential extensions include:
- Comparing classical approaches with large language models for sentiment classification
- Exploring domain adaptation and transfer learning
- Incorporating uncertainty estimation and confidence-aware decision-making
- Investigating sentiment analysis from a UX and human-centred AI perspective

