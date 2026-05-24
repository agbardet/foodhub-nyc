# Weekend Execution Plan — FoodHub Portfolio Project

**Dates:** Saturday 24 May + Sunday 25 May 2026  
**Goal:** Complete repo, verify notebook runs clean, push to GitHub, confirm GitHub Pages renders.

---

## Saturday 24 May

### Morning — 09:00–12:00 (3 hrs): Verify & Run

| Time | Task |
|------|------|
| 09:00–09:20 | Open `foodhub-nyc/` in VS Code. Confirm directory structure matches plan. |
| 09:20–09:45 | Create a virtual environment: `python -m venv .venv && pip install -r requirements.txt` |
| 09:45–11:00 | Open `notebooks/foodhub_eda.ipynb` in Jupyter. Run **Kernel → Restart & Run All**. Watch for errors. |
| 11:00–11:30 | Fix any errors that surface (path issues, library version mismatches, chart rendering). |
| 11:30–12:00 | Confirm all 10 figures are saved to `reports/figures/`. Open each one — check title, labels, reference lines. |

**Definition of done:** Notebook runs from top to bottom with zero errors. 10 PNG files exist in `reports/figures/`.

---

### Afternoon — 13:00–16:00 (3 hrs): Polish & Review

| Time | Task |
|------|------|
| 13:00–13:30 | Read `README.md` cold — does the first paragraph communicate business impact without any technical setup? |
| 13:30–14:00 | Read `key_findings.md` — does it read like a consulting brief, not a student report? Tighten any weak paragraphs. |
| 14:00–14:30 | Read notebook markdown cells — are the Act titles and section intros professional? Remove any remaining student-voice phrasing. |
| 14:30–15:00 | Check `data_dictionary.md` and `portfolio_copy.md` — any factual errors vs. notebook output? |
| 15:00–15:30 | Spell-check everything. Search for "Q1", "Q2" etc., "marks", "points", "Write your code here" — none should remain. |
| 15:30–16:00 | Screenshot 2–3 of the best charts. These become the repo social preview and portfolio card images. |

**Definition of done:** All files read cleanly as professional documents. No student artifacts visible.

---

### Evening — 16:00–18:00 (2 hrs): Git Init & First Push

| Time | Task |
|------|------|
| 16:00–16:20 | `cd foodhub-nyc && git init && git add . && git commit -m "Initial portfolio release: FoodHub NYC EDA"` |
| 16:20–16:40 | Create new GitHub repo `foodhub-nyc` (public). Push: `git remote add origin <url> && git push -u origin main` |
| 16:40–17:00 | On GitHub: Settings → Pages → Source: `main` branch, `/` root (or `/docs` if you add a docs/ page later). |
| 17:00–17:30 | Verify GitHub Pages URL loads. Confirm README renders correctly with badges and key findings. |
| 17:30–18:00 | Buffer: fix any rendering issues (broken image paths, badge URLs, etc.). |

**Definition of done:** Public GitHub repo is live. README renders correctly. GitHub Pages URL is accessible.

---

## Sunday 25 May

### Morning — 09:00–11:00 (2 hrs): Portfolio Page & Copy

| Time | Task |
|------|------|
| 09:00–09:30 | Open `portfolio_copy.md`. Copy the resume bullet points — update your LinkedIn and resume. |
| 09:30–10:30 | If you have a portfolio website repo: add the FoodHub project card using the card title, one-liner, three bullets, and tags from `portfolio_copy.md`. Use one of the chart screenshots as the card image. |
| 10:30–11:00 | If using the GitHub Pages stub from `portfolio_copy.md`: copy the HTML into a `docs/index.html`, push, verify it renders. |

**Definition of done:** Project is visible and linkable from your portfolio.

---

### Late Morning — 11:00–13:00 (2 hrs): Final Quality Pass

| Time | Task |
|------|------|
| 11:00–11:30 | Open the GitHub repo as a stranger would. Read README → click notebook link → does the analysis tell a coherent story? |
| 11:30–12:00 | Check that `reports/figures/*.png` files are committed to the repo and render in GitHub's file viewer. |
| 12:00–12:30 | Optional: Export notebook to HTML (`jupyter nbconvert --to html notebooks/foodhub_eda.ipynb`) and add to `docs/` for a richer GitHub Pages experience. |
| 12:30–13:00 | Tag the release: `git tag v1.0 && git push --tags`. Write a one-paragraph LinkedIn post announcing the project. |

**Definition of done:** Project is shareable. You can hand the GitHub URL to a recruiter or hiring manager right now.

---

## Checkpoint Questions (ask yourself before closing the laptop Sunday)

1. Does the repo README lead with business impact, not setup steps?
2. Can a non-technical reader understand the three most important findings from the README alone?
3. Does the notebook run end-to-end without errors in a fresh environment?
4. Are all chart images saved and committed?
5. Is the GitHub Pages URL live and accessible without a login?
6. Is the project linked from your portfolio and/or LinkedIn?

If the answer to all six is yes — ship it.
