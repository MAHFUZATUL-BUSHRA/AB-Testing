# A/B Testing Analysis - TWO SEO (Search Engine Optimization)/Digital Marketing Campaign.

This project implements an A/B testing analysis pipeline using Python, aiming to compare the performance of two groups—Control (Group A) and Test (Group B)—across various metrics. The dataset is processed and analyzed to extract actionable insights about user behavior and group performance differences.

## Project Overview
A/B testing is a powerful statistical method used to compare two variations of a single variable to determine which performs better. This project:

- Loads datasets containing key metrics such as impressions, clicks, purchases, and earnings.
- Performs feature engineering to compute derived metrics like conversion rate and earnings per purchase.
- Conducts hypothesis testing (normality, homogeneity, and significance tests) to compare the groups.
- Visualizes data distributions and results through various plots.

## Key Features
1. **Data Loading and Inspection**:
   - Reads datasets for Group A and Group B from separate Excel sheets.
   - Explores data structure, types, and summary statistics.

2. **Feature Engineering**:
   - Conversion Rate: `Conversion Rate = (Purchases / Clicks) * 100`
   - Earnings Per Purchase: `Earnings Per Purchase = Earnings / Purchases`

3. **Data Visualization**:
   - Histograms and density plots to visualize metric distributions.
   - Box plots to compare group distributions.

4. **Statistical Analysis**:
   - Shapiro-Wilk test for normality.
   - Levene’s test for homogeneity of variances.
   - Independent t-tests for normally distributed data with equal variances.
   - Mann-Whitney U test for non-parametric data.

5. **Graphical Insights**:
   - Generates graphs to compare impressions, clicks, purchases, earnings, conversion rates, and earnings per purchase across groups.

## Dataset
The dataset is provided in an Excel file `ab_testing_data.xlsx`, with the following sheets:
- **Control Group (Group A)**
- **Test Group (Group B)**

### Sample Columns:
- Impression
- Click
- Purchase
- Earning

### Derived Columns:
- Conversion Rate
- Earning per Purchase

## Statistical Tests
The project performs several statistical tests to validate hypotheses:

1. **Normality Test**:
   - Shapiro-Wilk test to check if the data follows a normal distribution.

2. **Homogeneity of Variance Test**:
   - Levene’s test to verify if the variances of the groups are equal.

3. **Parametric Tests**:
   - Independent t-tests for normally distributed data with equal variances.

4. **Non-Parametric Tests**:
   - Mann-Whitney U test for data not meeting normality assumptions or homogeneity of variance.

## Results Summary
### Conversion Rate Analysis:
- Mann-Whitney U test indicates significant differences between Group A and Group B.
- Median conversion rate of Group B is significantly higher than Group A.

### Other Metrics:
- Insights are provided for impressions, clicks, purchases, and earnings using appropriate statistical methods.

## Dependencies
- Python 3.8+
- pandas
- scipy
- seaborn
- matplotlib
- termcolor
- sklearn

## Visualization Samples
### Example Graphs
- Histograms comparing distributions of metrics for Group A and Group B.
- Box plots for visualizing variance and central tendency.
#### Clicks
![p](https://github.com/MAHFUZATUL-BUSHRA/AB-Testing/blob/main/graphs/click.png)
#### Impressions
![p2](https://github.com/MAHFUZATUL-BUSHRA/AB-Testing/blob/main/graphs/impression.png)
#### Purchase
![p3](https://github.com/MAHFUZATUL-BUSHRA/AB-Testing/blob/main/graphs/purchase.png)
#### Earnings
![p4](https://github.com/MAHFUZATUL-BUSHRA/AB-Testing/blob/main/graphs/earning.png)
#### EarningPerPurchase
![p5](https://github.com/MAHFUZATUL-BUSHRA/AB-Testing/blob/main/graphs/earning%20per%20purchase.png)
#### Convertion Rate
![p6](https://github.com/MAHFUZATUL-BUSHRA/AB-Testing/blob/main/graphs/conversion%20rate.png)


## Future Improvements
- Include automated outlier detection and handling.
- Add support for larger datasets with performance optimizations.
- Enhance visualizations with interactive dashboards (e.g., using Plotly).
- Can Apply Same method for other datasets also!

## Contributing
Contributions are welcome! Please fork this repository and submit a pull request for any proposed changes.

# 🔍 Additional A/B Testing Analysis – Search Optimization Dataset
🧪 A/B Test #2 – User Engagement & CTR Experiment (Ads Experience Test)

This A/B test analyzes the impact of a new ads experience on user engagement and CTR.
It uses four datasets covering pre-test metrics, assignments, and full activity logs.

## 📘 1. Objective

#### Evaluate whether introducing a new ads experience:

- Increases user activity (primary metric: activity_level)
- Maintains or improves guardrail metrics (DAU & CTR)
- Avoids any pre-test bias
- Achieves statistical significance

## 📁 2. Datasets Used

1.Activity_pretest.csv – Pre-test user activity (used for DAU baseline)
2.Ctr_pretest.csv – Pre-test click-through rates
3.Assignments.csv – Test/control group assignments
4.Activity_all.csv – Full activity logs before and during the experiment

## 📊 3. Pre-Test Analysis
#### Daily Active Users (DAU)
- 31 days of data
- Mean DAU: ~30,673
- Std Dev: 91
- DAU trends are stable → good baseline for experimentation
#### CTR
- Mean CTR: 33%
- Std Dev: 1.73
- Minimum detectable effect (MDE): ~2%
Pre-test results show stable and consistent behavior, enabling reliable test setup.

## 📐 4. Sample Size & Power Calculations
CTR (Binomial Test)
- Baseline CTR = 0.33
- MDE = 0.02
- α = 0.05, β = 0.2
➡️ Required sample size: ≈ 8,807 users per group

DAU (Continuous Metric)
- SD = 91
- MDE = 300 (≈1% increase)
 ➡️ Required duration: ≈ 2 days

## 🔁 5. Group Assignment Validation

Assignments.csv contains 60,000 users:
- Control users	29,951
- Treatment	users 30,049
- Distribution is balanced (mean groupid ≈ 0.50)
- No assignment irregularities across dates
✔ No allocation bias

## 📈 6. Engagement & Guardrail Metrics
### Activity Level (Per-User Engagement)

#### Before Test (Oct):

- Both groups ≈ 5.25 mean activity → identical

#### After Test (Nov):

- Control: ~5.4
- Treatment: ~10.0
✔ Strong performance lift in treatment group

### Daily Active Users (DAU)

#### Before Test:

- Control mean ≈ 15,320
- Treatment mean ≈ 15,352
- t-test p = 0.16 → No pre-test difference

#### After Test:

- Control DAU ≈ 15,782
- Treatment DAU ≈ 29,302
 ✔ Large gain without harming guardrails

### 🧪 7. Statistical Testing
#### Activity Level (Per-User)

#### Two-sample t-test:
- p-value = 0.0

➡️ Reject H₀ → Significant improvement in engagement

#### Active User Count

- Pre-test: No significant difference
- Post-test: Strong and significant difference

✔ Results are statistically valid
✔ No pre-test bias detected

### 📈 Visualizations Included

![p](https://github.com/MAHFUZATUL-BUSHRA/AB-Testing/blob/main/result.png)

### ✅ 8. Conclusion

The new ads experience significantly increases user engagement:

✔ Higher per-user activity
✔ Substantially more daily active users
✔ No negative impact on key guardrail metrics
✔ Statistically significant (p < 0.05)

➡️ Recommendation: Roll out the new ads experience.

---

Feel free to update this README to better fit the specific goals and outcomes of your project.

