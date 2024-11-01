# Wage Analysis by Gender

This repository contains the solution to a homework assignment for the course **BI-PST Probability and Statistics** at the Faculty of Information Technology, Czech Technical University in Prague. The objective is to statistically analyze data on starting salaries of men and women and compare these two groups.

**The task was performed in a team with other two students of the course.**

## Task Description

We were assigned data from the dataset **case0102** from the **Sleuth2** library in R, which contains information about starting salaries of men and women. The dataset includes a total of 93 observations:

- **61 women**
- **32 men**

The task is to perform a statistical analysis of these data according to the following steps:

1. **Data Loading and Group Separation**: Split the data into two groups based on gender (men and women). Provide a brief description of the data and the research problem. Estimate the mean, variance, and median for each group separately.

2. **Density and Distribution Function Estimation**: For each group, estimate the density using histograms and the distribution function using empirical distribution functions.

3. **Finding the Closest Distribution**: Estimate the parameters of normal, exponential, and uniform distributions for each group. Plot the corresponding densities with the estimated parameters onto the histograms. Discuss which distribution best fits the observed data.

4. **Generating Random Samples**: For each group, generate a random sample of 100 values from the selected distribution with the estimated parameters. Compare the histograms of the simulated values with the observed data and discuss the similarities.

5. **Calculating Confidence Intervals**: Calculate a two-sided 95% confidence interval for the mean for each group separately.

6. **Hypothesis Testing about the Mean**: At a significance level of 5%, test whether the mean is equal to the value K (in our case, K = 27) against a two-sided alternative. Interpret the results.

7. **Testing Equality of Means Between Groups**: At a significance level of 5%, test whether both groups have the same mean. Choose an appropriate test (two-sample t-test) and interpret the results.

## Project Structure

- **uloha.ipynb**: A Jupyter notebook containing all the code and outputs of the analysis.
- **case0102.csv**: The data file with information on salaries of men and women.
- **README.md**: This file, providing an overview of the project.

## Summary of Approach and Results

- **Data Loading and Preparation**: The data were loaded and divided into two groups based on gender.

- **Descriptive Statistics**:

    - **Men**:
        - **Mean**: Approximately 1730.70
        - **Variance**: Approximately 354778.88
        - **Median**: 1600.00
    - **Women**:
        - **Mean**: Approximately 1030.08
        - **Variance**: Approximately 236611.86
        - **Median**: 999.00

- **Distribution Estimation**: Based on graphical visualizations and parameter estimates, it was determined that the **normal distribution** best fits the data for both groups.

- **Generating Random Samples**: Random samples were generated for men and women from the normal distribution with the estimated parameters and compared with the original data. The histograms showed similar distributions.

- **Confidence Intervals**:

    - **Men**: The 95% confidence interval for the mean is (1527.32, 1934.08).
    - **Women**: The 95% confidence interval for the mean is (950.06, 1110.10).

- **Hypothesis Testing**:

    - **Hypothesis about Mean Equal to K (27)**:

        - **For Women**: The null hypothesis was rejected; the mean significantly differs from 27.
        - **For Men**: The null hypothesis was rejected; the mean significantly differs from 27.

    - **Hypothesis of Equal Means Between Groups**:

        - Using a two-sample t-test, the null hypothesis of equal means was rejected (test statistic T ≈ 6.29, critical value ≈ ±1.99). This indicates a statistically significant difference in average salaries between men and women.

## Conclusion

The data analysis revealed a statistically significant difference in starting salaries between men and women, with men having higher average salaries than women. This conclusion is supported by the results of the two-sample t-test at a 5% significance level. The parameter estimates and graphical visualizations support the assumption that the data are approximately normally distributed for both groups.

---

**Note**: Analysis performed using Python libraries (pandas, numpy, scipy, matplotlib).