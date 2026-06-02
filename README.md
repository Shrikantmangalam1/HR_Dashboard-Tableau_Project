# 📊 HR Analytics Dashboard — Tableau

An interactive HR analytics project built in Tableau, analyzing **8,950 employee records** across hiring trends, attrition, workforce demographics, compensation, and performance. The project features two polished dashboards and 17 worksheets that allow HR teams to explore the data at both a summary and individual employee level.

---

## 🗂️ Project Structure

```
hr-tableau-dashboard/
├── MY_Hr_Tableau_project.twbx   # Tableau packaged workbook (data embedded)
├── README.md
└── images/                      # Dashboard screenshots
```

---

## 📌 Dashboards

### 1. HR Summary
A high-level command center view of the entire workforce. It answers questions like: How many people are currently employed? How has hiring grown over time? Which departments have the most employees? What is the gender and education split? It pulls together KPI tiles, trend charts, and demographic breakdowns into a single view designed for leadership and HR managers.

![HR Summary Dashboard](https://raw.github.com/Shrikantmangalam1/HR_Dashboard-Tableau_Project/main/Project_screenshots/HR_dashboard_Overview.png)

### 2. HR Details
A detailed, filterable employee-level view. Users can drill down by department, job title, location, education, or performance rating to explore individual records. This view is useful for day-to-day HR operations, spotting patterns in specific teams, or reviewing employee profiles in context.

![HR Details Dashboard](https://raw.github.com/Shrikantmangalam1/HR_Dashboard-Tableau_Project/main/Project_screenshots/HR_Dashboard_Detail.png)

---

## 📋 Worksheets (17 Sheets)

| Sheet | Description |
|---|---|
| Active | Count of currently active employees (7,984 out of 8,950) |
| Hired | Total employees ever hired across all years |
| Terminated | Total employees who have left the organization |
| Hired Over Year | Year-by-year hiring trend from 2015 to 2024 |
| Terminated Over Year | Year-by-year attrition trend |
| Gender | Male vs Female headcount distribution |
| Departments | Employee count broken down by department |
| Location | Geographic map showing employee spread across US states |
| Stated | State-level employee count breakdown |
| Age and Education | Cross-analysis of age groups and education levels |
| Age vs Salary | Scatter/trend view of how salary relates to employee age |
| Age wise Hiring | Which age groups were hired most over time |
| Education Levels | Distribution of High School, Bachelor, Master, and PhD holders |
| Education vs Performance | How education level correlates with performance ratings |
| Gender Vs Education Level | Gender breakdown within each education category |
| Detailed Info | Full filterable employee table with all fields |
| Test | Development/testing sheet |

---

## 🗃️ Dataset

**File:** `Data/hr-dashboard-project/dataset.csv`  
**Records:** 8,950 employees  
**Delimiter:** Semicolon (`;`)  
**Source:** Simulated HR dataset for analytics and dashboard practice

### Fields

| Field | Type | Description |
|---|---|---|
| Employee_ID | String | Unique employee identifier |
| First Name | String | Employee first name |
| Last Name | String | Employee last name |
| Gender | String | Male / Female |
| State | String | US state of employment |
| City | String | City of employment |
| Education Level | String | High School / Bachelor / Master / PhD |
| Birthdate | Date | Date of birth (DD/MM/YYYY) |
| Hiredate | Date | Date of joining (DD/MM/YYYY) |
| Termdate | Date | Date of termination — blank if still active |
| Department | String | Department name |
| Job Title | String | Employee's job title (28 unique roles) |
| Salary | Integer | Annual salary in USD |
| Performance Rating | String | Excellent / Good / Satisfactory / Needs Improvement |

---

## 📊 Data Analysis & Key Insights

### 👥 Workforce Overview

| Metric | Value |
|---|---|
| Total Employees | 8,950 |
| Currently Active | 7,984 (89.2%) |
| Terminated | 966 (10.8%) |
| Average Employee Age | 39.5 years |
| Average Salary | $70,964 |
| Salary Range | $51,835 – $149,377 |

The workforce is predominantly active with an overall attrition rate of **10.8%**. The average age of 39.5 years suggests a mid-career dominant workforce, with hiring spanning from young graduates to experienced professionals.

---

### 🏢 Department Breakdown

| Department | Employees | Avg Salary | Attrition Rate | Excellent Performers |
|---|---|---|---|---|
| Operations | 2,718 | $65,400 | 10.6% | 15.0% |
| Sales | 1,835 | $76,205 | 11.0% | 23.7% |
| Customer Service | 1,673 | $65,838 | 11.0% | 13.6% |
| IT | 1,382 | $81,926 | 10.1% | 18.9% |
| Marketing | 718 | $67,659 | 9.7% | 15.0% |
| Finance | 452 | $76,451 | 13.9% | 21.2% |
| HR | 172 | $64,145 | 11.6% | 17.4% |

**Key observations:**
- **IT** pays the highest average salary ($81,926) and has the lowest attrition rate (10.1%), suggesting strong retention.
- **Finance** has the highest attrition rate (13.9%) despite above-average salaries — a potential area of concern.
- **Sales** stands out with the highest proportion of Excellent performers (23.7%), indicating strong motivation or a performance-driven culture.
- **HR** is the smallest department (172 employees) with the lowest average pay ($64,145).

---

### ⚧️ Gender Distribution

| Gender | Count | % of Workforce | Avg Salary | Attrition Rate |
|---|---|---|---|---|
| Male | 4,801 | 53.6% | $72,531 | 10.6% |
| Female | 4,149 | 46.4% | $69,151 | 11.0% |

The gender split is fairly balanced (54% Male / 46% Female). There is a **salary gap of ~$3,380** between male and female employees on average, which may warrant a deeper pay equity analysis. Attrition rates are nearly identical across genders.

---

### 🎓 Education Level Analysis

| Education | Employees | % | Avg Salary | Excellent % |
|---|---|---|---|---|
| Bachelor | 5,416 | 60.5% | $69,922 | 12.3% |
| High School | 1,819 | 20.3% | $62,144 | 12.9% |
| Master | 1,237 | 13.8% | $82,676 | 35.4% |
| PhD | 478 | 5.3% | $86,033 | 47.7% |

**Key observations:**
- A **clear salary progression** exists with higher education — PhD holders earn ~38% more than High School graduates.
- **PhD and Master holders** perform significantly better, with 47.7% and 35.4% receiving Excellent ratings respectively, compared to ~12-13% for Bachelor and High School employees.
- The majority of the workforce (60.5%) holds a Bachelor's degree.

---

### ⭐ Performance Rating Distribution

| Rating | Count | % |
|---|---|---|
| Good | 3,763 | 42.1% |
| Satisfactory | 2,498 | 27.9% |
| Excellent | 1,566 | 17.5% |
| Needs Improvement | 1,123 | 12.5% |

The performance distribution is **positively skewed** — 59.6% of employees are rated Good or Excellent. However, 12.5% fall into the Needs Improvement category, which is worth monitoring from a talent management perspective.

---

### 📅 Hiring Trends (2015–2024)

| Year | Hires |
|---|---|
| 2015 | 472 |
| 2016 | 729 |
| 2017 | 1,560 ⬆ Peak |
| 2018 | 850 |
| 2019 | 902 |
| 2020 | 968 |
| 2021 | 422 ⬇ Dip |
| 2022 | 1,042 |
| 2023 | 1,201 |
| 2024 | 804 |

Hiring peaked sharply in **2017 (1,560 hires)** before normalizing. A notable dip occurred in **2021 (422 hires)**, likely reflecting pandemic-era hiring freezes. Recovery is evident in 2022–2023 with hiring back above 1,000.

---

### 📍 Geographic Distribution

| State | Employees |
|---|---|
| New York | 6,270 (70.1%) |
| Michigan | 976 (10.9%) |
| Pennsylvania | 435 (4.9%) |
| North Carolina | 430 (4.8%) |
| Illinois | 285 (3.2%) |
| Ohio | 271 (3.0%) |
| Virginia | 180 (2.0%) |
| West Virginia | 103 (1.2%) |

The workforce is heavily concentrated in **New York (70%)**, making it the primary operating hub. The remaining employees are spread across 7 other US states.

---

### ⏳ Attrition Insights

- Overall attrition rate: **10.8%**
- Average tenure before termination: **1.9 years**
- Highest attrition department: **Finance (13.9%)**
- Lowest attrition department: **Marketing (9.7%)**

The short average tenure of 1.9 years among terminated employees suggests that early-stage retention (first 1–2 years) is a key challenge worth addressing through onboarding improvements and engagement initiatives.

---

## 🚀 How to Open

1. Download and install [Tableau Public](https://public.tableau.com/) (free) or Tableau Desktop
2. Clone or download this repository
3. Open `MY_Hr_Tableau_project.twbx` in Tableau
4. The dataset is fully embedded — no separate data connection needed

---

## 🛠️ Tools Used

- **Tableau 2026.1.2** — data visualization and interactive dashboard design
- **CSV** — raw semicolon-delimited data source with 8,950 records

---

## 👤 Author

Made by [Shrikant Mangalam]  
[Linkedin Profile](www.linkedin.com/in/shrikant-mangalam-75148126a)
