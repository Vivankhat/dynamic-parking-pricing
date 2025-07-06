# 🚗 Dynamic Pricing for Urban Parking Lots  
**Summer Analytics 2025 Capstone Project**

This project implements a real-time, demand-driven dynamic pricing system for 14 urban parking lots using a live data stream. Built using Pathway and Bokeh, it allows real-time visualizations of three models responding to live occupancy and demand conditions.
 
---

## 🏗️ Workflow Explanation

### 1. **Data Ingestion**
- The dataset (`dataset.csv`) contains real-time parking lot data.
- Uploaded into a Pandas DataFrame and then converted into a Pathway `pw.Table`.

### 2. **Model Implementations**

- **Model 1: Linear Pricing Model**
  - Price is linearly adjusted based on occupancy level.
  - Implemented with Pathway streaming + Bokeh.
  - Updates in real-time.

- **Model 2: Demand-Based Pricing**
  - Uses multiple factors: occupancy, queue length, nearby traffic, special events, and vehicle type.
  - Also runs live using Pathway and plots dynamically with Bokeh.

- **Model 3: Competitive Pricing**
  - Adjusts each lot’s price based on the pricing of nearby lots (distance calculated using lat-long).
  - Implemented as static logic (not yet streaming).
  - Outputs once and plots an instantaneous snapshot.

### 3. **Visualization Layer**
- Live Bokeh plots created for each model.
- Model 1 and 2 stream results live using `pw.run()` and show price changes per lot.
- Model 3 uses a static one-time plot of prices based on competitive logic.

---

## 🧠 Assumptions

- Occupancy data is streamed row by row.
- All inputs are normalized and bounded for pricing.
- Demand is calculated only for bike and car types.
- Competitors are only lots ≤ 0.5 km away.

---

## 📦 Tech Stack

| Tool     | Purpose                      |
|----------|------------------------------|
| **Pathway** | Stream processing engine     |
| **Bokeh**   | Real-time visualization     |
| **Panel**   | Multi-tab dashboards        |
| **Pandas/Numpy** | Data preprocessing   |

---

## 🧠 System Architecture

![Architecture Diagram](A_flowchart_diagram_in_digital_graphic_format_illu.png)

## 📈 Real-Time Visualizations

- Live Bokeh plots for each model (Model 1, 2)
- Tabs for each parking lot's individual behavior

---

## 📂 Files
- `Dynamic_Pricing_Urban_Parking_Solution.ipynb`: Main notebook + bokeh plot 
- `A_flowchart_diagram_in_digital_graphic_format_illu.png`: Architecture diagram

---
## 🧠 Authors & Acknowledgements

Submitted for **Summer Analytics 2025 Capstone Project**  
Thanks to the mentors and reviewers from the organizing team!
- Name: Vivan Khatri
- Submitted: **July 6, 2025**

