# Student Performance Prediction
### A Statistical Analysis Project | Statistics & Probability

---

## Project Overview

This project analyzes academic performance data of 200 students using basic statistical methods in Python. It investigates how factors like test preparation and gender relate to student scores in Math, Reading, and Writing.

---

## Files

| File | Description |
|------|-------------|
| `Student_Performance_Analysis_FIXED.ipynb` | Main Jupyter notebook — run this on Google Colab |
| `students_performance.csv` | Dataset (200 students, 6 columns) |
| `README.md` | This file |

---

## Dataset

**200 students, 6 columns:**

| Column | Type | Values |
|--------|------|--------|
| Gender | Categorical | Male, Female |
| Lunch | Categorical | Standard, Free/Reduced |
| TestPreparationCourse | Categorical | Completed, None |
| MathScore | Numerical | 0 – 100 |
| ReadingScore | Numerical | 0 – 100 |
| WritingScore | Numerical | 0 – 100 |

No missing values in the dataset.

---

## Tools & Libraries

- **Python 3.10+**
- `pandas` — data handling
- `numpy` — numerical computation
- `matplotlib` — plotting
- `seaborn` — statistical visualization
- `scipy` — statistical tests

---

## Project Sections

### Section 1 — Basic Statistical Analysis
- Descriptive statistics (Mean, Median, Standard Deviation)
- Missing value check
- Histogram, Boxplot, Scatter Plot

### Section 2 — Probability, Bayes' Theorem & CLT
- Probability of scoring above 70 per subject
- Bayes' Theorem: P(TestPrep | HighMath)
- Central Limit Theorem verification (1000 samples, n=30)

### Section 3 — Confidence Interval & Hypothesis Testing
- Shapiro-Wilk normality test
- 95% Confidence Interval for Math scores
- Independent t-test: gender-based Math performance (H₀ vs H₁)

### Section 4 — Correlation & Regression
- Pearson correlation matrix + heatmap
- Simple linear regression: MathScore = f(ReadingScore)
- R² interpretation

---

## Key Findings

| # | Finding | Result |
|---|---------|--------|
| 1 | Average scores | Math ≈ 68.8, Reading ≈ 70.8, Writing ≈ 70.2 |
| 2 | Test preparation effect | +5 to +8 points higher on average |
| 3 | Bayes' Theorem | P(Prep \| HighMath) > P(Prep) — prep predicts success |
| 4 | CLT verified | Sample means follow normal distribution ✓ |
| 5 | 95% Confidence Interval | Math: approximately [66.5, 71.1] |
| 6 | Gender difference (Math) | Not significant — p-value = 0.3007 |
| 7 | Subject correlation | Strongly correlated (r = 0.77 – 0.82) |
| 8 | Regression equation | MathScore = 0.85 × ReadingScore + 8.44 (R² = 0.60) |

---

## How to Run

1. Open [Google Colab](https://colab.research.google.com)
2. Upload `Student_Performance_Analysis_FIXED.ipynb` via **File → Upload notebook**
3. Upload `students_performance.csv` via the left sidebar 📁 → upload button
4. Click **Runtime → Run All**

> If you get a `FileNotFoundError`, make sure the CSV is uploaded to Colab's file sidebar before running.

---

## Conclusion

Simple statistical methods reveal meaningful patterns in student performance. Test preparation significantly improves scores across all subjects. No gender gap was found in Math performance. All three subjects are strongly correlated, and Reading Score can reasonably predict Math Score using linear regression.

---

*Subject: Statistics & Probability | Southeast University*
