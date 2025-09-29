# Rank-Prediction

Project Overview

This project predicts the Billboard Hot 100 song ranks using historical chart data.
The goal is to estimate a song’s rank based on past performance, trends, and chart-related features.

This is framed as a supervised regression problem.

Dataset

Source: Billboard Hot 100 Songs Dataset

File: charts.csv

Contains:

song, artist, date, rank

Historical stats: last-week, peak-rank, weeks-on-board

Methodology
1. Problem Framing

Task: Regression (predict numeric rank: 1–100)

Target variable: rank

Features used:

last-week – previous week’s position

weeks-on-board – number of weeks the song has charted

peak-rank – best position achieved

year & month (from date)

Model

Algorithm: Random Forest Regressor

Reason:

Handles non-linear patterns

Robust to outliers

Works well with tabular data without heavy preprocessing

3. Training & Evaluation

Train-test split: 80% / 20%

Metric: RMSE (Root Mean Squared Error)

Result:

RMSE ≈ 5.98 → on average, predictions are within ±5 ranks of the true chart position

Feature Importance

Feature importance from Random Forest:

last-week → most influential (strong persistence week-to-week)

weeks-on-board → longevity matters

peak-rank → historically strong performers rank higher

year/month → some seasonal/era trends



