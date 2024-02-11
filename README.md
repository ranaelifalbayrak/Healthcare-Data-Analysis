# Healthcare Data Analysis

## Overview

This project aims to analyze the relationship between various random variables in a healthcare context: exercise frequency (A), caloric intake (B), patient category (C), cholesterol level (D), blood pressure (E),
and Hemoglobin A1c (HbA1c) level (H).

## Problem Statement

- Exercise frequency (A): This represents how often a patient engages in physical exercise per
week. Patients who exercise more frequently are generally associated with better health
outcomes.
A has infinitely many possible values {0, 1, 2,…} and 𝑃(𝑎) = 0.5^(𝑎+1)
- Caloric intake (B): This refers to the kilocalories the patient consumes daily. Higher caloric
intake may lead to weight gain and potential health risks if not balanced with exercise and a
healthy diet.
B is a continuous random variable with the given probability density function:
𝑓(𝑏) = − 0.096𝑏^3 + 0.432𝑏^2 - 0.352𝑏 + 0.08, 𝑥 ≤ 𝑏 ≤ 𝑦
𝑓(𝑏) = (− 2𝑏 + 11)/15, 𝑦 ≤ 𝑏 ≤ 𝑧
𝑓(𝑏) = 0, 𝑒𝑙𝑠𝑒𝑤ℎ𝑒𝑟𝑒

![B](https://github.com/ranaelifalbayrak/Probability-and-Statistics-Term-Project-for-2022-2023-Spring/assets/116919905/748ca138-e0b0-40d0-a2e3-a8dc83bbf60a)


-  Patient category (C): The patient category is determined based on exercise frequency (a) and
caloric intake (b), and this categorization helps assess the patient's overall health risk based on
their fitness and dietary habits.
The categories include "not risky," "risky," and "very risky," and how they are determined is
shown in the graph below:

![C](https://github.com/ranaelifalbayrak/Probability-and-Statistics-Term-Project-for-2022-2023-Spring/assets/116919905/74dfaf34-543c-458c-9ad5-0c59715ba51e)


- Cholesterol level (D): Cholesterol level (mg/dL) measures the amount of cholesterol in the
patient's body. Higher-risk patients tend to have higher cholesterol levels.
D is a continuous random variable with a Normal distribution. It has different parameters for
different patient categories:
- Systolic blood pressure (E): Blood pressure indicates the pressure exerted on the arterial walls
(100mmHg). Higher-risk patients tend to have elevated blood pressure.
E is a continuous random variable with the following cumulative distribution function:
𝐹(𝑒; 𝑖, 𝑗) = (𝑒 − 𝑖)^2 − 𝑗 𝑓𝑜𝑟 (𝑖 + sqrt(𝑗)) ≤ 𝑒 ≤ (𝑖 + sqrt(𝑗 + 1))
It has different parameters for different patient categories:
-  Hemoglobin A1c (HbA1c) level (H): Hemoglobin A1c (HbA1c) level is a specific medical
measurement used to assess long-term blood glucose control in patients with diabetes.
Patients in higher-risk categories tend to have higher HbA1c values, indicating suboptimal
blood glucose control and a greater risk for diabetes-related complications.
H is a continuous random variable with the following probability density function:
𝑓(ℎ) = 𝑘, 0 ≤ ℎ ≤ 1
𝑓(ℎ) = 𝑙, 1 < ℎ ≤ 2
𝑓(ℎ) = 0, 𝑒𝑙𝑠𝑒𝑤ℎ𝑒𝑟𝑒


## Implementation  

The project implementation is divided into several tasks:

- 1. Generation of Synthetic Patient Data:
Implemented algorithms to generate synthetic patient data for each variable.
Generated population data for each random variable using its generator function. Plotted histograms and probability mass/density functions (PMF/PDF) for visualization.
- 2. Sampling and Descriptive Statistics:
Implemented a sampler function to take samples from the population.
Calculated estimators for population mean and variance without using built-in functions like numpy.mean, numpy.std, or numpy.var.
Plotted histograms of estimations with indicators for actual population mean and variance.
- 3. Parameter Estimation:
Estimated distribution parameters using Method of Moments and Method of Maximum Likelihood.
- 4. Confidence Intervals:
Calculated confidence intervals for the population mean of variable A.
- 5. Hypothesis Testing:
Conducted hypothesis testing to determine if the average exercise frequency has increased after a national publicity campaign on physical fitness.
"After a year-long national publicity campaign on physical fitness, a hospital embarks on a mission to
determine if the campaign has been effective. For this purpose, they survey 500 randomly selected
patients and find out that their average exercise frequency is now 1.2. Assuming that the standard
deviation of exercise frequency has not changed, does this mean that, at a 3% significance level, the
mean number of times a patient engages in physical exercise each week has increased?"
- 6. Naive Bayes Classifier:
Applied and evaluated the Naive Bayes classifier for the population.
