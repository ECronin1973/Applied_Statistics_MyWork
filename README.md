# Applied Statistics Assessment Submission

Welcome to my repository for the Applied Statistics module assessment for the academic year 2024/2025. This repository contains my submissions for the module, including detailed tasks and a comprehensive project.

### Overview
This README file is structured into two main sections:

Tasks 2024/2025 Applied Statistics: This section includes various tasks assigned throughout the module, showcasing my understanding and application of statistical concepts and techniques.

Project 2024/2025 Applied Statistics: This section presents my final project, which integrates the knowledge and skills acquired during the course to address a complex statistical problem.

Feel free to explore the repository to see my approach and solutions to the tasks and project. Your feedback is always welcome!

### Contents
tasks.ipynb: This file contains five tasks completed as outlined in the Tasks Section of the [2024 Applied Statistics Module README document](https://github.com/ianmcloughlin/2425_applied_statistics/blob/main/README.md).

project.ipynb: This file contains the completed project work as outlined in the Project Section of the [2024 Applied Statistics Module README document](https://github.com/ianmcloughlin/2425_applied_statistics/blob/main/README.md).

### Author
Name: Edward Cronin

Student ID: g00425645

Email: g00425645@atu.ie

## How to download this repository

1. Logon to GitHub to locate my specific repository dedicated to this project located at [My repository for Applied Statistics on GitHub]( https://github.com/ECronin1973/Applied_Statistics_MyWork) .
2. Click the download button.
3. To run the code, ensure you have Python installed.

## Code of Conduct

A code of conduct governs the use of this repository and has been uploaded within the repository for ease of reference.

# Tasks 2024/2025 Applied Statistics
_______________________________________________________________________________________________________________________________________________________________________________________
# Task 1: Lady Tasting Tea Experiment

### Overview
This project is inspired by the famous “Lady Tasting Tea” experiment, as described in Ronald A. Fisher’s book “The Design of Experiments”. We aim to replicate the experiment with a twist, involving twelve cups of tea, where six cups have milk poured in first and the other six have tea poured in first.

### Objective
A person claims to have the ability to discern whether milk or tea was poured into the cup first just by tasting it. Our objective is to calculate the probability that this person can correctly identify all six cups that had milk poured in first, under the assumption that they are merely guessing without any special powers.

### Experiment Setup
Total Cups: 12
Milk First: 6 cups
Tea First: 6 cups
The participant will taste each cup and determine the order in which milk or tea was poured.

## Probability Calculation 
Calculate the probability that the participant correctly identifies all six ‘milk first’ cups by chance.

### Instructions (PROBABIITY CALCULATION):
Use Python to simulate the experiment.
Assume the participant is guessing; they do not have any special powers.
Justify your workings with comments in code cells and explanations in Markdown cells.

## Allowing Errors
Consider if we are willing to accept one error in the participant’s selection.

### Instructions (ONE ERROR):
Calculate the probability that the participant makes at most one error.
Justify your workings as before.

## Accepting Two Errors
Discuss whether accepting two errors would be reasonable and calculate the corresponding probability.

### Instructions (TWO ERRORS):
Provide a detailed explanation of your reasoning in a Markdown cell.
Calculate the probability as before

## Summary
I have just completed this task, investing considerable time in reviewing the instructor's lectures and setting up my environment with the necessary libraries. After not using Anaconda for over 12 months, I had to delete and reinstall it along with VS-Code and add the Copilot AI extension. I also watched YouTube videos (listed in references) to learn how to use the Copilot AI tool. Additionally, I revised how to create README files and use Markdown language.

In the lecture videos, I discovered various methods of calculating the total number of combinations. To deepen my understanding, I referred to other sources such as www.w3schools.com. Python for Data Analytics provided me with a solid grasp of using Python, plotting, and visualization. To ensure all bases were covered, I included each method in my task as demonstrated by the instructor, adding relevant notes to each section for context.

Further Reading Performed
I explored research on this topic conducted by others. On the site https://lisds.github.io/textbook/wild-pandas/fishers_tea.html, it was noted that 'Muriel guessed correctly for each of the eight cups, and so correctly identified all four milk-first cups'. This test was not performed on an individual but outlined the necessary parameters for a test, comparing 'real-world' results versus the null hypothesis. I analyzed the code on that site and adapted it to display Fisher's table with 12 cups of tea. The four categories outlined in that experiment are also relevant in this test.

I viewed the code in Github and found the printed results too long, instead I researched how extract the results into csv files.  I generated two files, 1. combinations.csv which was created to collect the combinations and to count them, and 2. The overlaps.csv which contained the combination, overlap, and length of overlap between each element of combs and labels_milk. I took this approach to make the tasks.ipynb file more readable. 

## References
The following online resources were used to complete Task 1 in `tasks.ipynb` and compile content in the Task 1 section of the `README.md` document:

1. [ATU Lectures - Applied Statistics, Dr Ian McLoughlin](https://vlegalwaymayo.atu.ie/course/view.php?id=10454)
2. [Writing README.md files on GitHub](https://help.github.com/en/articles/basic-writing-and-formatting-syntax)
3. [Creating tables in Markdown](https://www.makeuseof.com/tag/create-markdown-table/)
4. [Python Documentation - `math.comb`](https://docs.python.org/3/library/math.html#math.comb)
5. [W3Schools - `math.comb`](https://www.w3schools.com/python/ref_math_comb.asp)
6. [W3Schools - `numpy.random.binomial`](https://www.w3schools.com/python/numpy/numpy_random_binomial.asp)
7. [Python Documentation - `math.factorial`](https://docs.python.org/3.12/library/math.html#math.factorial)
8. [Python Documentation - `itertools.combinations`](https://docs.python.org/3/library/itertools.html#itertools.combinations)
9. [Understanding Error Types in Data Analytics](https://en.wikipedia.org/wiki/Type_I_and_type_II_errors#Table_of_error_types)
10. [Understanding Power in Data Analytics](https://en.wikipedia.org/wiki/Power_(statistics)#Description)
11. [Images Not Displaying in GitHub](https://stackoverflow.com/questions/41468951/images-not-displaying-in-github-pages)
12. [GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/overview)
13. [GitHub Documentation - About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
14. [Further Information on The Design of Experiments](https://en.wikipedia.org/wiki/The_Design_of_Experiments)
15. [Fisher's Tea Experiment](https://lisds.github.io/textbook/wild-pandas/fishers_tea.html)
16. *Python for Data Analysis*, Wes McKinney, O'Reilly, Third Edition

# END

# Task 2: Assessing Normality of `numpy.random.normal()`

## Overview
In this task, we will assess whether `numpy.random.normal()` properly generates normal values. We will generate a sample of 100,000 values with a mean of 10.0 and a standard deviation of 3.0. We will then use the `scipy.stats.shapiro()` function to test for normality and visualize the results.

## Steps

1.Generate a Sample
Use the `numpy.random.normal()` function to generate a sample of 100,000 values with a mean of 10.0 and a standard deviation of 3.0.

python
import numpy as np

mean = 10.0
std_dev = 3.0
sample_size = 100000
sample = np.random.normal(mean, std_dev, sample_size)

2.Visualize Data

Create a histogram of the sample values and overlay the probability density function (PDF) of a normal distribution with the same mean and standard deviation.

import matplotlib.pyplot as plt
from scipy.stats import norm

## Plot histogram of the sample
plt.hist(sample, bins=50, edgecolor='black', density=True, alpha=0.8, color='g')

## Plot the corresponding normal distribution
xmin, xmax = plt.xlim()
x = np.linspace(xmin, xmax, 100)
p = norm.pdf(x, mean, std_dev)
plt.plot(x, p, 'k', linewidth=2)
title = f"Fit results: mean = {mean}, std = {std_dev}"
plt.title(title)
plt.show()

3.Test for Normality
Three tests are performed to test for Normality, QQ-Plot, Shapiro-Wilk Test and Kolmogorov-Smirnov Test.  Each test will test if the results come from a normal distribution.

### Shapiro-Wilk Test

Apply the scipy.stats.shapiro() function to test if your sample comes from a normal distribution. The function will return a test statistic and a p-value.

from scipy.stats import shapiro

## Perform the Shapiro-Wilk test for normality
stat, p_value = shapiro(sample[:10000])  # Shapiro test is sensitive to sample sizes > 5000
print(f"Shapiro-Wilk Test: Stat={stat}, p-value={p_value}")

Interpret the output from the Shapiro-Wilk test. If the p-value is greater than 0.05, it suggests that the sample likely comes from a normal distribution. Conversely, a p-value less than 0.05 suggests non-normality.

### QQ-Plot Test ###
Create a Q-Q (Quantile-Quantile) plot to test whether the dataset follows a normal distribution.

from scipy import stats

## Create a Q-Q plot
fig, ax = plt.subplots()
stats.probplot(sample, dist='norm', plot=ax)
plt.show()

### Kolmogorov-Smirnov Test
The kstest function will return a test statistic and a p-value. If the p-value is greater than 0.05, it suggests that the sample likely comes from a normal distribution. Conversely, a p-value less than 0.05 suggests non-normality.

### Integration Test
The 97.5th percentile test is performed to determine if 95% of the area under the normal distribution lies within 1.96 standard deviations away from the mean. 

## Summary of Analysis
According to the website [STATOLOGY](https://www.statology.org/normality-test-python/) there are four common ways to test for Normality in Python.

1. (Visual Method) Create a histogram.
If the histogram is roughly “bell-shaped”, then the data is assumed to be normally distributed.  In this case the shape of the histogram is 'bell shaped'.

2. (Visual Method) Create a Q-Q plot.
If the points in the plot roughly fall along a straight diagonal line, then the data is assumed to be normally distributed. In this case the points do plot roughly along a straight diagonal line.

3. (Formal Statistical Test) Perform a Shapiro-Wilk Test.
If the p-value of the test is greater than α = .05, then the data is assumed to be normally distributed.  P value in this test is (p-value)=0.35617671455482214 so is greater than .05.

4. (Formal Statistical Test) Perform a Kolmogorov-Smirnov Test.
If the p-value of the test is greater than α = .05, then the data is assumed to be normally distributed.  p value in this test is (p-value) 0.7485155595727593 so is greater than 0.05.

5. Integration Test.  
95% of the area under the normal distribution was within 1.96 standard deviations away from the mean.

Based on the results of the above tests we can conclude that the sample is likely normally distributed.

### Further Reading Performed

In order to complete this task, I performed a google search on testing for Normality in Python.  The website Statology gave me a good approach in addition to the great instruction I received when completing the online ATU lectures. I identified a useful youtube video titled 'Normality test - Simply explained'.  This video taught me that there are two ways to test for normal distribution 1. Analytical and 2. Graphically. There are three tests identified for Analytical testing 1. Shapiro-Wilk Test, 2. Kolmogorov-Smirnov Test and 3. Anderson-Darling Test. the objective of each of the tests is to determine if the p-value is smaller than 0.05.  If it is smaller,  Normal Distribution is not assumed.  If greater than 0.05 we assume normal distribution.  The disadvantage of analytical testing is the calculated p-value depends on the sample size (the larger the sample, the smaller the potential p-value). With a very large sample, it could be the case that the p-value is smaller than 0.05 and thus reject the null hypotesis, that it is a normal distribution.  To get around this problem, graphical tests of normal distribution are being used.  For graphical tests we either look at the histogram or QQ-Plot. If using the histogram we plot the normal distribution in the histogram of the data to see whether the curve of the normal distribution roughly corresponds to that of the normal distribution curve. The QQ-Plot is better as the Theoretical Quantiles the data should have if they are perfectly normally distributed and the quantiles of the measured values are compared. If the data is perfectly normally distributed, all points would lie on the line. The more the data deviates form the line, the less it is normall distributed. In addition, data that plots the 95% interval, if all your data lies within this interval, it is a very strong indication that  the data is normally distributed.  The 95% interval was further explored in Wikipedia (97.5th percentile point) where it states in probability and statistics, the 97.5th percentile point of the standard normal distribution is a number commonly used for statistical calculations. The approximate value of this number is 1.96, meaning that 95% of the area under a normal curve lies within approximately 1.96 standard deviations of the mean.    

## Libraries Used
numpy: For numerical operations and generating random samples.
scipy.stats: For statistical tests and probability distributions.
matplotlib: For plotting and visualizing data

## References
The following online resources were used to complete Task 2 in `tasks.ipynb` and compile content in the Task 2 section of the `README.md` document:

1. [ATU Lectures - Applied Statistics, Dr Ian McLoughlin](https://vlegalwaymayo.atu.ie/course/view.php?id=10454)
2. [Writing README.md files on GitHub](https://help.github.com/en/articles/basic-writing-and-formatting-syntax)
3. [Creating tables in Markdown](https://www.makeuseof.com/tag/create-markdown-table/)
4. [NumPy Documentation - `numpy.random.normal`](https://numpy.org/doc/stable/reference/random/generated/numpy.random.normal.html)
5. [NumPy Documentation - `numpy.histogram`](https://numpy.org/doc/stable/reference/generated/numpy.histogram.html)
6. [Normal Distribution - Wikipedia](https://en.wikipedia.org/wiki/Normal_distribution)
7. [Matplotlib Documentation - `matplotlib.pyplot.hist`](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html)
8. [Statsmodels Q-Q Plot](https://www.statsmodels.org/stable/generated/statsmodels.graphics.gofplots.qqplot.html)
9. [SciPy Documentation - `scipy.stats.shapiro`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.shapiro.html)
10. [SciPy Documentation - `scipy.stats.kstest`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.kstest.html)
11. [Normality test - Simply Explained](https://www.youtube.com/watch?v=AVketBmpUTE)
12. [97.5 th Percentile Point](https://en.wikipedia.org/wiki/97.5th_percentile_point)

# END

# Task 3: t-Test Calculation

## Overview
### Analysis of Resting Heart Rates Before and After Exercise Program

## Dataset

This task will consider the following dataset containing resting heart rates for patients before and after embarking on a two-week exercise program.

| Patient ID | 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  | 9  |
|------------|----|----|----|----|----|----|----|----|----|----|
| Before     | 63 | 68 | 70 | 64 | 74 | 67 | 70 | 57 | 66 | 65 |
| After      | 64 | 64 | 68 | 64 | 73 | 70 | 72 | 54 | 61 | 63 |

## Objective

Calculate the t-statistic based on this dataset using Python. Compare it to the value given by `scipy.stats`. Explain the work and list any sources used.

## Task Requirements

1. Calculate the differences between the before and after values.
2. Compute the mean and standard deviation of the differences.
3. Calculate the t-statistic using the formula: 

$$ t = \frac{\bar{d}}{s_d / \sqrt{n}} $$

where:

- $\bar{d}$ is the mean of the differences,

- $s_d$ is the standard deviation of the differences,

- $n$ is the number of observations.

4. Use `scipy.stats` to verify the t-statistic.

## Importing Relevant Libraries
python
import numpy as np
from scipy import stats
import matplotlib.pyplot as plt

Steps to Complete the Task

### Data
before = np.array([63, 68, 70, 64, 74, 67, 70, 57, 66, 65])
after = np.array([64, 64, 68, 64, 73, 70, 72, 54, 61, 63])

### Step 1: Calculate the Differences
differences = before - after

### Step 2: Compute the Mean and Standard Deviation of the Differences
mean_diff = np.mean(differences)
std_diff = np.std(differences, ddof=1)  # ddof=1 for sample standard deviation
n = len(differences)

### Step 3: Calculate the t-statistic
t_statistic = mean_diff / (std_diff / np.sqrt(n))
print(f"Calculated t-statistic: {t_statistic}")

### Step 4: Use scipy.stats to Verify the t-statistic
t_statistic_scipy, p_value = stats.ttest_rel(before, after)
print(f"scipy.stats t-statistic: {t_statistic_scipy}, p-value: {p_value}")

### Results
- Calculated t-statistic: 1.3372274824806283
- scipy.statst-statistic: 1.337227482480628
- p-value: 0.21396011317404623

### Initial Analysis of Values
t-statistic: A t-statistic of 1.337 suggests that the mean difference between the before and after heart rates is 1.337 standard deviations away from zero.
p-value: A p-value of approximately 0.214 indicates that there is a 21.4% chance that the differences observed are due to random variation rather than a true effect of the exercise program. This p-value is greater than the common significance level of 0.05, indicating that the observed differences are not statistically significant.

### Analysis Utilizing Various Charts
__Generate Bar Chart__
x = np.arange(len(before))
width = 0.35  # the width of the bars

fig, ax = plt.subplots()
bars_before = ax.bar(x - width/2, before, width, label='Before', color='blue', alpha=0.7)
bars_after = ax.bar(x + width/2, after, width, label='After', color='green', alpha=0.7)

ax.set_xlabel('Patient ID')
ax.set_ylabel('Heart Rate')
ax.set_title('Heart Rates Before and After Exercise Program')
ax.set_xticks(x)
ax.set_xticklabels(range(len(before)))
ax.legend()

plt.show()

__Generate Line Plot__
plt.figure()
plt.plot(range(len(before)), before, marker='o', linestyle='-', color='blue', label='Before')
plt.plot(range(len(after)), after, marker='o', linestyle='-', color='green', label='After')
plt.xlabel('Patient ID')
plt.ylabel('Heart Rate')
plt.title('Heart Rates Before and After Exercise Program')
plt.legend()
plt.show()

__Generate Scatter Plot__
plt.figure()
plt.scatter(range(len(before)), before, color='blue', label='Before')
plt.scatter(range(len(after)), after, color='green', label='After')
plt.xlabel('Patient ID')
plt.ylabel('Heart Rate')
plt.title('Heart Rates Before and After Exercise Program')
plt.legend()
plt.show()

__Generate Histogram__
plt.figure(figsize=(10, 6))

plt.hist(before, bins=10, color='blue', alpha=0.5, label='Before', edgecolor='black')
plt.hist(after, bins=10, color='green', alpha=0.5, label='After', edgecolor='black')

plt.title('Histogram of Heart Rates Before and After Exercise Program')
plt.xlabel('Heart Rate')
plt.ylabel('Frequency')
plt.legend()

plt.show()

__Generate Box Plot__
plt.figure(figsize=(10, 6))
plt.boxplot([before, after], labels=['Before', 'After'], patch_artist=True,
            boxprops=dict(facecolor='lightblue', color='blue'),
            medianprops=dict(color='red'))

plt.title('Box Plot of Heart Rates Before and After Exercise Program')
plt.xlabel('Condition')
plt.ylabel('Heart Rate')

plt.show()

### Conclusion

The charts displayed values of heart rates before and after an exercise program.  The visual results matched the results of t-statistic which was verified using scipy.stats.
Both the manually calculated t-statistic and the one from scipy.stats are the same, and the p-value suggests that the changes in heart rates are not statistically significant. 

### Assumptions

The t-test makes five key assumptions:

1. Paired Samples
The t-test assumes that the data consists of paired samples. In this case, the heart rates before and after the exercise program are paired for each patient.

2. Normality
The differences between the paired samples (before and after values) should be approximately normally distributed. This assumption is crucial for the validity of the t-test results.

3. Independence
The pairs of observations (before and after values for each patient) should be independent of each other. This means that the heart rate measurements for one patient should not influence the measurements for another patient.

4. Scale of Measurement
The data should be measured on an interval or ratio scale. In this case, heart rates are measured on a ratio scale, which is appropriate for the t-test.

5. No Significant Outliers
The differences between the paired samples should not have significant outliers, as outliers can affect the results of the t-test.

### Summary of Assumptions
Paired Samples: Each before value is paired with an after value for the same patient.

Normality: The differences between the paired samples should be normally distributed.

Independence: The pairs of observations should be independent of each other.

Scale of Measurement: The data should be measured on an interval or ratio scale.

No Significant Outliers: The differences should not have significant outliers.

These assumptions ensured the validity and reliability of these t-test results. If any of these assumptions were violated, the results of the t-test would not be accurate.

## Libraries Used
The folowing libraries were used in Task 3:
NumPy: Essential for numerical computing. It supports arrays, matrices, and functions for high-level mathematical operations.
SciPy: Provides functions for statistical tests, including the paired t-test.
Matplotlib: A 2D plotting library for creating graphs and visualizations.
These libraries are crucial for performing the calculations and visualizations required in this task.

## References
The following online resources were used to complete Task 3 in `tasks.ipynb` and compile content in the Task 3 section of the `README.md` document:

1. [ATU Lectures - Applied Statistics, Dr Ian McLoughlin](https://vlegalwaymayo.atu.ie/course/view.php?id=10454)
2. [Writing README.md files on GitHub](https://help.github.com/en/articles/basic-writing-and-formatting-syntax)
3. [Creating tables in Markdown](https://www.makeuseof.com/tag/create-markdown-table/)
4. [Statistical functions](https://docs.scipy.org/doc/scipy/reference/stats.html#statistical-functions-scipy-stats)
5. [scipy.stats](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_rel.html#ttest-rel)
6. [Statology - The Four Assumptions Made in a T-Test](https://www.statology.org/t-test-assumptions/): This article explains the four key assumptions of a t-test, including independence, normality, homogeneity of variances, and random sampling.
7. [Statistics for Research Students - Independent T-Test Assumptions](https://usq.pressbooks.pub/statisticsforresearchstudents/chapter/independent-t-test-assumptions/): This resource provides a detailed explanation of the assumptions underlying the independent t-test and how to interpret the results.
8. [Statistics By Jim - T Test Overview](https://statisticsbyjim.com/hypothesis-testing/t-test/) : How to Use & Examples: This article offers an overview of different types of t-tests, their assumptions, and examples of how to use them.
9. [Real Statistics Using Excel - Violations of T-Test Assumptions](https://real-statistics.com/students-t-distribution/problems-data-t-tests/): This page discusses what to do when the assumptions of a t-test are violated and provides references for further reading.
10. [Datanovia - Independent T-Test Assumptions](https://www.datanovia.com/en/lessons/t-test-assumptions/independent-t-test-assumptions/): This tutorial explains the assumptions of the independent t-test and provides examples of how to check these assumptions using R.

# END


# Task Four

# Task Five





_______________________________________________________________________________________________________________________________________________________________________________________

# Project 2024/2025 Applied Statistics

### PlantGrowth Analysis 
 
### Overview
This project analyzes the PlantGrowth dataset from Vicent Arel-Bundocks Rdatasets page. The dataset contains two main variables: a treatment group and the weight of plants within those groups. 

## Steps
1. **Download and Save the Dataset**: 
- The dataset was downloaded from [Vicent Arel-Bundocks Rdatasets page](https://vincentarelbundock.github.io/Rdatasets/datasets.html) and saved to the repository.

 2. **Describe the Dataset**: 
 - The dataset was loaded into pandas DataFrame as it is a common practice in data analysis for several reasons:
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html

1. Ease of Data Manipulation
DataFrames provide a powerful and flexible way to manipulate and analyze data. They allow you to easily filter, sort, and transform data using intuitive syntax.
For example, you can quickly select specific rows or columns, apply functions to the data, and perform aggregations.
"Ease of Data Manipulation." pandas documentation, https://pandas.pydata.org/docs/.

2. Integration with Other Libraries
pandas integrates seamlessly with other Python libraries commonly used in data analysis, such as NumPy, SciPy, Matplotlib, and Seaborn.
This integration makes it easy to perform complex statistical analyses, create visualizations, and conduct machine learning tasks.
"Integration with Other Libraries." pandas documentation, https://pandas.pydata.org/docs/user_guide/index.html.

3. Handling Missing Data
DataFrames provide robust methods for handling missing data. You can easily identify, fill, or drop missing values, ensuring that your analysis is accurate and reliable.
"Handling Missing Data." pandas documentation, https://pandas.pydata.org/docs/user_guide/missing_data.html.

4. Data Cleaning and Preparation
pandas offers a wide range of functions for cleaning and preparing data. You can remove duplicates, convert data types, and handle categorical data with ease.
This is crucial for ensuring that your data is in the right format for analysis.
"Data Cleaning and Preparation." pandas documentation, https://pandas.pydata.org/docs/user_guide/index.html.

5. Descriptive Statistics and Summarization
DataFrames make it easy to generate descriptive statistics and summaries of your data. You can quickly calculate measures such as mean, median, standard deviation, and more.
This helps you understand the distribution and characteristics of your data before performing more advanced analyses.
"Descriptive Statistics and Summarization." pandas documentation, https://pandas.pydata.org/docs/user_guide/index.html.


6. Data Visualization
pandas works well with visualization libraries like Matplotlib and Seaborn. You can create a wide range of plots and charts to visualize your data and gain insights.
Visualizations are essential for communicating your findings and making data-driven decisions 
"Data Visualization." pandas documentation, https://pandas.pydata.org/docs/user_guide/index.html.

 __Exploration of Dataset__
  To get an initial look at the dataset, the first few rows were displayed using the head() method. This gives us a quick overview of the data.  Next, we provide a summary of the dataset using the describe() method. This method gives us important statistical information about the numerical columns in the dataset, such as the count, mean, standard deviation, minimum, and maximum values.
 
 __A summary of the dataset__
 Observations: The dataset contains 30 observations ie. there are 30 individual data points or entries in the dataset. Each observation represents a single instance of data collected for analysis. In this case, each observation corresponds to the weight of a plant and the treatment group it belongs to.

 Variables: There are three variables in the dataset weight:
 https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.columns.html

 Unnamed: 0: This appears to be an index column t appears to be automatically generated when the dataset was created and can be ignored for analysis.
 https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.drop.html

 weight: This is a numerical variable representing the weight of the plants.  It is measured in some unit (likely grams or kilograms, though the dataset does not specify)
 https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html

 group: This is a categorical variable representing the treatment group to which each plant belongs. The groups are ctrl (control), trt1 (treatment 1), and trt2 (treatment 2).
 https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.groupby.html

 Data Types: The weight variable is of type float64, the Unnamed: 0 variable is of type int64, and the group variable is of type object.
 https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.dtypes.html

 
 3. **Perform t-tests and ANOVA**: 
 - A t-test was performed to determine if there is a significant difference between the two treatment groups (trt1 and trt2). 
 - ANOVA was performed to determine if there is a significant difference between the three treatment groups (ctrl, trt1, and trt2). 
 
 4. **Explain Your Work**: 
 - A t-test is a statistical test used to compare the means of two groups. It assumes that the data is normally distributed and that the variances of the two groups are equal. 
 - ANOVA (Analysis of Variance) is used to compare the means of three or more groups. It is more appropriate than multiple t-tests when analyzing more than two groups because it reduces the risk of Type I errors. 
 
 ## Results 
  - The t-test between trt1 and trt2 showed a p-value of X, indicating that there is/is not a significant difference between the two groups. 
 - The ANOVA between ctrl, trt1, and trt2 showed a p-value of Y, indicating that there is/is not a significant difference between the three groups. 
 
 ## Conclusion 
 Based on the analysis, we can conclude that...
