# Data for Episode 4: flower gift sales

**File:** `flower_gifts_sales_raw.csv` (28,842 rows, 8 columns, about 2.6 MB)
SHA-256: `a61d9b2314dbe048d595ab484ee92113ac9b1db9268e5fd380264a9c3618933f`

**Source:** "Online Retail" by Daqing Chen, UCI Machine Learning Repository (2015).
https://archive.ics.uci.edu/dataset/352/online+retail · DOI: 10.24432/C5BW33

**License:** Creative Commons Attribution 4.0 International (CC BY 4.0), https://creativecommons.org/licenses/by/4.0/

**Changes I made:** I kept only the rows whose Description contains FLOWER, ROSE, VASE, GARDEN or PLANT, and saved them as CSV. No values were changed, and the messy parts (missing CustomerID, duplicates, cancelled orders) are left in on purpose for the cleaning lesson.

**Load it (no login needed):**
```python
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/isajafari1989/Data-Science-With-Isa/ep4-data-v1/data/flower_gifts_sales_raw.csv")
```
