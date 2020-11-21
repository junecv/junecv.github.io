---
layout: post
title: Predicting COVID Cases
---

For CS145 final project, I used historical and population data to predict cumulative COVID cases on county level.

By training a linear regression model with data between April and August 2020, below results were achieved:

Method | Data | mean abs error | median abs error
--- | --- | --- | --- |
Evaluation | Sep 1st to 30th | 7.52 | 2.08
Evaluation | Oct 1st to 31st | 9.63 | 2.81
Prediction | Nov 1st to 7th  | 15.95 | 3.99

The mean error rate was 1.66%. Click [here](/projects/covid.html) to learn more.
