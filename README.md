# Applied Statistics: Problem Solutions

This repository contains solutions to four applied statistics problems completed in a single Jupyter notebook: `problems.ipynb`

---

## Repository Structure
```
├── problems.ipynb      # Main notebook with all solutions
├── README.md           # Documentation 
├── requirements.txt    # Python dependencies
└── .gitignore          # Ignore unnecessary files
```

---

## Packages Used and Documentation
- **Python Standard Library:**
  - [math](https://docs.python.org/3/library/math.html) – Mathematical functions
  - [itertools](https://docs.python.org/3/library/itertools.html) – Combinatorics
  - [random](https://docs.python.org/3/library/random.html) – Random sampling
- **Third-Party Libraries:**
  - [numpy](https://numpy.org/doc/stable/reference/index.html) – Numerical operations
  - [pandas](https://pandas.pydata.org/docs/) – Data manipulation
  - [matplotlib](https://matplotlib.org/stable/contents.html) – Data visualization
  - [scipy.stats](https://docs.scipy.org/doc/scipy/reference/stats.html) – Statistical tests (t-test, ANOVA)
- **Jupyter Notebook:** [Jupyter Documentation](https://jupyter.org/documentation)

---

## Problems Overview

### Problem 1: Lady Tasting Tea Experiment
**Goal:** Extend Fisher’s classic hypothesis test to 12 cups (8 tea-first, 4 milk-first) and calculate probabilities of correct guesses by chance.

**What the code does:**
- Creates a `pandas` DataFrame representing 12 cups with brewing method and guesses.
- Randomizes order using `DataFrame.sample()`.
- Calculates number of combinations using `math.comb()` and probability of guessing all correctly.
- Uses `itertools.combinations()` to generate all possible selections and compares overlaps.
- Visualizes distribution of correct guesses using a bar chart.
- Computes probabilities for guessing 0, 1, 2, or 3 cups correctly.

**References:** [Lady Tasting Tea](https://jyyna.co.uk/lady-tasting-tea/), [Significance Thresholds](https://measuringu.com/setting-alpha/)

---

### Problem 2: Normal Distribution Simulation
**Goal:** Compare sample vs population standard deviation across 100,000 samples of size 10.

**What the code does:**
- Generates samples using `numpy.random.normal()`.
- Calculates sample SD (`ddof=1`) and population SD (`ddof=0`).
- Plots histograms of both distributions using `matplotlib`.

**References:** [Standard Deviation Explained](https://www.khanacademy.org/math/statistics-probability/summarizing-quantitative-data/variance-standard-deviation-sample/a/population-and-sample-standard-deviation-review)

---

### Problem 3: Independent Samples t-Test
**Goal:** Simulate t-tests to evaluate Type II error rates when detecting differences in means between two groups.

**What the code does:**
- Defines mean differences from 0 to 1 in 0.1 increments.
- Runs 1000 simulations for each difference.
- Performs t-tests using `scipy.stats.ttest_ind()`.
- Calculates proportion of times null hypothesis was not rejected (Type II error).
- Plots mean difference vs Type II error rate.

**References:** [t-Test Overview](https://www.jmp.com/en/statistics-knowledge-portal/t-test), [Statistical Power](https://www.ebmconsult.com/articles/statistics-power-1-beta)

---

### Problem 4: One-Way ANOVA
**Goal:** Compare means of three groups using ANOVA and post-hoc tests.

**What the code does:**
- Generates three samples from normal distributions with different means.
- Displays descriptive statistics using `pandas`.
- Performs ANOVA using `scipy.stats.f_oneway()`.
- Runs pairwise t-tests and applies Bonferroni correction.

**References:** [ANOVA Guide](https://www.graphpad.com/guides/the-ultimate-guide-to-anova), [One-Way ANOVA 1](https://statistics.laerd.com/statistical-guides/one-way-anova-statistical-guide.php), [One-Way ANOVA 2](https://statistics.laerd.com/statistical-guides/one-way-anova-statistical-guide-2.php), [Bonferroni Correction](https://statisticsbyjim.com/hypothesis-testing/bonferroni-correction/)


