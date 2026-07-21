## Healthcare ER Wait Time Analysis ##
The purpose of this project is to use exploratory data analysis to identify meaningful patterns in ER wait times and develop actionable business recommendations.


## EXECUTIVE SUMMARY ##
I used Excel to clean, prepare, and analyze a simulated ER wait-time dataset. I conducted an exploratory analysis guided by several business questions, including which factors were associated with longer ER wait times and when those waits were highest. Critical patients waited an average of 18.4 minutes, compared with 173.5 minutes for low-urgency patients. Longer wait times were associated with several operational factors, including the stage of the ER process, nurse workload, and time of day. The largest delay occurred while waiting to see a medical professional, which accounted for approximately 55% of the average total wait. Evening visits and heavier nurse workloads were also associated with longer waits. All 84 extreme-wait visits involved low-urgency patients, 79.8% occurred in the evening, and 20.2% ended with the patient leaving without being seen. Recommendations include investigating bottlenecks during Monday evenings, reviewing staffing and patient flow during evening shifts, and focusing improvement efforts on the delay between triage and seeing a medical professional. These actions could improve patient flow and satisfaction while helping managers allocate resources more effectively.

## Business Questions
- When are ER Wait times highest?
- Which patient and operational factors are associated with longer waits?
- Which stage of the ER process contributes most to total wait time?
- How are wait times related to patient satisfaction and outcomes?
- What conditions are most common among extreme wait-time visits?

## Dataset Overview

- **Source:** [[Dataset source](https://www.kaggle.com/datasets/rivalytics/er-wait-time?resource=download)]
- **File:** `ER_Wait_Time_Dataset.csv`
- **Records:** 5,000 ER visits
- **Hospitals:** 5
- **Data type:** Simulated healthcare operational data
- **Key fields:** urgency level, time of day, nurse-to-patient ratio, wait stages, patient outcome, and satisfaction

  ## Tools and Skills

- **Tool:** Microsoft Excel
- **Techniques:** Data cleaning, descriptive statistics, PivotTables, PivotCharts, outlier analysis, segmentation, and exploratory data analysis
- **Business skills:** Translating findings into operational recommendations

## Data Cleaning and Preparation

The dataset was reviewed for missing values, duplicate records, duplicate Visit IDs, incorrect data types, invalid ranges, and inconsistent categories. One text-encoding issue in a hospital name was corrected.

Additional preparation included creating helper fields for facility-size groups and extreme wait-time outliers. Facility capacity was grouped into Small, Medium, Large, and Very Large categories to make comparisons more meaningful.
