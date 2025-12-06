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
3. Validated schema and data types using notebooks (bronze, silver, gold)

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

# Bronze notebook
<p align="center">
<img width="1844" height="916" alt="Image" src="https://github.com/user-attachments/assets/4771617e-c7e4-4d69-901a-28a063e9a641" />
</p>


<br>

#  Silver notebook
<p align="center">
<img width="1782" height="878" alt="Image" src="https://github.com/user-attachments/assets/df40ef6e-f1ac-48e0-8a09-ab50454dbe72" />
</p>


</br>

<p align="center">
<img width="1784" height="797" alt="Image" src="https://github.com/user-attachments/assets/61a94543-b32a-4104-a003-ea3583225068" />
</p>

<br>

<p align="center">
<img width="1663" height="856" alt="Image" src="https://github.com/user-attachments/assets/d85e5e01-57aa-43d1-b6ca-f90f121ee792" />
</p>

<br>

<p align="center">
<img width="1676" height="864" alt="image" src="https://github.com/user-attachments/assets/6e82e0a5-29c4-4898-bba8-500a8ae62d09" />
</p>

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

<br> 

<p align="center">
<img width="1732" height="793" alt="Image" src="https://github.com/user-attachments/assets/99c05888-d3c2-45f5-b436-0059bd959565" />
</p>


