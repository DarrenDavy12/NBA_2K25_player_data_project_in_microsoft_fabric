# 🏀 NBA 2K25 Player Data — Microsoft Fabric End-to-End Data Engineering Project

This project demonstrates a complete data engineering workflow using **Microsoft Fabric**, based on the **NBA 2K25 Player Dataset** from Kaggle.  
It showcases:

- Lakehouse ingestion  
- Warehouse SQL transformation  
- Data cleaning  
- Star schema modeling  
- Fabric pipelines  
- Power BI analytics dashboard  
- Version-controlled documentation  

This is a clean, job-ready MVP project suitable for data engineering & analytics roles.

---

## 🏗️ 1. Architecture Overview

**Tools Used**
- Microsoft Fabric (Lakehouse, Warehouse, Data Factory Pipelines)
- SQL (T-SQL)
- Power BI (Direct Lake / SQL Endpoint)
- OneLake Storage
- GitHub for version control


**Pipeline Summary**
Raw CSV → Lakehouse → Warehouse Cleaning → Star Schema → Power BI Dashboard


---

## 📊 2. Dataset Description — NBA 2K25

**Dataset:** NBA 2K25 Player Ratings  
**Source:** Kaggle  
**File Used:** `current_nba_players.csv`  
**Rows:** ~500–600  
**Columns:** Player ratings, attributes, demographics, badges, team data, etc.

### Key Features Included:
- Player Name  
- Team  
- Age  
- Height  
- Weight  
- Position  
- Overall Rating  
- Potential Rating  
- Salary  
- Playmaking, Shooting, Defense, Rebounding, Athleticism attributes  

<br>

  <img width="803" height="211" alt="Image" src="https://github.com/user-attachments/assets/c80e60b4-cad5-47d4-8d27-30e2eded53f5" />


---

## 🏞️ 3. Lakehouse Ingestion

1. Created a **Fabric Lakehouse**  
2. Uploaded `current_nba_players.csv` into `/Files`  
3. Validated schema and data types 

<br>

<p align="center">
<img width="1741" height="416" alt="Image" src="https://github.com/user-attachments/assets/c9266354-c30a-4123-b225-cc96a68fd3de" />
</p>

<br>

<p align="center">
  <img width="1752" height="407" alt="Image" src="https://github.com/user-attachments/assets/6647bc52-ed1d-480a-bc21-3eef94da17cf" />
</p>

<br>

<p align="center">
<img width="1500" height="843" alt="Image" src="https://github.com/user-attachments/assets/a524f25e-c087-4d84-b0e9-95f0f6702320" />
</p>

<br>

---

## 🧹 4. Warehouse SQL — Data Cleaning & Preparation

Created a **Fabric Warehouse** to clean the dataset and prepare it for modelling.

### Cleaning Tasks Performed
- Converted salary & numeric fields to correct types  
- Removed nulls or replaced with defaults  
- Fixed team/position inconsistencies  
- Standardized height & weight formatting  
- Ensured numeric ratings were valid (0–99)  
- Generated PlayerID surrogate key  

### Example SQL Snippets

**Convert salary to numeric**
```sql
UPDATE players
SET salary = REPLACE(salary, '$', '');
