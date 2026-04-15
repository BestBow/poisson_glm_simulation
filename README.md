Poisson GLM: Likelihoods, Simulation & Visualization

**Author:** Satvik Gahlot  
**Main artifact:** `poisson_glm_analysis` (Jupyter notebook)

## What this project does

The notebook is a self-contained statistics / data-science exercise on **Poisson regression** as a generalized linear model (GLM). It walks through:

1. **Simulation** — Draw covariates and Poisson counts from a model with known intercept and slope.
2. **Estimation** — Fit a Poisson GLM with a log link using **statsmodels** and compare estimates to the true parameters.
3. **Likelihood intuition** — Plot the profile **log-likelihood** for the slope and relate the peak to the MLE.
4. **Model comparison** — Fit a null (intercept-only) model and run a **likelihood ratio test** against the full model.
5. **Visualization** — Combined figure: fitted mean curve with a confidence band, plus the profile log-likelihood.
6. **Concepts** — Short markdown discussion of why the **log-likelihood** is used (numerical stability, sums vs. products).
7. **Bonus** — Residual-style diagnostics, overdispersion checks, and a **2D log-likelihood heatmap** over \((\beta_0, \beta_1)\).

Exported figures (written when you run the notebook) include names like `q1_simulated_data.png`, `q3_loglik_curve.png`, `q5_combined.png`, and related bonus outputs.

## Requirements

Install Python 3.9+ and:

- `numpy`
- `pandas`
- `matplotlib`
- `statsmodels`
- `scipy`

Example:

```bash
pip install numpy pandas matplotlib statsmodels scipy
```

## How to run

From the directory that contains the notebook:

```bash
jupyter notebook poisson_glm_analysis.ipynb
```

Or open the file in **VS Code**, **Cursor**, or **JupyterLab** and run all cells top to bottom. The notebook sets a fixed random seed for reproducibility.

## Note on code style

Code cells have been cleaned so they contain **no `#` comments**; explanatory text lives in **markdown** cells. Logic is unchanged, but formatting may follow Python’s default `ast.unparse` style (e.g. some strings use single quotes).

## Project layout

| File | Role |
|------|------|
| `poisson_glm_analysis.ipynb` | Full analysis, questions, and figures |
| `README.md` | This file |

Optional PNG outputs appear next to the notebook after a full run.
