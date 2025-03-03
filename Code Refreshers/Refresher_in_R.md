# R Refresher Workshop

You can compare your final results or review code on Answers.Rmd file

## Introduction
Welcome to the R refresher workshop! In this workshop, we'll work with one of R's built-in datasets and explore fundamental statistics and data science concepts.

We will be using the `mtcars` dataset, which is available in R by default.

## Dataset: `mtcars`
The `mtcars` dataset provides information about various car models, including miles per gallon (mpg), number of cylinders (cyl), horsepower (hp), and more.

---

### Problem 1: Descriptive Statistics

#### Task:
1. Load the `mtcars` dataset: data(mtcars)
2. Compute the summary statistics (mean, median, range, and standard deviation) for the variable `mpg`.

---

### Problem 2: Data Visualization

#### Task:
1. Create a histogram of the `mpg` variable.
2. Create a scatter plot comparing `mpg` to `hp`.

---

### Problem 3: Correlation

#### Task:
1. Compute the correlation between the `mpg` and `hp` variables.
2. Interpret the result.

---

### Problem 4: Linear Regression

#### Task:
1. Fit a linear regression model to predict `mpg` based on `hp` (horsepower).
2. Plot the regression line along with the data points.
3. Summarize the model output.

---

### Problem 5: Grouping and Aggregation

#### Task:
1. Group the data by the number of cylinders (`cyl`) and compute the average `mpg` for each group.

---

### Problem 6: Outliers Detection

#### Task:
1. Use the `boxplot` function to identify potential outliers in the `mpg`, `hp`, `wt`, and `qsec` variables.
2. Display the outliers (if any).

---

## Bonus Questions - EDA Driven (answers may vary)

### Bonus 1: Visualizing Relationships Between Multiple Variables

#### Task:
1. Create a **pair plot** (scatterplot matrix) to visualize the relationships between `mpg`, `hp`, `wt` (weight), and `qsec` (1/4 mile time).
2. Which pair of variables seems to have the strongest relationship? Interpret the results.

### Bonus 2: Distribution Analysis

#### Task:
1. Create **density plots** for the variables `mpg`, `hp`, and `wt`. How are these variables distributed? Are they skewed or approximately normal?

### Bonus 3: Identifying Multicollinearity

#### Task:
1. Use the **correlation matrix** to identify pairs of variables that are highly correlated (correlation coefficient > 0.8).
2. Is there any multicollinearity between predictors in this dataset? What might this mean in the context of regression modeling?

### Bonus 4: Creating a Heatmap of Correlations

#### Task:
1. Create a **heatmap** to visualize the correlation matrix of all the numerical variables in the `mtcars` dataset.
2. Highlight any interesting correlations (either positive or negative) that could be insightful.

### Bonus 5: Identifying Trends by Cylinder Group

#### Task:
1. Create a **boxplot** to compare the distribution of `mpg` for different numbers of cylinders (`cyl`).
2. Are there significant differences in `mpg` based on the number of cylinders? What does this tell you about the data?


