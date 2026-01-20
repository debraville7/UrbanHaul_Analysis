# 🚚 UrbanHaul – Optimizing Rider Performance and Operational Efficiency with Analytics

## 👇 Dashboard

➡️ [OPERATIONAL OVERVIEW DASHBOARD](./visual/URBANHAUL-POWER%20BI-%20DASHBOARD.png)

➡️ [RIDER PERFORMANCE DASHBOARD](./visual/RIDER%20PERFORMANCE%20DASHBOARD.png)

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

## 🧠 Business Objectives

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
➡️ [View Chart](./visual/TOP%20%26%20POORLY%20RATED%20RIDERS.png)

**Observation**
- Top riders score between 7.3 and 9.4, with Abigail Nelson standing out at 9.4
- Poorly rated riders cluster between 3.2 and 4.5, well below acceptable performance thresholds
- The rating gap between the highest and lowest performers exceeds 6 points, indicating extreme performance dispersion

**Insight**
 UrbanHaul’s rider network is not operating at a consistent performance level. While top riders demonstrate that excellent service quality and efficiency are achievable, the presence of very low-rated riders signals hidden operational risks such as service inconsistency, customer dissatisfaction, and potential burnout or disengagement.
 
**Recommendation**
 Adopt a dual strategy: scale best practices from top performers while immediately diagnosing and supporting low-performing riders through targeted coaching, workload adjustments, and operational fixes rather than punitive action.

---

### 🔹 Insight 2: Efficiency ≠ Earnings Across Regions  
📍 **Chart:** Operational Efficiency by Region  
➡️ [View Chart](./visual/OPERATIONAL%20EFFICIENCY%20BY%20REGION.png)

**Observation**
- California has the highest operational efficiency score (1.9) and the highest earnings per KM ($0.92)
- Illinois follows closely with strong efficiency (1.8) and solid earnings ($0.85)
- Florida and Texas show moderate efficiency (1.7) but noticeably lower earnings per KM ($0.81 and $0.79)
- New York stands out with the lowest operational efficiency (1.0) despite relatively comparable earnings per KM ($0.82)

**Insight**
 Operational efficiency alone does not fully explain earnings performance. Some regions convert efficiency into revenue more effectively than others, while certain high-cost or high-complexity markets (e.g., New York) generate reasonable earnings despite poor efficiency—likely at the expense of higher operational strain.
 
**Recommendation**
*Segment regional strategy into two tracks:*
- Scale efficiency-driven profitability in regions like California and Illinois
- Diagnose cost and complexity drivers in regions like New York where earnings persist despite low efficiency

---

### 🔹 Insight 3: Delivery Priority Drives Operational Pressure  
📍 **Chart:** Delivery Volume by Priority  
➡️ [View Chart](./visual/DELIVERY%20BY%20PRIORITY.png)

**Observation**
- Low-priority deliveries account for 61.4% (7,878 deliveries)
- High-priority deliveries represent 35.6% (4,563 deliveries)
- Medium-priority deliveries are minimal at 3.0% (390 deliveries)
- Delivery demand is heavily skewed toward low urgency, but high-priority orders still form over one-third of total volume

**Insight**
 UrbanHaul’s operations are sustained by high-volume, low-urgency work, but a significant portion of demand requires rapid fulfillment and higher service reliability. This creates a dual operating model where efficiency and responsiveness must be balanced carefully to avoid rider overload and service degradation.
 
**Recommendation**
 Segment operational planning by delivery priority—optimize efficiency for low-priority volume while protecting service quality and rider capacity for high-priority deliveries through targeted staffing, routing, and incentives.

---

### 🔹 Insight 4: Revenue Is Concentrated by Category  
📍 **Chart:** Delivery & Revenue by Category  
➡️ [View Chart](./visual/DELIVERY%20%26%20REVENUE%20BY%20CATEGORY.png)

**Observation**
- Bulk/Wholesale leads both in volume (5,446 deliveries) and revenue ($141,717)
- Medical (3,439 deliveries, $96,874) and Parcel (2,169 deliveries, $61,916) are strong secondary revenue drivers
- Pharmacy has moderate volume (787) but relatively strong revenue ($23,468)
- Categories like Retail Goods, Fragile Items, Electronics, Grocery, and Food show low volume and disproportionately low revenue contribution

**Insight**
 UrbanHaul’s revenue is highly concentrated in a few categories, but revenue efficiency per delivery differs significantly. Some categories generate strong returns per delivery, while others consume operational capacity with limited financial upside.
 
**Recommendation**
- Double down on Bulk/Wholesale, Medical, and Parcel categories for growth
- Introduce category-based pricing adjustments for low-yield segments
- Bundle low-revenue categories with higher-value routes to improve efficiency

---

### 🔹 Insight 5: Customer Ratings Are Volatile  
📍 **Chart:** Customer Rating Trend  
➡️ [View Chart](./visual/CUSTOMER%20RATING%20TREND.png)

**Observation**
- Ratings peak early in February (6.3), followed by a sharp drop in March (5.2)
- Mid-year recovery occurs from June to September, reaching 6.0 in September
- Another decline appears in October (5.4) before stabilizing around 5.7 in November and December
- No sustained upward trend is visible across the year

**Insight**
 Customer experience at UrbanHaul lacks consistency. While the organization is capable of delivering high-quality service, variability suggests operational instability—potentially driven by fluctuating rider workload, seasonal demand spikes, or uneven execution across regions and delivery types.
 
**Recommendation**
 Shift focus from peak performance to consistency by identifying and stabilizing the operational drivers behind rating drops, particularly during transition months and high-demand periods.

---

### 🔹 Insight 6: Shift Performance Is Balanced  
📍 **Chart:** Performance by Shift  
➡️ [View Chart](./visual/PERFORMANCE%20BY%20SHIFT.png)

**Observation**
- Night shift has the highest average performance score (6.3) and contributes 33.75% to overall rider rating
- Morning shift follows closely with a 6.2 score and 33.58% contribution
- Afternoon shift records the lowest score (6.0) and slightly lower contribution (32.67%)
- Performance contribution across shifts is nearly evenly split, with less than a 1.1 percentage-point spread

**Insight**
 UrbanHaul’s rider performance is broadly consistent across shifts, indicating that no single shift disproportionately drives overall performance. However, the small but persistent edge seen in night shifts suggests operational conditions at night are marginally more favorable.

**Recommendation**
 Maintain balanced resource allocation across shifts while selectively transferring night-shift efficiencies to daytime operations to lift overall performance without increasing workload pressure.

---

### 🔹 Insight 7: Vehicle Type Does Not Drive Rider Experience  
📍 **Chart:** Vehicle Performance  
➡️ [View Chart](./visual/VEHICLE%20PERFORMANCE%20BY%20OVERALL%20RATING.png)

**Observation**
- Cars and motorcycles handle the highest delivery volumes (3.5K and 3.4K)
- Bikes and vans manage slightly fewer deliveries (3.0K and 2.9K)
- Overall rider ratings are nearly identical across vehicles
Car: 6.2
Motorcycle: 6.2
Bike: 6.2
Van: 6.1
Rating variance across vehicles is minimal (0.1 difference)

**Insight**
 Vehicle type does not materially affect rider satisfaction or perceived performance. Differences in delivery volume are therefore driven by operational deployment and route assignment rather than rider experience.

**Recommendation**
 Evaluate vehicle performance primarily through efficiency and cost lenses rather than rider rating, while maintaining consistent rider experience standards across the fleet.

---

### 🔹 Insight 8: Rider Performance Is Stable Over Time  
📍 **Chart:** Overall Rider Rating Trend  
➡️ [View Chart](./visual/OVERALL%20RIDER%20RATING%20TREND.png)
**Observation**
- Ratings start at 5.9 in January, peak at 6.4 in February, then drop back to 5.9 in March
- Mid-year ratings stabilize between 6.0 and 6.3 from April through July
- A noticeable dip occurs in August (6.1) and October (6.1)
- Ratings recover and trend upward in November (6.2), reaching a year-high again in December (6.4)
- Overall variation remains within a narrow band (~0.5 range)

**Insight**
 UrbanHaul’s rider performance is generally stable, but short-term operational disruptions or workload shifts periodically affect outcomes. The strong recovery at year-end suggests that corrective actions or seasonal normalization are effective when applied.

**Recommendation**
 Focus on reducing mid-year volatility by identifying and proactively managing the drivers behind temporary performance dips, while institutionalizing the practices that support strong year-end performance.

---

## 🧰 Tools & Skills Demonstrated
- Power BI (Power Query, Data Modeling, DAX, Visualization)
- KPI Design & Interpretation
- Business & Operational Analytics
- Executive Storytelling
- Stakeholder-Ready Recommendations

---

## ✅ Final Takeaway
This analytics solution enables UrbanHaul to move from **reactive management to proactive performance optimization**, aligning rider-level execution with executive-level strategy.


