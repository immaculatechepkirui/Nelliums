# Unravelling Africa's Sovereign Debt Crisis — Submission Package

Project: Unravelling Africa’s sovereign debt crisis — path to sustainability  
Author / Team: Immaculate Chepkirui  
Sheet used: https://docs.google.com/spreadsheets/d/1nScTr3a0GXHtcBAQIHTXpJAqKLSvpr2K/edit?gid=151745

Overview
- A reproducible Jupyter Notebook workflow that:
  - Loads the public Google Sheet CSV export.
  - Cleans and coerces types (dates, numeric).
  - Auto-maps fiscal and macro columns (debt, GDP, expenditure, trade, inflation, unemployment, population, etc.).
  - Engineers policy-relevant indicators (debt-to-GDP, trade balance, sector expenditure shares).
  - Provides exploratory plots and correlation analysis.
  - Implements a deterministic debt-to-GDP projection model for scenario analysis.

Reproducible baseline projection (exact numbers used in the submission)
- Baseline assumptions used for the projection included in the deliverables:
  - Initial (latest) debt-to-GDP (start): 70.0% (0.70)
  - Real GDP growth (annual): 3.0% (0.03)
  - Real interest rate (annual): 5.0% (0.05)
  - Primary balance: -1.0% of GDP (primary deficit = -0.01)
  - Horizon: 10 years

- Result from the baseline projection (deterministic debt identity):
  - Start period 1 debt-to-GDP: 70.00%
  - End of year 10 debt-to-GDP (final year): 95.76%

Key deliverables (included)
- `Unravelling_Africa_Sovereign_Debt.ipynb` — reproducible Jupyter Notebook (step-by-step).
- `PRESENTATION_SLIDES.md` — slide content (text for each slide).
- `PRESENTATION_SCRIPT.txt` — speaker script with timing.
- `SUBMISSION_SUMMARY.md` — concise executive summary, findings and recommendations.
- `CHECKLIST.md` — rubric mapping and submission checklist.

How to reproduce the projection
1. In your notebook, set the projection inputs (cells provided in the notebook):
   - initial_b = 0.70 (or use the latest df_work['debt_to_gdp'] if present)
   - n_years = 10
   - growth = 0.03
   - interest = 0.05
   - primary_balance = -0.01
2. Run the projection cell (the notebook includes the function and prints the projection table).
3. The resulting CSV is saved automatically to `output/debt_projection_example.csv`.

Notes & transparency
- The 70.0% initial debt ratio was the starting value used in your projection run (this came from your notebook run).
- The projection is deterministic and aggregate: it assumes homogeneous debt composition, constant real interest and growth rates, and a constant primary balance across the horizon. These simplifications are documented in the summary and the notebook and can be extended in next steps.

