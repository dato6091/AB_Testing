
# A/B Testing Projects Collection

## Overview

This repository contains a collection of A/B testing studies designed to demonstrate a variety of techniques and workflows for evaluating the impact of experimental changes. Each study is a standalone project covering a unique use case and statistical analysis approach. These projects showcase how data-driven decisions can be made effectively through proper experimentation and analysis.

## Projects

### 1. A/B Test Analysis for a Fast-Food Marketing Campaign
- **Objective**: Identify the most effective promotional strategy for introducing a new menu item by analyzing sales data.
- **Key Features**:
  - Statistical tests (ANOVA, Kruskal-Wallis, Tukey’s HSD).
  - Comprehensive EDA and visualization of sales trends.
  - Data cleaning and preparation for accurate testing.
- **Key Findings**: Promotions 1 and 3 outperformed Promotion 2 significantly. Recommendation to implement Promotion 1 across all locations.
- **Location**: `AB_Test_FastFood_Marketing.ipynb`

### 2. A/B Test Analysis for Cookie Cats
- **Objective**: Evaluate the impact of altering the position of a "gate" in a mobile game on player engagement and retention.
- **Key Features**:
  - Comparison of metrics such as rounds played and retention rates.
  - Bootstrapping for confidence interval estimation.
  - Hypothesis testing using two-sample t-tests.
- **Key Findings**: Moving the gate to level 40 significantly increased player engagement and retention. Recommendation to roll out the new gate position.
- **Location**: `AB_Test_Cookie_Cats.ipynb`

### 3. Comprehensive A/B Testing Workflow
- **Objective**: Demonstrate a full A/B testing workflow, from metric calculations to significance analysis and final recommendations.
- **Key Features**:
  - Three detailed notebooks:
    1. `1. Calculating Metrics.ipynb`: Aggregates and visualizes key metrics.
    2. `2. Example of Significance Power Calculator.ipynb`: Calculates significance levels and statistical power.
    3. `3. AB Test Analysis.ipynb`: Conducts hypothesis testing and interprets results.
  - Comparison of control and test groups using t-tests.
  - Visualization of CTR trends over time.
- **Key Findings**: Significant improvements in user activity and CTR in the test group. Recommendation to implement the tested feature across all users.
- **Location**: Folder containing the three notebooks.

## Dependencies

- Python 3.9 or later
- Libraries: `pandas`, `numpy`, `scipy`, `matplotlib`, `seaborn`, `altair`, `statsmodels`, `scikit-posthocs`

## Usage

1. Clone the repository and navigate to the respective project folder.
2. Open the relevant Jupyter notebook(s).
3. Install the dependencies and run the notebooks sequentially to reproduce the results.

## Future Work

- Explore additional metrics for deeper insights.
- Test variations of experimental setups to optimize key outcomes.
- Investigate long-term impacts and trends post-implementation.

## Conclusion

This collection highlights the value of structured A/B testing for making data-driven decisions. Each project provides a template for implementing experiments, analyzing results, and drawing actionable conclusions across different domains.

