
# 🇬🇧 365-Day UK 180 Day  Indefinite Leave to Remain Compliance Checker

This script verifies whether, in **any rolling 365-day period**, you've spent:

- ✅ **At least 180 days in the UK** (i.e. *not abroad*).
- ⚠️ **No more than 150 days abroad**, otherwise a **warning** is raised.

It also provides:
- 📊 Summary statistics on your travel.
- 📈 A line graph showing "Days in UK" across all 365-day periods.

---

## 🖥️ Usage

1. Make sure you have **Python 3.7+** installed.
2. Open the [irl_180_day_check.ipynb](Notebook).
3. Write in your travel data as a list of tuples:

```python
data = [
    ("2024-05-18", "2024-06-04"),
    ("2024-07-20", "2024-09-18"),
    ...
]
```

Each entry represents a period **spent abroad**, and the script will calculate all relevant metrics and checks from these dates. 

4. Run the notebook script.

## ✅ Features

- **Compliance Check**: Confirms 180+ UK days in all 365-day windows.
- **Warning Flag**: Detects windows with 150+ days abroad.
- **Statistics**:
  - Total periods abroad
  - Total days abroad
  - Max and average trip duration
- **Visualization**:
  - Matplotlib graph showing UK-day count for every rolling 365-day window.

---

## 📊 Output

### Console
Displays:
- Any **violations**
- Any **warnings**
- Summary travel statistics

### Graph
Visualizes:
- "Days in UK" in each 365-day period
- Red dashed line at 180 days (legal minimum)
- Orange dotted line at 215 days (150 days abroad threshold)
