
# A/B Test Analysis for Cookie Cats

## Overview

This project examines an A/B test conducted for the mobile game **Cookie Cats**. The goal was to evaluate the impact of altering the position of a gameplay feature, the "gate," on player engagement and retention. Two groups were tested:
- **Control Group (Gate 30)**: The gate was placed at level 30.
- **Experimental Group (Gate 40)**: The gate was moved to level 40.

The analysis explores which version of the game yields better player engagement and retention.

## Dataset

The dataset includes:
- **userid**: Unique identifier for each player.
- **version**: Test group (Gate 30 or Gate 40).
- **sum_gamerounds**: Total rounds played by each player.
- **retention_1**: Whether the player returned the day after installing (1 = yes, 0 = no).
- **retention_7**: Whether the player returned a week after installing (1 = yes, 0 = no).

## Objectives

1. Compare player engagement between the control and experimental groups using rounds played.
2. Assess short-term (Day 1) and long-term (Day 7) player retention.
3. Provide recommendations for the most effective gate position.

## Methodology

### 1. Data Exploration and Preprocessing
- Analyzed the distribution of game rounds and retention metrics for both groups.
- Checked for missing data and outliers.

### 2. Statistical Testing
- **Hypotheses**:
  - $H_0$: Metrics are equal for both groups (no effect of gate position).
  - $H_1$: Metrics differ between groups (effect of gate position).
- **Metrics Tested**:
  - Total game rounds per user.
  - Retention after 1 day and 7 days.
- **Bootstrap Confidence Intervals**:
  - Used to evaluate the overlap of metrics between groups.
- **Two-Sample T-Tests**:
  - Compared mean values across groups.

### 3. Tools Used
- **Visualization**:
  - Histograms and boxplots for distribution analysis.
- **Statistical Analysis**:
  - Bootstrapping and hypothesis testing using Python libraries.

## Key Findings

| Metric                | Gate 30 (95% CI)        | Gate 40 (95% CI)         | Relative Effect (%) |
|-----------------------|-------------------------|--------------------------|---------------------|
| Rounds Played         | (85.06, 102.93)         | (95.18, 113.91)          | +11%               |
| Retention (Day 1)     | (0.7800, 0.8290)        | (0.8090, 0.8550)         | +3.4%              |
| Retention (Day 7)     | (0.4130, 0.4750)        | (0.4600, 0.5210)         | +11%               |

- Moving the gate to level 40 improved all key metrics significantly.
- The experimental group had a statistically significant increase in player engagement and retention compared to the control group.

## Conclusion

The experiment demonstrates that moving the gate to level 40 enhances both player engagement and retention. The following actions are recommended:
- **Implementation**: Deploy the new gate position (level 40) across all players.
- **Monitoring**: Track engagement and retention metrics post-implementation to confirm sustained improvements.
- **Future Testing**: Continue using A/B testing to optimize other gameplay elements.

## Dependencies

- Python 3.9 or later
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `teatasting`

## Usage

1. Clone the repository and install the required dependencies.
2. Open the Jupyter notebook (`AB_Test_Cookie_Cats.ipynb`).
3. Execute the cells to replicate the analysis and results.

## Future Work

- Experiment with additional gameplay elements to optimize player engagement.
- Analyze the effects of demographic or geographic segmentation on results.
- Investigate potential long-term effects of the new gate position on player monetization.
