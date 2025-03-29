# VOC Report Analysis for TVF Board Surveys  

---

### **Dashboard Link**  
https://app.powerbi.com/view?r=eyJrIjoiYTVkZDY2MjktZDdlNy00Y2ZmLWEyMTMtMzAxNDE2OTY4NTIxIiwidCI6IjdiOGQ3YzQzLTZjMzAtNDJkOS04YzI2LTg4NWIxZWRmZDdkZSJ9

---

## **Problem Statement**  
This dashboard analyzes TVF's board and community satisfaction with property management services. Key focus areas include:  
- **Low board member response rates** (0% in FY22-04).  
- **Inconsistent community engagement** (68.68% to 85.71%).  
- **Critical suggestions** for improving timeliness, property visits, and vendor processes.  

---

## **Steps Followed**  

1. **Data Loading**  
   - Imported survey data (CSV/Excel) into Power BI Desktop.  
   - Merged datasets for surveys FY22-02 to FY23-01.  

2. **Data Quality Check**  
   - Validated columns:  
     - `Total Responses`: 466 | `Completed Surveys`: 435 (93.3%).  
     - Handled nulls in `Board Member Response %` and `Community Response %`.  

3. **Data Modeling**  
   - Created relationships between `Survey Name` and `Community Name`.  
   - Built calculated tables for response rate trends.  

4. **DAX Measures**  
   - **Completed Survey %**:  
     ```dax  
     Completed % = DIVIDE([Completed Surveys], [Total Responses])  
     ```  
   - **Satisfaction Score**: Weighted average of satisfaction ratings.  

5. **Visual Design**  
   - **Slicers**: `Survey Name`, `Community`, `Response Type` (Board/Community).  
   - **Stacked Bar Chart**: Completed vs. Incomplete surveys.  
   - **Gauge Visual**: Avg. time to complete surveys (26.27 mins).  
   - **Table with Conditional Formatting**:  
     - Green: Satisfaction ≥70%.  
     - Red: Satisfaction <70%.  
   - **Card Visuals**: Highlighted 0% board response (FY22-04).  
   - **Textbox**: Displayed respondent suggestions.  

---

## **Key Insights**  

### 1. Response Rates  
| Metric                | Value               |  
|-----------------------|---------------------|  
| Total Responses       | 466                 |  
| Completed Surveys     | 435 (93.3%)         |  
| Board Member Response | 0% (FY22-04)        |  
| Community Response    | 68.68% – 85.71%     |  

### 2. Satisfaction Levels  
| Category      | Percentage |  
|---------------|------------|  
| Dissatisfied  | 20%        |  
| Neutral       | 14%        |  
| Satisfied     | 27%        |  

### 3. Top Suggestions from Respondents  
1. **Improve response timeliness** to community inquiries.  
2. **Monthly in-person property visits** (where feasible).  
3. **Obtain 2-3 vendor bids** for service contracts.  

### 4. Community-Specific Trends  
- **Highest Engagement**: The Glover Park (85.71%).  
- **Lowest Engagement**: Butternut Court Condominium (needs follow-up).  

---

## **Recommendations**  
1. **Board Engagement**: Address 0% response rates with targeted outreach.  
2. **Automated Alerts**: Flag overdue inquiries to improve timeliness.  
3. **KPI Dashboard**: Track compliance with monthly property visits.  
4. **Vendor Bid Tracker**: Ensure 2-3 bids are obtained for contracts.  

---

## **Dashboard Snapshot**  
![image alt](https://github.com/priyankfeb/PowerBI-VoC-Report/blob/ed2fe3d85bcc1592e81fb5fe3f5d7e6ba9e1eb4c/image%20(4)%20(1).png)  

---

**Created by**: Priyank Sharma  
**Data Source**: TVF Board Surveys (modified for security).  
**Tools**: Power BI, DAX, Conditional Formatting.  

--- 

**Note**: This report identifies actionable gaps in TVF’s service delivery and provides a roadmap for enhancing stakeholder satisfaction.  
