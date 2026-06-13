# CLAUDE.md — Student Dropout EDA Assistant

## Project Context
This is a Data Science 2026 group project using the UCI Student Dropout and Academic Success dataset.

**Project Question:** How can an institution identify students who may need support early enough to improve student outcomes?

**Dataset:** UCI ML Repository ID 697
- Fetched via: `from ucimlrepo import fetch_ucirepo; dataset = fetch_ucirepo(id=697)`
- Target variable: `Target` with 3 classes — `Dropout`, `Enrolled`, `Graduate`
- ~4400 rows, 36 features (demographic, academic, socioeconomic)

**Stack:** Python, Jupyter Notebook, pandas, numpy, matplotlib, seaborn, scikit-learn

---

## My Goals Right Now
I am working on the **EDA (Exploratory Data Analysis)** phase. Help me:
1. Understand the shape, types, and quality of the data
2. Explore the target variable distribution
3. Identify which features are most associated with dropout vs graduation
4. Spot any data quality issues (missing values, outliers, skewed distributions)
5. Produce clean, well-labelled visualisations I can reuse in my presentation

---

## Code Style Preferences
- Use `pandas`, `matplotlib`, and `seaborn` — no plotly unless I ask
- Save every plot with `plt.savefig('filename.png', dpi=150, bbox_inches='tight')`
- Use `sns.set_theme(style='whitegrid', palette='Set2')` for consistent styling
- Add a markdown cell above each code cell explaining what it does and why
- Use comments inside code cells for anything non-obvious
- Keep cells focused — one idea per cell
- Variable names should be descriptive (e.g. `dropout_rate_by_course` not `x`)

---

## Dataset Notes
- Most features are encoded as integers (e.g. marital status, nationality) — refer to the UCI data dictionary for what each value means
- Key academic features to prioritise:
  - `Curricular units 1st sem (grade)` and `2nd sem (grade)`
  - `Curricular units 1st sem (approved)` and `2nd sem (approved)`
  - `Admission grade`
  - `Age at enrollment`
- Key socioeconomic features:
  - `Scholarship holder`
  - `Tuition fees up to date`
  - `Debtor`
  - `GDP`, `Unemployment rate`, `Inflation rate`

---

## What I Want From You
- When I ask for a plot, write the full cell including title, axis labels, and savefig
- When I ask a question about the data, suggest the right pandas or seaborn approach and explain it briefly
- If you notice something interesting in the data (e.g. class imbalance, a skewed feature), point it out proactively
- Keep explanations concise — I understand Python, just guide me on the analysis choices
- If I ask you to "explore X", give me 2–3 cells: summary stats, a visualisation, and a 2-sentence interpretation

---

## Project Files
- `student_dropout_project.ipynb` — main notebook
- `CLAUDE.md` — this file

---

## Do Not
- Do not use plotly or bokeh
- Do not run model building code yet — EDA only for now
- Do not use inline `print` statements where a `df.head()` or `.describe()` display is cleaner
