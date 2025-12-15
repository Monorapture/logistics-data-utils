# 🧰 Python Analyst Toolkit

A collection of reusable Python modules and helper functions to automate daily data analysis tasks.
Built to follow the **DRY Principle** (Don't Repeat Yourself).

## 📂 Modules

| Module | Description |
| :--- | :--- |
| `excel_tools.py` | Smart saving of DataFrames with **auto-adjusted column widths** (Autofit). |
| `db_utils.py` | (Planned) Wrapper for SQLite connections and common SQL queries. |
| `logistics_math.py` | (Planned) Standard formulas for Safety Stock, EOQ, and Lead Time calculation. |

## 🚀 How to use

Simply copy the desired module (e.g., `excel_tools.py`) into your project folder and import it.

### Example: Auto-Formatting Excel Files
Instead of writing 20 lines of formatting code every time, use this one-liner:

```python
import pandas as pd
import excel_tools  # Import this library

# 1. Create Data
df = pd.DataFrame({'Product': ['Switch 16A', 'Cable 50m'], 'Stock': [50, 200]})

# 2. Save nicely formatted
excel_tools.save_excel_auto_width(df, "reports/my_report.xlsx")
