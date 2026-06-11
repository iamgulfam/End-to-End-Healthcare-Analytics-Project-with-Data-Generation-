# End-to-End-Healthcare-Analytics-Project-with-Data-Generation
# 🏥 Healthcare Analytics End-to-End Project (Python + Power BI)

This repository contains a complete **Healthcare Analytics Project**, built using:

- **Python** (Faker-based realistic synthetic data generator)
- **Power BI** (Interactive Dashboards)
- **Star Schema Data Model**
- **Realistic hospital-like metrics**

This project simulates a real hospital environment covering **patients, doctors, appointments, surgeries, attendance, slots, and departments** with 10 years of historical data.

---

## 🚀 Project Features

### ✔ **Synthetic Healthcare Dataset (10 Years)**
Generated using Python (Faker + Random) with realistic distributions:
- Doctors (Specializations, experience, departments)
- Patients (Demographics, chronic conditions, insurance)
- Appointments (Status, duration, revenue)
- Operations (Type, outcome, cost)
- Doctor Attendance Logs
- Slot Scheduling System

### ✔ **Data Model (Star Schema)**


---

## 📊 Dashboards Built in Power BI

### 1️⃣ **Patient Analytics Dashboard**
- Total Patients  
- Total Appointments  
- Avg Patient Age  
- Chronic Condition Distribution  
- Gender & Insurance Segmentation  
- City-level Insights  

### 2️⃣ **Operations & Surgery Dashboard**
- Total Surgeries  
- Success Rate  
- Surgery Costs  
- Surgeries by Type  
- Outcomes Distribution  

### 3️⃣ **Operational Efficiency Dashboard**
- Slot Utilization %  
- Total Slots vs Booked Slots  
- Attendance vs Absenteeism  
- Emergency vs Normal Consultations  

---

## 🛠 Tools Used

| Component | Tool |
|----------|------|
| Data Generation | Python, Faker |
| Data Storage | CSV Files |
| BI Modeling | Power BI Desktop |
| Visualization | Power BI Reports |
| Version Control | GitHub |

---

## 📁 Repository Structure

This script generates:
- Doctor Dimension  
- Patient Dimension  
- Department Dimension  
- Slots Dimension  
- Appointments Fact  
- Operations Fact  
- Attendance Fact  

Each CSV is exported into the `/data/` folder.

---

## 📈 Power BI Components

### Data Model Includes:
- Relationship mapping  
- Cleaned date table  
- DAX measures for insights  

### Dashboards:
- Patient Analytics  
- Surgery & Operations  
- Slot Utilization & Doctor Attendance  

The `.pbix` file is stored in:


---

## 📄 Documentation

Located in the `/docs/` folder:

- `project_overview.pdf` → End-to-end explanation  
- `data_dictionary.md` → Table descriptions, fields, data types  

---

## 🤝 How to Use This Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/healthcare-analytics-powerbi-project.git


---

# 📄 **BONUS: Data Dictionary (Put inside /docs/data_dictionary.md)**

```markdown
# 📘 Data Dictionary

## Dim_Patients
| Column | Description |
|--------|-------------|
| patient_id | Unique patient identifier |
| patient_name | Full name |
| gender | Male/Female |
| age | Age |
| blood_group | A+/O-/AB+ etc |
| city | Location |
| chronic_condition | Diabetes/BP/Asthma/None |
| insurance_type | Private/Government/Self Pay |

---

## Dim_Doctors
| Column | Description |
|--------|-------------|
| doctor_id | Unique doctor ID |
| doctor_name | Name |
| specialization | Cardiology/Oncology etc |
| department_id | FK to department |
| experience_years | Total experience |

---

## Fact_Appointments
| Column | Description |
|--------|-------------|
| appointment_id | Unique appointment |
| patient_id | FK to Dim_Patients |
| doctor_id | FK to Dim_Doctors |
| slot_id | FK to Dim_Slots |
| appointment_date | Date of appointment |
| appointment_status | Completed/Cancelled/No Show |
| revenue | Consultation fee |

---

## Fact_Operations
| Column | Description |
|--------|-------------|
| operation_id | Unique surgery |
| patient_id | FK |
| doctor_id | FK |
| department_id | FK |
| cost | Surgery cost |
| outcome | Success/Complication/ICU Needed |

---

## Fact_Attendance
| Column | Description |
|--------|-------------|
| doctor_id | FK |
| attendance_date | Date |
| is_present | 1/0 |

---
