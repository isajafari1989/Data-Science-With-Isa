# Data Science with Isa 📊

Hi, I'm **Isa Jafari**. I'm learning data science from the beginning and sharing the whole journey on YouTube, from my first lines of pandas to getting hired.

This repo has the **notebooks from my YouTube series "Hire-Ready Data Science"**. Every notebook is written for beginners like me: one step per cell, with a plain-English explanation above each piece of code.

▶️ **YouTube channel:** [Data Science with Isa](https://www.youtube.com/@DataSciencewithIsa)
📺 **Playlist:** [Hire-Ready Data Science](https://www.youtube.com/playlist?list=PLAGemWA1l92M)

---

## Episodes

| # | Episode | Notebook | Video |
|---|---------|----------|-------|
| 1 | Introduction: my data science hire map | – | [Watch](https://youtu.be/2eGgJeuApaY) |
| 2 | The Only Beginner Stack You Need: Python, Jupyter, pandas & Git | – | [Watch](https://youtu.be/aBTfaj0zsuU) |
| 3 | Your First Real Dataset (Restaurant Bills) | [03-first-dataset.ipynb](03-first-dataset.ipynb) | [Watch](https://youtu.be/NQGmLdpUlMA) |
| 4 | Make Messy Data Feel Manageable (Flower Gift Sales) | [04-messy-data.ipynb](04-messy-data.ipynb) | – |

---

## Episode 3: Your First Real Dataset

**Business question:** Which day brings the restaurant the most revenue?

**What you'll practise:**
- Loading a dataset with `seaborn` and looking at it with `shape`, `head()` and `dtypes`
- Checking data quality: missing values and duplicates
- Making a new column without loops (vectorization)
- `groupby` + `agg`: split, calculate, combine
- A simple bar chart with `matplotlib`

**Result:** Saturday brings in the most revenue ($1,778.40, about 37%), but Sunday has the highest average bill ($21.41).

---

## Episode 4: Make Messy Data Feel Manageable

**Business question:** Which weeks and weekdays bring this shop the most flower-gift revenue?

**Data:** a flower-gift subset of "Online Retail" by Daqing Chen, UCI Machine Learning Repository (2015), CC BY 4.0. See [data/README.md](data/README.md). The notebook loads a pinned copy (tag `ep4-data-v1`), so everyone gets the same numbers, with no login.

**What you'll practise:**
- Inspecting a new dataset: `shape`, `head()`, `dtypes`, `isna().sum()`, `duplicated().sum()`
- Fixing text dates with `pd.to_datetime`
- Deciding drop vs fill for missing values, and saying why
- Removing duplicates and separating cancelled orders (invoices starting with C)
- `.dt.day_name()`, `groupby`, and `resample("W")` for weekly totals
- A simple line chart, and an answer with honest limits

**Result:** Thursday brings the most revenue (£114,916.12, 24.6%), and Sunday the least (8.5%). There are no Saturday sales. The best week ended on 22 May 2011 (£15,113.80).

---

## Free tools

- **[Smart Teleprompter](https://isajafari1989.github.io/Data-Science-With-Isa/teleprompter/)** — a free browser teleprompter. Paste a script, and read it on your phone or laptop (speed, size, mirror, voice-follow, and camera recording). [How it works](teleprompter/README.md).

---

## How to run the notebooks

1. Install Python and Jupyter (Episode 2 shows how).
2. Install the libraries:
   ```
   pip install pandas seaborn matplotlib
   ```
3. Download or clone this repo, open the notebook in Jupyter, and run the cells from top to bottom.

Episode 3 needs no data file: seaborn downloads the example dataset for you. Episode 4 loads its data from this repo with one line (internet needed). To match my Episode 4 numbers exactly, use `pip install pandas==3.0.6 matplotlib==3.11.2`.

---

## Learning together

I'm a beginner too, so if you spot a mistake or have a better way to do something, open an issue or leave a comment on the video. I'd love to hear what you found in your own notebook! 🙌
