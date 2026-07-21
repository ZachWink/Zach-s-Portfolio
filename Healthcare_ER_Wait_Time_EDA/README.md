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

## Methodology

The analysis followed the steps below:

1. Cleaned and validated the dataset.
2. Calculated descriptive statistics for total ER wait time.
3. Examined the distribution of total wait times.
4. Identified extreme wait-time visits using the interquartile range method.
5. Compared average and median wait times across patient and operational categories.
6. Investigated major time-based bottlenecks, including evenings and Mondays.
7. Examined the stages of the ER process to determine where the largest delays occurred.
8. Analyzed patient outcomes and satisfaction in relation to wait time.
9. Investigated the common conditions among extreme wait-time visits.
10. Developed recommendations based on the strongest patterns found in the data.

---

## Key Findings

### 1. Patient urgency was strongly associated with wait time

Critical patients waited an average of 18.4 minutes, while low-urgency patients waited an average of 173.5 minutes.

This pattern suggests that the hospitals were prioritizing patients based on urgency. Although this is expected in an ER setting, low-urgency patients experienced substantially longer waits and may require additional patient-flow strategies.

### 2. Evenings were the strongest time-based bottleneck

Evening visits had both the highest visit volume and the highest average wait time.

- **Evening visit volume:** 1,725 visits
- **Average evening wait:** Approximately 100 minutes
- **Median evening wait:** 74 minutes

Evening visits also had the highest average wait time within every urgency category, showing that the evening bottleneck remained even after accounting for patient urgency.

### 3. Higher nurse workloads were associated with longer waits

Average wait time increased substantially as the nurse-to-patient ratio increased.

- **Ratio of 1:** 16.1-minute average wait
- **Ratio of 5:** 172.1-minute average wait

This was one of the strongest relationships found in the dataset. However, the analysis identifies an association and does not prove that nurse workload directly caused the longer waits.

### 4. The largest delay occurred before seeing a medical professional

The average ER visit included:

- **Registration:** 11.7 minutes
- **Triage:** 24.8 minutes
- **Waiting to see a medical professional:** 45.4 minutes
- **Total wait:** 81.9 minutes

The wait to see a medical professional accounted for approximately 55% of the average total wait time. This suggests that improvement efforts should focus on patient flow and provider availability after triage.

### 5. Longer waits were associated with lower satisfaction and patients leaving

Patients who left without being seen had the longest average wait time of approximately 179 minutes.

Patient satisfaction also declined sharply as wait time increased:

- **Satisfaction level 5:** 14.8-minute average wait
- **Satisfaction level 1:** 167.5-minute average wait

These results suggest that reducing excessive wait times could improve patient experience and reduce the number of patients who leave before receiving care.

### 6. Extreme wait-time visits followed a clear pattern

A total of 84 visits had wait times above the outlier threshold of 263 minutes.

Among these visits:

- **100%** involved low-urgency patients
- **79.8%** occurred in the evening
- **46.4%** occurred on a Monday
- **79.8%** resulted in discharge
- **20.2%** ended with the patient leaving without being seen

These outliers were concentrated among low-urgency patients visiting during periods of high operational pressure.

---

## Additional Findings

Several factors showed little or no meaningful relationship with wait time:

- Average wait times were highly consistent across the five hospitals.
- Median wait times were also similar across hospitals.
- Urban and rural hospitals had nearly identical average wait times.
- Facility-size groups showed little difference in average wait time.
- Specialist availability did not show a clear linear relationship with wait time.
- Monday had the highest average wait time, but its urgency mix was similar to other days.
- Winter had the longest seasonal waits, although the dataset did not include enough information to determine the exact cause.

These findings are important because they show that some expected relationships were not supported by the dataset.

---

## Visualizations

### ER Wait Time Analysis Report

![ER Wait Time Analysis Report]([Images/1_er_wait_time_analysis_report.png](https://github.com/ZachWink/Zach-s-Portfolio/blob/9b3d2b40766230310f590fd29e48e79c69c733f4/Healthcare_ER_Wait_Time_EDA/Images/1_ER_Wait_Time_Analysis_Report.png))

This report summarizes the main findings, business impact, recommendations, and limitations of the analysis.

### EDA Findings

![EDA Findings](Images/eda_findings.png)

This section presents the major comparisons across urgency level, time of day, nurse workload, patient outcome, satisfaction, and other operational categories.

### Total Wait Time Analysis

![Total Wait Time Analysis](Images/total_wait_time_summary.png)

The wait-time distribution was strongly right-skewed. The median wait of 60 minutes was lower than the average of 81.9 minutes because a smaller number of extremely long visits increased the average.

---

## Business Impact

The findings identify the periods, patient groups, and stages of the ER process experiencing the greatest operational pressure.

Reducing excessive waits may help the hospitals:

- Improve patient satisfaction
- Reduce the number of patients leaving without being seen
- Improve patient flow after triage
- Allocate staff and providers more effectively
- Focus resources on the busiest shifts
- Identify low-urgency patients at risk of experiencing extreme delays

The analysis also helps managers avoid making broad changes across the entire ER process when the largest delay appears to occur specifically before patients see a medical professional.

---

## Recommendations

### Investigate evening and Monday-evening bottlenecks

Evenings had the highest volume and longest average wait time, while Monday evenings represented one of the strongest operational bottlenecks.

Hospital managers should compare evening demand with staffing levels, provider coverage, room availability, and patient-flow procedures.

### Review staffing and patient flow during high-demand periods

Higher nurse-to-patient ratios were strongly associated with longer waits.

Managers should review whether staffing schedules match demand during evenings and other high-pressure periods. Additional staffing data would be required before determining whether staffing changes are necessary.

### Focus improvement efforts on the post-triage stage

Waiting to see a medical professional represented the largest share of total wait time.

Process-improvement efforts should focus on the period after triage rather than treating every stage of the ER process as equally responsible.

### Develop a strategy for low-urgency patients

All extreme wait-time visits involved low-urgency patients.

The hospitals could investigate options such as fast-track care, separate treatment pathways, improved wait-time communication, or reassessment procedures for low-urgency patients.

### Monitor patients at risk of leaving without being seen

Patients who left without being seen experienced the longest average waits.

Hospitals should monitor long-wait patients and consider additional communication or reassessment procedures before they decide to leave.

### Track satisfaction alongside operational performance

Satisfaction declined sharply as wait times increased.

Wait time and patient satisfaction should be monitored together to evaluate whether operational improvements also improve the patient experience.

---

## Limitations

This analysis identifies patterns and associations but does not establish direct causation.

The dataset does not include several variables that could help explain the findings, including:

- Detailed nurse and provider schedules
- Provider availability by shift
- Staff absences
- Room occupancy
- Room turnover time
- Inpatient bed availability
- Patient diagnoses
- Treatment complexity
- Treatment duration
- Employee workload or burnout
- External events affecting patient demand

Because the dataset is simulated, the findings should be interpreted as an analytical exercise rather than conclusions about a specific healthcare organization.

---

## Next Steps

With additional data, the analysis could be expanded by:

- Comparing hourly patient arrivals with scheduled staffing
- Examining provider coverage by shift
- Measuring treatment duration and room turnover
- Investigating diagnosis and treatment complexity
- Studying seasonal illness patterns
- Tracking changes in patients' urgency while they wait
- Building an interactive Excel or Power BI dashboard
- Developing a model to estimate or predict ER wait times
- Monitoring patients at risk of leaving without being seen

---

## Repository Structure

```text
Healthcare_ER_Wait_Time_EDA/
│
├── Data/
│   └── ER_Wait_Time_Dataset.xlsx
│
├── Excel/
│   └── Healthcare_ER_Wait_Time_EDA.xlsx
│
├── Images/
│   ├── er_wait_time_analysis_report.png
│   ├── eda_findings.png
│   └── total_wait_time_summary.png
│
└── README.md
