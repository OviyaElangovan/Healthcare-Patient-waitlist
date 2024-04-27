# Healthcare-Patient-waitlist
## Goal
•	Track the current status of the patient waiting list
•	Analyse the historical monthly trend of waiting list Inpatient & Outpatient categories
•	Detailed specialty level & age profile analysis
# Metrics Required
•	Average & Median Waiting list
•	Current Total Waitlist
# Views Required
•	Summary Page
•	Detailed Page for Granular analysis
# DAX 
- Latest Month Wait List = CALCULATE(SUM(All_Data[Total]),All_Data[Archive_Date] = MAX(All_Data[Archive_Date])) + 0
- PY Latest Month Wait List = CALCULATE(SUM(All_Data[Total]), All_Data[Archive_Date] = EDATE(MAX(All_Data[Archive_Date]),-12)) + 0
- Average Waiting List = AVERAGE(All_Data[Total])
- Median Waiting List = MEDIAN(All_Data[Total])
- Avg / Med Wait List = SWITCH(VALUES('Calculation Method'[Calc Method]), "Average", [Average Waiting List], "Median", [Median Waiting List])
# Inference
On average, through the years from 2018 to 2021, the percentage of patient wait lists concerning their category
Inpatient - 10.62%
Outpatient - 72.49%
Day Case - 16.89%
Top 5 Specialty_Name concerning Average waiting list
Accident & Emergency
Paediatric Cardiology
Paediatric Orthopaedic
Pediatric Dermatology
Pediatric ENT



