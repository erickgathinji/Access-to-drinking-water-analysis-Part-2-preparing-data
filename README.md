# 🌍 Access to Drinking Water Analysis – Part 2

## 📘 Overview
This project explores **global access to safe and affordable drinking water**, with a special focus on the **differences between urban and rural service levels**. The analysis supports the United Nations **Sustainable Development Goal 6: "Ensure availability and sustainable management of water and sanitation for all"**.

The dataset, provided by the **WHO/UNICEF Joint Monitoring Programme (JMP)**, covers multiple years (2000–2020). Using **Google Sheets**, I performed data cleaning, transformation, and exploratory analysis to uncover patterns, trends, and inequalities in water service provision.

---

## 📊 Data Description
- **Sources:**
    - Estimates of the use of water (2000-2020).csv
    - Regions.csv 
- **Format:** CSV files imported and processed in Google Sheets  
- **Deliverable:** <a href="https://docs.google.com/spreadsheets/d/12iigZr-Ib51FirMBhE6JaIyrjY7ZEcZtcVlF6AwEbJE/edit?usp=sharing" target="_blank">Final Google Sheets File</a>
- [Final Google Sheets File (opens in new tab)](https://docs.google.com/spreadsheets/d/12iigZr-Ib51FirMBhE6JaIyrjY7ZEcZtcVlF6AwEbJE/edit?usp=sharing)


**Key Features:**
- `name`: Country or area  
- `year`: Observation year  
- `pop_n`: National population (in thousands)  
- `pop_u`: Urban population share (%)  
- **Service Levels** (by national `_n`, rural `_r`, urban `_u`):  
  - `wat_bas`: Basic access  
  - `wat_lim`: Limited access  
  - `wat_unimp`: Unimproved  
  - `wat_sur`: Surface water  

---

## ❓ Problem Statement
The project aims to answer:  
- How evenly is drinking water access distributed across **national, rural, and urban** populations?  
- What are the **annual rates of change (ARC)** in access levels over time?  
- How do **population size, urbanization, and income group** influence water access?  
- Which regions face the **greatest challenges** in achieving universal water access?  

---

## 🛠️ Tools & Methods
- **Google Sheets** – data preparation, analysis, visualization  
- **Data Cleaning:**  
  - Managed missing values (`NaN`, blanks)  
  - Fixed delimiter issues and duplicate entries  
  - Corrected out-of-bounds percentages (>100%)  
- **Key Functions Used:**  
  - Logical: `IF`, `IFS`, `SWITCH`, `AND`, `OR`  
  - Aggregation: `SUMIFS`, `AVERAGE`, `MEDIAN`, `MODE`, `STDEV`, `QUARTILE`  
  - Lookup: `VLOOKUP`, `HLOOKUP`, `LOOKUP`  
  - Text/Regex: `TRIM`, `SPLIT`, `REGEXMATCH`, `REGEXREPLACE`  
  - Error handling: `IFERROR`, `IFNA`  
- **Analysis Techniques:** Pivot Tables, calculated fields, year-over-year ARC formulas  
- **Visualizations:** Line charts, histograms, stacked bar charts, box plots, scatter plots  

---

## 🔍 Key Steps Taken
1. **Data Import & Setup**  
   - Imported datasets into Google Sheets  
   - Resolved formatting and delimiter inconsistencies  
   - Verified row/column integrity using `COUNTA()`  

2. **Population Analysis**  
   - Compared dataset totals to global estimates (e.g., 2020 ≈ 7.82B people, 55% urban)  
   - Calculated rural population share = `100 – pop_u`  
   - Standardized units (`pop_n` → millions) for clearer visualization  

3. **Service Level Analysis**  
   - Validated and rounded percentage values (ensuring ≤100%)  
   - Computed ARC for basic services at national, rural, and urban levels  
   - Measured spread and central tendencies for access features  

4. **Regional & Income Group Analysis**  
   - Merged supplementary `Regions.csv` to enable regional comparisons  
   - Grouped data by **income categories** using pivot tables  
   - Explored links between GNI, urbanization, and service levels  

5. **Comparative Visualizations**  
   - 100% stacked columns for access composition  
   - Box plots for spread of access levels  
   - Scatter plots showing ARC vs. population size  

---

## 📈 Insights & Findings
- **Regional Gaps:** Sub-Saharan Africa lags behind, with current projections suggesting full basic access only by ~2080.  
- **Urban Advantage:** Urban areas generally record **higher and faster growth** in access than rural ones.  
- **Income Correlation:** Higher-income countries show stronger urbanization and better access, while low-income countries report higher reliance on limited and surface water sources.  
- **Population Impact:** Despite alignment with global population totals, disparities remain across regions and income groups.  

---

## ⚠️ Challenges & Lessons Learned
- Handling **delimiter inconsistencies** and cleaning malformed CSV rows  
- Managing **missing data, outliers, and percentages over 100%**  
- Learning the importance of **absolute vs. relative cell references** for multi-row calculations  
- Gaining experience with **error handling (`IFERROR`)** and advanced lookup functions  
- Reinforcing the role of **data governance** (validation, access control, version history) in maintaining integrity  

---

## 📊 Visuals
Key charts created in Google Sheets include:  
- Line charts → Population vs. urban/rural shares  
- Box plots → Spread of access across service levels  
- Stacked column charts → Composition of access by area  
- Income group summary → Income categories vs. access trends  

---

## 💡 Reflection
This project reinforced my ability to handle **real-world, messy data** in Google Sheets — from import and cleaning to analysis and visualization. Beyond technical skills, it emphasized the importance of **responsible data use**, ensuring insights support actionable progress toward **global water equity**.  

---

