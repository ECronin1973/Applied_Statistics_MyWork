# My Assessment Repository

This repository contains my assessment submission for the module Applied Statistics

# Tasks 2024/2025 Applied Statistics
# Project 2024/2025 Applied Statistics

The tasks.ipynb file within this repository consists of five tasks completed as outlined in the Tasks Section of the 2024 Applied Statistics Module README document [Link to Document](https://github.com/ianmcloughlin/2425_applied_statistics/blob/main/README.md)

The project.ipynb file within this repository consists of completed project work as outlined in the Project Section of the 2024 Applied Statistics Module README document [Link to Document](https://github.com/ianmcloughlin/2425_applied_statistics/blob/main/README.md)

Author: Edward Cronin g00425645
Author email: g00425645@atu.ie

# How to download this repository

1. Logon to GitHub to locate my specific repository dedicated to this project located at [My repository for Applied Statistics on GitHub]( https://github.com/ECronin1973/Applied_Statistics_MyWork) .
2. Click the download button.
3. To run the code, ensure you have Python installed.

## Code of Conduct

A code of conduct governs the use of this repository and has been uploaded within the repository for ease of reference.

# Task One

## Lady Tasting Tea Experiment

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

_______________________________________________________________________________________________________________________________________________________________________________________

# Task Two

# Task Three

# Task Four

# Task Five



# REFERENCES
The following online resources were used to complete these tasks and compile this README.md document. 
1. ATU Lectures - Applied Statistics, Dr Ian McLoughlin (https://vlegalwaymayo.atu.ie/course/view.php?id=10454)
2. Writing readme.md files on Github (https://help.github.com/en/articles/basic-writing-and-formatting-syntax)
3. Creating tables in markdown (https://www.makeuseof.com/tag/create-markdown-table/)
4. https://docs.python.org/3/library/math.html#math.comb (Task One)
5. https://www.w3schools.com/python/ref_math_comb.asp (Task One)
6. https://www.w3schools.com/python/numpy/numpy_random_binomial.asp (Task One)
7. https://docs.python.org/3.12/library/math.html#math.factorial (Task One)
8. https://docs.python.org/3/library/itertools.html#itertools.combinations (Task One)
9. Understanding error types in Data Analytics: https://en.wikipedia.org/wiki/Type_I_and_type_II_errors#Table_of_error_types (Task One)
10. Understanding Power in Data Analytics: https://en.wikipedia.org/wiki/Power_(statistics)#Description (Task One)
11. Images not displaying in Github : https://stackoverflow.com/questions/41468951/images-not-displaying-in-github-pages (Task One)
12. GitHub Copilot in VS Code : https://code.visualstudio.com/docs/copilot/overview (Task One)
13. https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes (all tasks)
14. Further information the Design on Experiments: https://en.wikipedia.org/wiki/The_Design_of_Experiments (Task One)
15. https://lisds.github.io/textbook/wild-pandas/fishers_tea.html (Task One)
16. Python for Data Analysis, Wes McKinney, O Reilly, Third Edition

_______________________________________________________________________________________________________________________________________________________________________________________

# Project

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

