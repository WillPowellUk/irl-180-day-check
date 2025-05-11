
# 🇬🇧 365-Day Residency Compliance Checker

This script verifies whether, in **any rolling 365-day period**, you've spent:

- ✅ **At least 180 days in the UK** (i.e. *not abroad*).
- ⚠️ **No more than 150 days abroad**, otherwise a **warning** is raised.

It also provides:
- 📊 Summary statistics on your travel.
- 📈 A line graph showing "Days at Home" across all 365-day periods.

---

## 📁 Input

Travel data is currently hardcoded as a list of tuples:

```python
data = [
    ("2024-05-18", "2024-06-04"),
    ("2024-07-20", "2024-09-18"),
    ...
]
```

Each entry represents a period **spent abroad**, and the script will calculate all relevant metrics and checks from these dates.

---

## ✅ Features

- **Compliance Check**: Confirms 180+ home days in all 365-day windows.
- **Warning Flag**: Detects windows with 150+ days abroad.
- **Statistics**:
  - Total periods abroad
  - Total days abroad
  - Max and average trip duration
- **Visualization**:
  - Matplotlib graph showing home-day count for every rolling 365-day window.

---

## 🖥️ Usage

1. Make sure you have **Python 3.7+** installed.
2. Install the required library:

```bash
pip install pandas matplotlib
```

3. Run the script:

```bash
python residency_checker.py
```

---

## 📊 Output

### Console
Displays:
- Any **violations**
- Any **warnings**
- Summary travel statistics

### Graph
Visualizes:
- "Days at home" in each 365-day period
- Red dashed line at 180 days (legal minimum)
- Orange dotted line at 215 days (150 days abroad threshold)
