# PED Utilization and Availability Analysis

This project analyzes **utilization, availability, and downtime recovery** data for the months of **February** and **March**, using raw data consolidated from multiple sources.

## 📂 Data Source

The file `PED_Feb_March_Utilization_Availability_Downtime_recover.xlsx` contains:

- Multiple sheets representing different data sources
- Raw logs of equipment performance, shift data, operating, available, downtime

---

## 🏗️ Major Equipment Filter - SCIC-PED

For this analysis, only **Major Equipment** under the SCIC-PED category were considered. These include:

- CARGO TRUCK W/ CRANE  
- HYDRAULIC EXCAVATOR  
- HYDRAULIC EXCAVATOR (MINI)  
- HYDRAULIC EXCAVATOR (LONG ARM)  
- HYDRAULIC EXCAVATOR WHEEL TYPE  
- CRAWLER TRACTOR  
- ROUGH TERRAIN CRANE  
- ARTICULATED DUMP TRUCK  
- VIBRATORY ROLLER  
- JUMBO DRILL  
- LOAD HAUL DUMPER  
- LOW PROFILE TRUCK  
- COMMANDO DRILL  
- GROUTING MACHINE  

Only records matching these equipment names were used for summary, comparison, and visualization.

---

## 🔄 Process Overview

### 1. Data Consolidation

- Imported and cleaned data from multiple sheets.
- Standardized column headers .
- Merged datasets using common keys:
  - `Date`
  - `Equipment`
  - `Shift`
  - `Operating`
  - `Available`
  - `Downtime`

### 2. Data Querying

Filtered data for:

- Specific months (February and March)
- Major Equipment Only (as listed above)

Added calculated metrics:

```text
Utilization Rate% = Operating / Shift
Availability Rate% = Available / Shift
Downtime Rate% = Downtime / Shift
