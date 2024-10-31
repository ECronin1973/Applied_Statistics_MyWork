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

_______________________________________________________________________________________________________________________________________________________________________________________

# Task 2: Assessing Normality of `numpy.random.normal()`

## Overview
In this task, we will assess whether `numpy.random.normal()` properly generates normal values. We will generate a sample of 100,000 values with a mean of 10.0 and a standard deviation of 3.0. We will then use the `scipy.stats.shapiro()` function to test for normality and visualize the results.

## Steps

1.Generate a Sample
Use the `numpy.random.normal()` function to generate a sample of 100,000 values with a mean of 10.0 and a standard deviation of 3.0.

```python
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


_______________________________________________________________________________________________________________________________________________________________________________________









# Task Three

# Task Four

# Task Five





_______________________________________________________________________________________________________________________________________________________________________________________

# Project 2024/2025 Applied Statistics

### Overview
In this project, you will analyze the [PlantGrowth R dataset](https://vincentarelbundock.github.io/Rdatasets/csv/datasets/PlantGrowth.csv).
You will find [a short description](https://vincentarelbundock.github.io/Rdatasets/doc/datasets/PlantGrowth.html) of it on [Vicent Arel-Bundock's Rdatasets page](https://vincentarelbundock.github.io/Rdatasets/).
The dataset contains two main variables, a treatment group and the weight of plants within those groups.

### Objective
Your task is to perform t-tests and ANOVA on this dataset while describing the dataset and explaining your work.

In doing this you should:
1. Download and save the dataset to your repository.
2. Describe the data set in your notebook.
3. Describe what a t-test is, how it works, and what the assumptions are.
3. Perform a t-test to determine whether there is a significant difference between the two treatment groups `trt1` and `trt2`.
4. Perform ANOVA to determine whether there is a significant difference between the three treatment groups `ctrl`, `trt1`, and `trt2`.
5. Explain why it is more appropriate to apply ANOVA rather than several t-tests when analyzing more than two groups.

