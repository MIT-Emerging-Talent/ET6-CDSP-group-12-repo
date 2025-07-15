# 📊 Crypto Adoption & Migration Analysis

This notebook explores the relationship between **cryptocurrency adoption trends** and **international migrant stock** across countries and regions. The goal is to investigate whether migration levels influence the uptake of decentralized financial technologies.

---

## 📁 Datasets Used

### 1. Global Crypto Adoption Index (2022–2024)

- **Source**: Chainalysis
- **Cleaned File**: `../1_datasets/cleaned/GCAI.xlsx`
- **Description**: Ranks 150 countries each year based on crypto activity in centralized exchanges, DeFi platforms, and retail transactions.
- **Columns Used**: `Rank`, `Country`, `Region`, `Year`

### 2. International Migrant Stock (2024)

- **Source**: United Nations DESA, Population Division
- **Cleaned File**: `../1_datasets/cleaned/Migrant_Stock.xlsx`
- **Description**: Provides migrant population counts by region in 2024.
- **Columns Used**: `Region`, `2024 Migrant Stock`

---

## 🎯 Objectives

- 🧼 Clean, merge, and align datasets based on region
- 📈 Normalize adoption ranks into a score out of 1
- 📊 Analyze and visualize regional patterns
- 🔍 Explore the correlation between migrant stock and crypto adoption

---

## 🔎 Analysis Highlights

- Bar and line plots compare **regional adoption scores vs. migrant stock**
- An exploded pie chart shows the **distribution of migrant stock**
- Region-level scatter plots display **country-wise variation**
- Pearson correlation analysis reveals the **relationship strength**

---

## 🧪 Dependencies

The following Python libraries are used:

```bash
pandas
matplotlib
seaborn
openpyxl
scipy
