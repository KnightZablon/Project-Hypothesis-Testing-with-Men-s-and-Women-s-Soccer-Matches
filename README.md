# Project-Hypothesis-Testing-with-Men-s-and-Women-s-Soccer-Matches

In this project, I worked as a sports journalist at a major online sports media company and aimed to investigate whether more goals are scored in women's international soccer matches than in men's. This was based on my intuition, but I wanted to validate the claim using statistical analysis.

Steps I Took:
Data Loading: The first step was to load two datasets: one containing results from men's international soccer matches and another containing results from women's international soccer matches. These datasets were stored in CSV files named men_results.csv and women_results.csv.

Data Filtering: I filtered the data to include only official FIFA World Cup matches, starting from January 1, 2002, onward. This was necessary to focus on matches from the most recent tournaments and ensure consistency in the analysis.

Data Transformation: To prepare the data for analysis, I created new columns to track the total number of goals scored in each match. This was calculated by adding the home and away scores from each match. I also added a "group" column to distinguish between men's and women's matches.

Visualization: I plotted histograms of the goals scored in both men's and women's matches. This helped me visually inspect the distribution of goals and assess the normality of the data. It became clear that the goals scored data was not normally distributed, which led me to choose a non-parametric statistical test.

Statistical Hypothesis: To test my hypothesis, I set up the null and alternative hypotheses:

Null hypothesis (H₀): The mean number of goals scored in women's international soccer matches is the same as in men's.
Alternative hypothesis (H₁): The mean number of goals scored in women's international soccer matches is greater than in men's.
Statistical Test Selection: Since the data was not normally distributed, I opted for the Wilcoxon-Mann-Whitney test, a non-parametric test for comparing the distributions of two independent groups. This test would allow me to determine if the distribution of goals scored in women's matches is significantly greater than in men's.

Performing the Test: I used two methods to perform the test:

Pingouin library: I used the pingouin.mwu() function to perform a right-tailed Wilcoxon-Mann-Whitney test, which compares the number of goals scored in women's matches to that in men's matches.
SciPy library: For validation, I also used the mannwhitneyu() function from the SciPy library to perform the same test.
Hypothesis Test Interpretation: I extracted the p-value from the results of both tests. If the p-value was less than or equal to the significance level of 0.01 (10% significance level), I would reject the null hypothesis. If the p-value was greater, I would fail to reject the null hypothesis.

Conclusion: Based on the p-value obtained from the test, I determined whether there was sufficient evidence to reject the null hypothesis and conclude that more goals are scored in women's matches than in men's.

Outcome:
Through this statistical analysis, I was able to validate or refute my initial hypothesis. The results would either support the idea that women's international soccer matches have more goals on average or suggest that the scoring patterns are not significantly different between the two groups. This investigation helped provide data-driven insights for an engaging and informative article that would be well-received by the audience.
