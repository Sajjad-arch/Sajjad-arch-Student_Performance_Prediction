# Student Performance Analysis

A statistical analysis project exploring academic performance patterns across 200 students using Python.

## Overview

This project applies foundational statistics and probability concepts — descriptive stats, Bayes' theorem, the Central Limit Theorem, confidence intervals, hypothesis testing, and linear regression — to a real-world student performance dataset.

## Files

| File | Description |
|------|-------------|
| `students_performance.csv` | Dataset: 200 students, 6 columns |
| `Student_Performance_Analysis.ipynb` | Jupyter notebook with full analysis and visualizations |
| `student_performance_analysis.py` | Plain Python script version of the notebook |

## Dataset

The dataset contains the following columns:

- `Gender` — Male / Female
- `Lunch` — standard / free/reduced
- `TestPreparationCourse` — completed / none
- `MathScore` — score out of 100
- `ReadingScore` — score out of 100
- `WritingScore` — score out of 100

## Analysis Sections

### Section 1 — Basic Analysis
- Descriptive statistics (mean, median, standard deviation) for all three subjects
- Histograms, boxplots, and a scatter plot (Math vs. Reading)

### Section 2 — Probability, Bayes' Theorem & CLT
- Probability of scoring above 70 in each subject
- Bayes' theorem: given a high Math score, what is the probability the student completed test preparation?
- Central Limit Theorem verification via 1,000 random samples of size n=30

### Section 3 — Confidence Intervals & Hypothesis Testing
- Shapiro-Wilk normality check on Math scores
- 95% confidence intervals for all three subjects
- Two-sample t-test: is there a statistically significant gender difference in Math performance?

### Section 4 — Correlation & Regression
- Pearson correlation matrix across all three subjects
- Simple linear regression: predicting Math score from Reading score

## Key Findings

| Finding | Result |
|---------|--------|
| Average scores | Math ≈ 68.8, Reading ≈ 70.8, Writing ≈ 70.2 |
| Test preparation | Students who prepared scored 5–8 points higher |
| Bayes' theorem | P(Prep \| HighMath) > P(Prep) — prep correlates with success |
| CLT verification | Sample means form a normal distribution ✓ |
| 95% CI for Math | Approximately [66.5, 71.1] |
| Gender difference in Math | Not significant (p-value = 0.3007) |
| Subject correlations | Strong across all subjects (r = 0.77–0.82) |
| Regression equation | MathScore = 0.85 × ReadingScore + 8.44 (R² = 0.60) |

**Conclusion:** Test preparation is the strongest predictor of higher scores. No significant gender gap exists in Math performance. All three subjects are strongly correlated, and CLT confirms that sampling distributions of means are approximately normal even with a modest population size.

## Requirements

```
pandas
numpy
matplotlib
seaborn
scipy
```

Install with:

```bash
pip install pandas numpy matplotlib seaborn scipy
```

## Usage

**Run the notebook:**

```bash
jupyter notebook Student_Performance_Analysis.ipynb
```

**Run the script:**

```bash
python student_performance_analysis.py
```

Make sure `students_performance.csv` is in the same directory as the script or notebook.

## Tools Used

- **Pandas** — data loading and manipulation
- **Matplotlib / Seaborn** — visualizations
- **SciPy** — statistical tests (Shapiro-Wilk, t-test)
- **NumPy** — numerical computations and sampling
