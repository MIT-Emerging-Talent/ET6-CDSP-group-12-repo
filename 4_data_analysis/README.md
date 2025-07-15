# 📊 Crypto Adoption & Migration Analysis

> **Conclusion:**  
> Regions with larger migrant populations often show stronger
cryptocurrency adoption activity — especially in top-ranked countries.
However, the relationship weakens when including Central & Western Europe.  
>**Confidence Level:**
> Moderate – supported by cleaned regional-level data and visual + statistical validation.

---

## 🧠 Summary of Analytical Approach

This project analyzes the relationship between **cryptocurrency adoption**
and **international migrant stock** by:

- Cleaning and aligning data from **Chainalysis** and the **United Nations**
- Creating a **normalized adoption score** from country rankings
- Aggregating by **region** and filtering top-performing countries
- Visualizing adoption vs. migration trends
- Performing **correlation analysis**

---

## 📁 Datasets Used

### 1. Global Crypto Adoption Index (2022–2024)

- **Source**: Chainalysis
- **File**: `../1_datasets/cleaned/GCAI.xlsx`
- **Description**: Ranks 150 countries annually based on crypto activity
 in centralized exchanges, DeFi platforms, and retail usage.
- **Columns Used**: `Rank`, `Country`, `Region`, `Year`

### 2. International Migrant Stock (2024)

- **Source**: UN DESA, Population Division
- **File**: `../1_datasets/cleaned/Migrant_Stock.xlsx`
- **Description**: Total number of migrants per region in 2024.
- **Columns Used**: `Region`, `2024 Migrant Stock`

---

## 🔎 Research Highlights

- **Crypto adoption** varies significantly by region, with strong
performance in parts of **Sub-Saharan Africa**, **South and Southeast Asia**,
and **Latin America**.
- **Migrant stock** is highly concentrated in regions like **North America**
and **Europe**.
- After normalizing adoption scores and aggregating by region, we explored the
strength of the relationship using correlation analysis:

  > 📈 **Pearson correlation (all regions):** 0.136  
  > 📊 **p-value:** 0.748  
  > 🔍 **Interpretation:** Weak or no correlation  
  > 📈 **Pearson correlation (excluding Central & Western Europe):** 0.647  
  > 📊 **p-value:** 0.116  
  > 🔍 **Interpretation:** Moderate positive correlation

These findings suggest that **Central & Western Europe may act as an outlier**,
due to unique socio-economic or regulatory characteristics.

---

## ⚠️ Limitations

- Manual standardization of region names may introduce mapping bias
- Crypto adoption is rank-based, not volume-based
- Migrant data is only for 2024, while adoption spans 3 years
- Some regions (e.g., North America) include very few countries

---

## 💡 Future Research Ideas

- Use raw on-chain volume instead of rank-based metrics
- Include more detailed demographic info (e.g., income, gender)
- Analyze crypto adoption by **remittance corridor**
- Add **qualitative data** on crypto policy or accessibility

---

## 🧪 Dependencies

This notebook uses the following Python libraries:

```bash
pandas
matplotlib
seaborn
openpyxl
scipy
