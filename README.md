# COMP1844 — Summer 2026 — Tutorial 04: Data Processing Techniques

### Overview

This tutorial session aligns with **Lecture 4** (CSV I/O, pandas Series & DataFrames, data preprocessing) and extends the skills from **Tutorial 03** (visualisation and EDA).

The repository contains **two student notebooks** in the `notebooks/` folder. Each notebook lists exercises as markdown questions with empty code cells — **no solutions are included**. Work through the tasks in your own notebook cells.

| Notebook | Focus | Data |
|----------|-------|------|
| [`notebooks/lab4.ipynb`](notebooks/lab4.ipynb) | Official lab tasks + supplementary pandas/matplotlib practice on a real dataset | `Data/Market.csv` |
| [`notebooks/practice.ipynb`](notebooks/practice.ipynb) | Standalone pandas & matplotlib drills | Synthetic data only (created in code) |

---

## Repository structure

```
COMP1844-Su26-Tutorial04/
├── README.md
├── LaboratorySession4.pdf
├── Data/
│   └── Market.csv
└── notebooks/
    ├── lab4.ipynb
    └── practice.ipynb
```

---

## Prerequisites

- Python 3.x
- NumPy, pandas, matplotlib
- Completion of Tutorial 03 (basic plotting, histograms, box plots)

---

## Getting Started

1. Clone or download this repository.
2. Open a notebook from the `notebooks/` folder in Jupyter Notebook, JupyterLab, or VS Code.
3. Run the **Setup** cell (imports) at the top of each notebook.
4. Read each markdown section, then write your code in the empty cells below it.
5. For `lab4.ipynb`, load the dataset using the path **`../Data/Market.csv`** (relative to the `notebooks/` folder).

Suggested order: complete **`notebooks/lab4.ipynb`** first, then **`notebooks/practice.ipynb`**.

---

## `notebooks/lab4.ipynb` — Laboratory Session 4

Follows [*LaboratorySession4.pdf*](LaboratorySession4.pdf). Uses the California housing sample in `Data/Market.csv`.

### Part A — Core lab tasks

| Task | Topic |
|------|-------|
| **1** | Load and inspect `Market.csv` |
| **2** | Data cleaning — missing values, duplicates, wrong formats and values |
| **3** | Descriptive statistics for `median_house_value` (mean, median, range) |
| **4** | Extract a NumPy array; compare line, box, and bar charts; justify the best chart type |

### Part B — Additional practice (same dataset)

Uses the cleaned DataFrame from Task 2 (`df_clean`).

| Task | Topic |
|------|-------|
| **5** | pandas Series with custom index |
| **6** | Multi-panel dashboard with `plt.subplots` (2×2) |
| **7** | Nested layout with `fig.subfigures` |
| **8** | `groupby` aggregation table and grouped bar chart |
| **9** | Filtering (`boolean indexing`, `query`) and sorting |
| **10** | Export / reload CSV with `try/except` |

---

## `notebooks/practice.ipynb` — Supplementary workbook

Fifteen exercises to practise pandas and matplotlib **from synthetic data** — no external files, no overlap with the lab dataset.

### Part 1 — Pandas (Exercises 1–8)

| Exercise | Topic |
|----------|-------|
| **1** | Build a DataFrame (≥ 30 rows) |
| **2** | Derived column and `describe()` |
| **3** | Boolean indexing |
| **4** | Sorting, `nlargest`, `nsmallest` |
| **5** | `groupby` — single aggregation |
| **6** | `groupby` — multiple aggregations |
| **7** | Binning with `pd.cut` |
| **8** | pandas Series with custom index |

### Part 2 — Matplotlib (Exercises 9–15)

| Exercise | Topic |
|----------|-------|
| **9** | Side-by-side subplots (`1 × 2`) |
| **10** | Horizontal bar chart from a groupby result |
| **11** | Grouped bar chart (mean vs median) |
| **12** | `2 × 2` dashboard |
| **13** | Scatter plot with colour and size encoding |
| **14** | Nested layout with `fig.subfigures` |
| **15** | Capstone — one report figure (≥ 3 chart types) + written explanation |

---

## Dataset

**`Data/Market.csv`** — teaching sample of the California housing dataset (~28 rows). The full dataset is available on [Kaggle](https://www.kaggle.com/).

Columns include `longitude`, `latitude`, `housing_median_age`, `total_rooms`, `population`, `median_income`, `median_house_value`, and `ocean_proximity`.

The teaching file contains intentional data-quality issues for Task 2 (duplicates, missing values, inconsistent labels, wrong numeric formats). Inspect the data before cleaning — do not assume it is ready to use.

When working from `notebooks/lab4.ipynb`, read and write CSV files under `Data/` using paths relative to the notebook, e.g. `../Data/Market.csv` and `../Data/Market_clean.csv`.

---

## How this session relates to Tutorial 03

| Tutorial 03 | Tutorial 04 |
|-------------|-------------|
| Data-project pipeline and EDA | Data preprocessing and pandas structures |
| Univariate visualisation on a health dataset | Cleaning, aggregation, multi-panel figures |
| Read and understand data | Series, DataFrames, `groupby`, `subplots`, `subfigures` |

---

## References

- [pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Matplotlib — subplots](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.subplots.html)
- [Matplotlib — subfigures](https://matplotlib.org/stable/gallery/subplots_axes_and_figures/subfigures.html)

---

## License

This lab session is part of the COMP1844 module at the University of Greenwich.
