# Customer Segmentation Engine

Groups customers into meaningful, human-readable segments using unsupervised clustering --
no manual rule-writing required.

## Problem
Generic "email everyone the same offer" marketing wastes budget on customers who will never
convert and under-serves the ones who would. This finds natural customer groups automatically.

## What It Does
- Scales Age, Annual Income, and Spending Score before clustering (required for K-Means)
- Uses the elbow method + silhouette score to pick the right number of clusters, not a guess
- Fits K-Means and automatically names each cluster based on its income/spending profile
- Visualizes the segments so a marketer can sanity-check them at a glance

## Real Results (real Mall Customer dataset, 200 customers)
Five segments came out clean and distinct:
1. **High-Value** -- avg income $86.1k, avg spending score 81.5 (the best marketing target)
2. **High-Income Low-Spend** -- avg income $86.1k, avg spending score 19.4 (untapped potential)
3. **At-Risk / Low Value** -- avg income $26.8k, avg spending score 18.4
4. Two "Average Customer" segments across different income/age profiles

## Tech Stack
Python, Scikit-learn, Matplotlib

## How to Run
Open in Google Colab, run all cells. Dataset auto-downloads via `kagglehub` with a synthetic
fallback if it ever fails.
