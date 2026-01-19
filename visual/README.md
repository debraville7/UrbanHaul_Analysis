# 🚚 UrbanHaul – Optimizing Rider Performance and Operational Efficiency with Analytics

## 📌 Executive Summary
UrbanHaul is a rapidly scaling last-mile delivery platform operating across major urban markets and multiple delivery categories. As growth accelerated, leadership lacked a centralized, data-driven view of rider performance, operational efficiency, and service quality.

This project delivers a **two-dashboard analytics solution** built in Power BI:
- **Executive / Operations Overview Dashboard** for strategic decision-making
- **Rider Performance Dashboard** for operational management

Together, these dashboards transform raw delivery data into **actionable insights** that support performance optimization, cost control, service consistency, and sustainable growth.

---

## 📚 Table of Contents
1. [Rationale for the Project](#-rationale-for-the-project)
2. [Problem Statement](#-problem-statement)
3. [Business Objectives](#-business-objectives)
4. [Business Questions & KPIs](#-business-questions--kpis)
5. [Analytical Approach](#-analytical-approach)
6. [Data Dictionary](#-data-dictionary)
7. [Data Transformation Process](#-data-transformation-process)
8. [Dashboard 1 – Executive / Operations Overview](#-dashboard-1--executive--operations-overview)
9. [Dashboard 2 – Rider Performance](#-dashboard-2--rider-performance)
10. [Tools & Skills Demonstrated](#-tools--skills-demonstrated)
11. [Final Takeaway](#-final-takeaway)

---

## 🎯 Rationale for the Project
- **Performance optimization at scale:** Visibility into rider productivity, service quality, and workload balance is critical as operations grow.
- **Proactive risk management:** Without analytics, burnout risk and inefficiencies are identified too late.
- **Data-driven decision-making:** KPI-driven insights replace reactive, anecdotal management.

---

## ❗ Problem Statement
UrbanHaul operates a complex, multi-category delivery network with varying urgency levels and route difficulty. Despite rapid expansion, leadership lacks structured insights into:
- Operational efficiency
- Individual rider performance
- Service quality consistency
- Cost-to-serve dynamics

As a result, decisions around rider management, routing, vehicle allocation, and regional scaling remain largely reactive.

This project addresses that gap by delivering a **multi-layered analytics solution** that connects rider-level performance with executive-level operational outcomes.

---

## 🧠 Business Objectives: Analytical Approach

### Dashboard 1: Executive / Operations Overview
**Purpose:** Strategic oversight and resource allocation  
**Focus Areas:**
- Regional efficiency
- Delivery volume by category & priority
- Earnings efficiency
- Customer satisfaction trends

### Dashboard 2: Rider Performance
**Purpose:** Operational monitoring and coaching  
**Focus Areas:**
- Performance by shift and vehicle
- Rating trends over time
- Productivity vs workload balance
- Burnout risk identification

---

## ❓ Business Questions → KPIs

### Dashboard 1: Executive / Operations Overview
**Key Questions**
- Which riders consistently achieve high performance?
- Which regions achieve the highest efficiency and earnings per KM?
- How does delivery volume vary by category and priority?
- Are customer ratings improving or declining?

**KPIs**
- Total Revenue  
- Delivery Volume  
- Average Earnings per KM  
- Average Customer Rating  

---

### Dashboard 2: Rider Performance
**Key Questions**
- How does rider performance vary by shift?
- How does performance differ by vehicle type?
- How do rider ratings trend over time?

**KPIs**
- Overall Rider Rating  
- Customer Rating  
- Earnings per KM  
- Average Deliveries per Day  
- Burnout Risk Flag  

---

## 🗂 Data Dictionary

### Riders
| Column Name | Description |
|------------|------------|
| rider_id | Unique rider identifier |
| rider_name | Rider’s full name |
| rider_type | Employment type (full-time / gig / contract) |
| joined_via_referral | Indicates if rider joined via referral |
| gender | Rider gender |
| age | Rider age |
| region | Rider region |
| profile_image | Link to profile image |

---

### Vehicles
| Column Name | Description |
|------------|------------|
| vehicle_id | Unique vehicle identifier |
| vehicle_type | Mode of transport |
| fuel_type | Fuel type |
| max_load_kg | Maximum cargo capacity |

---

### Delivery_Category
| Column Name | Description |
|------------|------------|
| delivery_category_id | Unique category identifier |
| delivery_category | Type of delivery |
| priority_level | Delivery urgency |

---

### Geography
| Column Name | Description |
|------------|------------|
| geo_id | Unique geographic identifier |
| state | State name |
| city | City name |

---

### Rider_Performance
| Column Name | Description |
|------------|------------|
| entry_id | Unique record identifier |
| rider_id | Links to Riders table |
| vehicle_id | Vehicle used |
| delivery_category_id | Delivery category |
| year_month | Reporting period |
| avg_daily_distance_km | Average daily distance |
| total_monthly_distance_km | Monthly distance |
| avg_deliveries_per_day | Average daily deliveries |
| avg_monthly_earnings_usd | Monthly earnings |
| shift_time | Shift period |
| earnings_satisfaction | Earnings satisfaction rating |
| shift_flexibility | Schedule flexibility rating |
| dispatch_support | Dispatch support rating |
| route_difficulty | Route difficulty score |
| customer_rating | Average customer rating |
| commission | Revenue generated from rider |

---

## 🔄 Data Transformation Process
- Data type standardization
- Duplicate record removal
- Geography normalization (State & City split)
- Text cleansing and standardization
- Invalid and out-of-range value handling

---

## 📊 Key Insights & Recommendations

### 🔹 Insight 1: Rider Performance Is Highly Polarized  
📍 **Chart:** Top vs Poorly Rated Riders  
➡️ [View Chart](./visuals/insight_01_rider_polarization.png)

**Takeaway:** A small group of riders significantly outperforms others, indicating both scalability potential and hidden risk.  
**Action:** Scale best practices from top performers and proactively support low performers.

---

### 🔹 Insight 2: Efficiency ≠ Earnings Across Regions  
📍 **Chart:** Operational Efficiency by Region  
➡️ [View Chart](./visuals/insight_02_efficiency_by_region.png)

**Takeaway:** Some regions convert efficiency into earnings better than others.  
**Action:** Apply region-specific strategies instead of a one-size-fits-all model.

---

### 🔹 Insight 3: Delivery Priority Drives Operational Pressure  
📍 **Chart:** Delivery Volume by Priority  
➡️ [View Chart](./visuals/insight_03_delivery_priority.png)

**Takeaway:** Low-priority deliveries dominate volume, but high-priority orders drive risk.  
**Action:** Segment routing, staffing, and incentives by priority level.

---

### 🔹 Insight 4: Revenue Is Concentrated by Category  
📍 **Chart:** Delivery & Revenue by Category  
➡️ [View Chart](./visuals/insight_04_category_revenue.png)

**Takeaway:** High volume does not always mean high value.  
**Action:** Focus capacity on high-yield categories and reprice or bundle low-yield ones.

---

### 🔹 Insight 5: Customer Ratings Are Volatile  
📍 **Chart:** Customer Rating Trend  
➡️ [View Chart](./visuals/insight_05_customer_rating_trend.png)

**Takeaway:** Service quality is inconsistent throughout the year.  
**Action:** Stabilize operations during historically volatile periods.

---

### 🔹 Insight 6: Shift Performance Is Balanced  
📍 **Chart:** Performance by Shift  
➡️ [View Chart](./visuals/insight_06_performance_by_shift.png)

**Takeaway:** Performance is evenly distributed across shifts, with a slight night-shift edge.  
**Action:** Transfer night-shift efficiencies to daytime operations.

---

### 🔹 Insight 7: Vehicle Type Does Not Drive Rider Experience  
📍 **Chart:** Vehicle Performance  
➡️ [View Chart](./visuals/insight_07_vehicle_performance.png)

**Takeaway:** Rider satisfaction is consistent across vehicles.  
**Action:** Optimize fleet decisions using efficiency and cost, not perception.

---

### 🔹 Insight 8: Rider Performance Is Stable Over Time  
📍 **Chart:** Overall Rider Rating Trend  
➡️ [View Chart](./visuals/insight_08_overall_rating_trend.png)

**Takeaway:** Performance is resilient but experiences short-term volatility.  
**Action:** Proactively manage seasonal dips and institutionalize year-end best practices.

---

## 🧰 Tools & Skills Demonstrated
- Power BI (DAX, Data Modeling, Visualization)
- KPI Design & Interpretation
- Business & Operational Analytics
- Executive Storytelling
- Stakeholder-Ready Recommendations

---

## ✅ Final Takeaway
This analytics solution enables UrbanHaul to move from **reactive management to proactive performance optimization**, aligning rider-level execution with executive-level strategy.


