# Excel Bike Buyer Analysis Dashboard

## Project Overview
This project involves analyzing bike buyer demographics to create an interactive Excel dashboard. The dataset was cleaned, transformed, and visualized using pivot tables/charts, with dynamic filters (slicers) for exploratory analysis.

**Key Highlights**:
- 🧹 Data cleaning & deduplication
- 📊 3 interactive visualizations
- ⚙️ Dynamic filters (marital status/region/education)
- 📈 Age bracket analysis using nested `IF` logic
- 🎨 Professional dashboard layout

## Features
### Data Cleaning  
Removed duplicates & standardized categorical values (e.g., "M" → "Male").
  
### Pivot Analytics  
- Average income comparison (bike buyers vs non-buyers by gender)
- Commute distance distribution analysis
- Age bracket purchase trends

### Interactive Dashboard  
- Slicers for marital status, region, and education
- Responsive design with aligned visualizations
- Custom color schemes & gridline-free layout

## Dataset Overview
| Column            | Description                          |
|-------------------|--------------------------------------|
| ID                | Unique customer identifier          |
| Marital Status    | Married/Single                      |
| Gender            | Male/Female                         |
| Income            | Annual income                       |
| Children          | Number of children                  |
| Education         | Education level                     |
| Occupation        | Job category                        |
| Home Owner        | Yes/No                              |
| Cars              | Number of cars owned                |
| Commute Distance  | Work commute range                  |
| Region            | Geographic region                   |
| Age               | Customer age                        |
| Purchased Bike    | Yes/No purchase indicator           |

## Steps to Reproduce
### 1. Data Cleaning  
- Remove duplicates (`Data → Remove Duplicates`)
- Standardize values using Find/Replace (`Ctrl+H`):
  - M → Married, S → Single
  - M → Male, F → Female

### 2. Age Brackets (Nested IF)  
```excel
=IF(L2<=30, "Adolescent (0-30)", 
 IF(L2<=54, "Middle-Aged (31-54)", 
 "Old (55+)"))
```

### 3. Pivot Tables  
#### Average Income Analysis:
- **Rows:** Gender
- **Columns:** Purchased Bike
- **Values:** Average Income

#### Commute Distance:
- **Rows:** Commute Distance
- **Columns:** Purchased Bike
- **Values:** Count

#### Age Brackets:
- **Rows:** Age Brackets
- **Columns:** Purchased Bike
- **Values:** Count

## Visualizations
- **Clustered Column Chart** (Income)
- **Stacked Bar Chart** (Commute Distance)
- **Line Chart** (Age Brackets)

## Dashboard Setup
1. Create a new sheet, remove gridlines
2. Add header: **"Bike Sales Dashboard"**
3. Arrange charts with consistent spacing
4. Format charts with coordinated colors

### Slicers
- Insert slicers for **Marital Status, Region, Education**
- Connect to all pivot tables:
  - `Slicer → Report Connections → Select all pivot tables`

## Screenshots
-  Final interactive dashboard
![image](https://github.com/user-attachments/assets/fc7c9b22-5c05-48cc-a5cb-4a634af6472e)
- **Data-Cleaning.png** - Before/after data standardization
- **Pivot-Settings.png** - Example pivot table configuration

## Tools Used
- Microsoft Excel
- PivotTables & PivotCharts
- Slicers
- Data Cleaning Tools
- Conditional Formatting
- Nested IF Statements

## Conclusion
This project demonstrates core Excel skills including data transformation, analytical visualization, and dashboard creation. The interactive elements allow users to explore how different demographic factors correlate with bike purchases.

### Enhancement Ideas:
- Add calculated fields (e.g., income brackets)
- Incorporate VBA for automated updates
- Create **"Export to PDF"** button
- Add trendlines to visualizations

## Download Dataset
