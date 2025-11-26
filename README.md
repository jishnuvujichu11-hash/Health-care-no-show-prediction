# Health-care-no-show-prediction
Predicting whether a patient will miss their scheduled medical appointment using machine learning, explainability (SHAP), and Power BI analytics.
# Project Overview

Across healthcare systems, approximately 1 in 4 scheduled appointments turn into a No-Show. This results in:
Financial losses for hospitals and doctors due to unused appointment slots
Delayed treatment for other patients who could have taken those slots
Goal of this project:
To analyze patient appointment behavior and predict the probability of a No-Show, so clinics and hospitals can improve overbooking policies, reminders, and resource planning.

# Dataset Description (KaggleV2-May-2016)
This project uses the famous Brazilian Medical Appointment No-Show dataset.

Columns Description
PatientId – Unique patient identifier
AppointmentID – Unique appointment identifier
Gender – Male/Female
ScheduledDay – When the appointment was booked
AppointmentDay – Actual appointment date
Age – Patient age
Neighbourhood – Clinic location
Scholarship – Bolsa Família financial aid
Hypertension – True/False
Diabetes – True/False
Alcoholism – True/False
Handcap – Number of disabilities (0–4)
SMS_received – Number of SMS reminders sent
No-show – Whether the patient missed the appointment

# Machine Learning Workflow
Data Cleaning & Transformation
Converted date formats
Calculated LeadDays (Scheduled → Appointment gap)
Created AgeCategory and LeadDayCategory
Target encoded neighbourhood → Neighbourhood_TE
Added medical risk flag: Old_Chronic
Extracted:
Appointment_Weekday
Scheduled_Weekday
Appointment_Hour
Model Training
Models tested:

Logistic Regression
Random Forest
XGBoost (Best Model)
Final XGBoost Scores

Accuracy: ~0.80
ROC-AUC: ~0.75
Predictions Added to Dataset
NoShow_Prob (probability of missing the appointment)
ShowUp_Prob
Risk_Segment (Low / Medium / High)

# Power BI Dashboard
The dashboard includes:

Total Appointments
Total No-Shows
No-Show Rate (%)
High-Risk %
No-Shows by Weekday
Gender Distribution
Age Category Distribution
Lead Days vs No-Show Rate (line chart)
Risk Segment Donut Chart
