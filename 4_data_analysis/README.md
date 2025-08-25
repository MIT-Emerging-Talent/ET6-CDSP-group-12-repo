# Crypto Adoption & Migration Analysis

- **Conclusion:**  

> Our findings suggest that regions with **higher international migrant populations**
often show **stronger engagement with cryptocurrency tools**, especially among the
top 50 countries. While correlation is not definitive across all regions, excluding
statistical outliers like Central & Western Europe reveals a
**moderate positive relationship** between migrant stock and crypto adoption.

- **Relation to Research Question:**  

> These insights support the hypothesis that
**blockchain-based financial tools could serve as a viable alternative to traditional credit systems** — especially in regions underserved by formal
financial infrastructure. Migrants in such regions may be more likely to adopt
decentralized platforms that don't require traditional credit histories, pointing
to blockchain's **potential for fostering financial inclusion**.  

- **Confidence Level:**  

> Moderate — supported by cleaned regional-level data and cross-validation through
visual and statistical analysis. Results may vary depending on data granularity
and region definitions.

---

## Summary of Analytical Approach

This analysis investigates whether **blockchain-based solutions** — reflected in global crypto adoption — can **financially include migrant populations** where traditional credit systems fall short.

Steps:

- Cleaned and standardized datasets from **Chainalysis (crypto adoption)** and the **UN (migrant stock)**
- Normalized adoption rankings into 0–1 scores
- Grouped countries by **region and year** (2022–2024)
- Linked crypto adoption to **migrant stock levels**
- Visualized regional trends
- Conducted correlation analysis to evaluate statistical relationships

---

## Datasets Used

### 1. Global Crypto Adoption Index (2022–2024)

- **Source**: Chainalysis
- **File**: `../1_datasets/cleaned/GCAI.xlsx`
- **Description**: Ranks 150 countries annually based on crypto
activity in centralized exchanges, DeFi platforms, and retail usage.
- **Used Fields**: `Rank`, `Country`, `Region`, `Year`

### 2. International Migrant Stock (2024)

- **Source**: UN DESA, Population Division
- **File**: `../1_datasets/cleaned/Migrant_Stock.xlsx`
- **Description**: Aggregated count of international migrants in 2024,
grouped by region.
- **Used Fields**: `Region`, `2024 Migrant Stock`

---

## Research Highlights

- **Crypto adoption** is higher in regions with stronger grassroots digital
finance, such as:
  - Sub-Saharan Africa
  - Central & Southern Asia
  - Latin America

- **Migrant populations** are most concentrated in:
  - Northern America
  - Western Europe
  - Southern Asia

- After region alignment and normalization, we performed Pearson correlation:

  - 📈 **Correlation (all regions):** 0.136  
    📊 **p-value:** 0.748  
    🔍 **Interpretation:** Weak or no correlation

  - 📈 **Correlation (excluding Central & Western Europe):** 0.647  
    📊 **p-value:** 0.116  
    🔍 **Interpretation:** Moderate positive correlation

  Excluding Central & Western Europe — which has high migration but moderate
  adoption — reveals a clearer relationship between migration levels and crypto
  adoption.

---

## Limitations

- **Region labels** were standardized manually and may introduce minor bias
- **Crypto adoption rankings** are ordinal, not volume-based
- **Migrant data** is from 2024 only; no time-series alignment
- **Small sample size** per region (especially North America) may skew trends

---

## Future Research Ideas

- Replace rankings with **on-chain volume or wallet address count**
- Investigate **remittance corridors** using transaction-level blockchain data
- Incorporate **policy environment scores** or **mobile internet access** per region
- Explore **case studies** (e.g., El Salvador) where adoption is policy-driven

---

## Dependencies

The following Python libraries were used:

```bash
pandas
matplotlib
seaborn
openpyxl
scipy
