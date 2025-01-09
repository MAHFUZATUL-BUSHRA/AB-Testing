# A/B Testing Analysis

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



---

Feel free to update this README to better fit the specific goals and outcomes of your project.

