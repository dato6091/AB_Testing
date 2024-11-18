
# Comprehensive A/B Testing Workflow

## Overview

This repository demonstrates a complete A/B testing workflow, from calculating metrics to evaluating statistical significance and analyzing results. The project consists of three Jupyter Notebooks, each focusing on a critical stage of the process:

1. **Calculating Metrics**: Prepares and computes key performance indicators (KPIs) for the control and test groups.
2. **Significance & Power Calculator**: Calculates statistical significance and power for different sample sizes and metrics.
3. **A/B Test Analysis**: Conducts hypothesis testing and provides actionable insights based on the results.

## Notebooks Overview

### 1. Calculating Metrics
- **Objective**: Aggregate and compute metrics such as average activity levels, retention rates, and click-through rates (CTR).
- **Key Features**:
  - Data preprocessing for user activity and CTR data.
  - Aggregation of metrics by groups (control vs. test).
  - Visualization of trends over time using Altair.

### 2. Example of Significance Power Calculator
- **Objective**: Understand the statistical power and significance thresholds required for the A/B test.
- **Key Features**:
  - Implementation of significance level calculators.
  - Power analysis to ensure test reliability.
  - Interactive examples to visualize type I and type II errors.

### 3. A/B Test Analysis
- **Objective**: Perform hypothesis testing and evaluate the impact of the experimental changes.
- **Key Features**:
  - Two-sample t-tests to compare means between control and test groups.
  - Visualization of pre- and post-test metrics.
  - Clear conclusions and recommendations based on statistical results.

## Dataset

The dataset includes:
- **User Activity Data**:
  - **userid**: Unique identifier for users.
  - **dt**: Date of activity.
  - **groupid**: Group identifier (0 = control, 1 = test).
  - **activity_level**: User activity metric.
- **Click-Through Rate (CTR) Data**:
  - **ctr**: Click-through rate for each user on a given date.

## Key Findings

### Statistical Testing Results:
1. **Activity Levels**:
   - Before the test: No significant difference between groups.
   - After the test: Significant improvement in activity levels in the test group.
   - **T-statistic**: -1600.79, **P-value**: < 0.001 (for post-test activity levels).

2. **Click-Through Rate (CTR)**:
   - Significant improvement in CTR for the test group after the introduction of the new feature.

## Recommendations

Based on the analysis:
- The new feature positively impacts user engagement and CTR.
- It is recommended to roll out the feature to all users.
- Post-implementation, monitor key metrics to confirm sustained improvement.

## Dependencies

- Python 3.9 or later
- Libraries: `pandas`, `numpy`, `scipy`, `altair`, `matplotlib`

## Usage

1. Clone the repository and install dependencies.
2. Run the notebooks sequentially:
   - `1. Calculating Metrics.ipynb`
   - `2. Example of Significance Power Calculator.ipynb`
   - `3. AB Test Analysis.ipynb`
3. Follow the conclusions and recommendations in Notebook 3.

## Future Work

- Include additional metrics for a more comprehensive analysis.
- Test the feature's impact across different user segments.
- Extend the analysis to include long-term trends post-implementation.
