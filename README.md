# Codtech-task-4
# 🚚 CodTech Task 4 - Supply Chain Optimization using Linear Programming

## 📌 Problem Statement
A company wants to **minimize total shipping costs** by deciding how many units of various SKUs (Stock Keeping Units) to ship from multiple suppliers, considering supply limits and cost per route.

---

## 📊 Dataset

- **File Name**: `supply_chain_data.csv`
- **Source**: Public GitHub Repository
- **Contains**:
  - Product type
  - SKU
  - Shipping costs
  - Supplier name
  - Location

📥 [Download Dataset](https://raw.githubusercontent.com/SAI-ADITY-A/Supply-chain-analysis/main/supply_chain_data.csv)

---

## ⚙️ Optimization Goal

**Objective**:  
Minimize total shipping cost while ensuring no more than 100 units are shipped per SKU.

**Constraints**:
- Total units shipped for each SKU ≤ 100
- Only available supplier routes considered

---

## 🧠 Techniques Used

- Linear Programming (LP)
- Python with PuLP and Pandas

---

## 📂 Files Included

| File | Description |
|------|-------------|
| `supply_chain_data.csv` | Dataset used for optimization |
| `optimization_model.ipynb` | Google Colab notebook with full code |
| `README.md` | Project documentation |

---

## 💻 Code Summary

```python
from pulp import LpProblem, LpMinimize, LpVariable, lpSum
import pandas as pd

# Load dataset
df = pd.read_csv('supply_chain_data.csv')

# Define LP mod
