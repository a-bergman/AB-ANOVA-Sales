# Problem Statement

This data set is from [Kaggle](https://www.kaggle.com/datasets/chebotinaa/fast-food-marketing-campaign-ab-test/data).

A fast food restaurant wants to add a new menu item, but are unsure which campaign to use. They ran 3 campaigns at several locations in randomly selected markets with a different promotion being used at each location and then recorded sales for four weeks.

Our task is to identify the most effective promotion by conducting an A/B test via Python in Google Colab.

# What Is An A/B Test And Why Run One?

Simply put, an A/B test is a way of comparing two or more versions of any kind asset to determine which performs better.

A/B testing typically is part of a larger pipeline (randomization, observation, data collection, and analysis against KPIs), but for this experiment we only have the collected data.

# Procedure

Our process is composed of multiple parts:

- Data Exploration
- Data Visualizations
- Statistical Testing
- Additional Statistical Testing
- Conclusions

# Hypotheses

H<sub>0</sub>: There is no difference between the three promotions being tested

H<sub>A</sub>: At least one promotion leads to increased weekly sales compared to the others

# Results & Recommendations

After exploring and visualizing our data, we ran 3 tests:

- Levene's Test (variance of homogeneity)
- An ANOVA Test (Kruskal-Willis)
- A Post-Hoc Test (Tukey's HSD)

-----

Key Results:

- We were able to reject H<sub>0</sub>: Promotion 1 outperformed the other two promotions.
    - Promotions 1 and Promotion 3 outperformed Promotion 2, but there is no statistically significant difference between Promotions 1 and Promotion 3.
- Market size, especially large market size, is a significant driver of sales.

Additional Results:

- Sales were consistent across all four weeks.
- Store age is not correlated with sales.
- Market size, experiment week, and the promotion are not correlated.

Recommendations:

- The business should proceed with either Promotion 1 or Promotion 3.

- Conduct additional research on market size to properly assess its impact on sales.