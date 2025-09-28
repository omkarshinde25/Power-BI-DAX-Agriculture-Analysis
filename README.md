# Power BI Project: Agriculture Data Analysis (DAX and Data Modeling)

## Project Overview
This project focuses on analyzing agricultural datasets using Power BI and DAX.  
The dashboard provides insights into crop production, revenue, fertilizer sales, and pricing trends.  
It demonstrates the power of data modeling, measures, and KPIs to make agricultural data easy to understand.

## Contents
- Power BI Dashboard (DAX Agriculture.pbix)
- DAX Measures for key KPIs
- Dashboard Screenshots (Insights and KPIs)
- Relationship schema used in the model

## Key Insights and DAX Measures

Q1. Total Production (Tonnes)  
Formula: Total Production Tone = SUM(CropProduction[Production_Tonnes])  
Result: 778.26K  

Q2. Total Revenue for Crops  
Formula: Total Revenue Crop = SUMX(CropProduction,CropProduction[Area_Hectares]*CropProduction[Price_Per_Tonne])   
Result: 5.88bn  

Q3. Average Price Per Tonne (Fertilizers)  
Formula: Average Price_Per_Tone = AVERAGE(CropProduction[Price_Per_Tonne])   
Result: 15.47K  

Q4. Average Revenue per Equipment Item  
Formula: Average Revenue For Equiplment = AVERAGEX(EquipmentSales,EquipmentSales[Revenue]/EquipmentSales[Units_Sold])  
Result: 1.06M  

Q5. Fertilizer Sales Transactions  
Formula: fertilizer sales = COUNT(FertilizerSales[Sales_Revenue])   
Result: 120  

Q6. Number of Crop Records  
Formula: Number of Crop Record = COUNTROWS(CropProduction )  
Result: 150  

Q7. Unique Crop Types  
Formula: Unique Crop = DISTINCTCOUNT(CropProduction[CropName])  
Result: 10  

Q8. Minimum Price Per Tonne (Crops)  
Formula: Min Price_Per_Tone = MIN(CropProduction[Price_Per_Tonne])  
Result: 1.27K  

Q9. Maximum Equipment Revenue  
Formula: Max Revenue = MAX(EquipmentSales[Revenue])   
Result: 1.87bn 

Q10. Variance between Total Fertilizer Sales Revenue and Average Revenue  
Formula: Variance between total sales and average = SUM(FertilizerSales[Sales_Revenue])-AVERAGE(FertilizerSales[Sales_Revenue]) 
Result: 4.09bn

## Dashboard Preview
### Q1 to Q4
<img src="https://github.com/omkarshinde25/Power-BI-DAX-Agriculture-Analysis/blob/main/Pictures/Screenshot%202025-09-28%20194530.png" width="800"> <br>

### Q5 to Q8
<img src="https://github.com/omkarshinde25/Power-BI-DAX-Agriculture-Analysis/blob/main/Pictures/Screenshot%202025-09-28%20093159.png" width="800"> <br>

### Q9 to Q10
<img src="https://github.com/omkarshinde25/Power-BI-DAX-Agriculture-Analysis/blob/main/Pictures/Screenshot%202025-09-28%20093224.png" width="800"> <br>


## Tools and Technologies
- Power BI Desktop  
- DAX (Data Analysis Expressions)
- Measured DAX
- Excel (Raw Data Sources)  

## How to Use
1. Clone or download this repository.  
2. Open the file Agriculture.pbix in Power BI Desktop.  
3. Explore:
   - KPI Cards
   - DAX Measures
   - CropProduction, FertilizerSales, EquipmentSales Analysis
   - Pricing Insights  
4. Modify the dataset to test with your own agricultural data.

## Learning Outcomes
- Hands-on practice with DAX measures  
- Building KPI dashboards  
- Understanding agriculture data trends  
- Applying data modeling principles in Power BI  
