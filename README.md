# EV Charging Station Analysis
**Data Analytics with AI Academic Internship Project**

---

## 📋 Program Attribution

| Field | Details |
|---|---|
| **Program** | IBM SkillsBuild Data Analytics with AI Academic Internship |
| **Conducted by** | BharatCares in association with AICTE |
| **Student Name** | Kanishkaraj R P R |
| **College** | Misrimal Navajee Munoth Jain Engineering College |

---

## 🚀 Project Overview

This project applies an end-to-end data analytics and machine learning pipeline to global electric vehicle (EV) charging infrastructure data. As EV adoption accelerates worldwide, public charging availability remains uneven. This project analyses **5,000 global station records across 17 attributes** to evaluate usage patterns, cost structures, operator footprints, and renewable energy integration. It delivers both strategic insights and a predictive priority-scoring model to guide smarter infrastructure planning.

---

## 📂 Dataset Details

| Property | Value |
|---|---|
| **File Name** | `detailed_ev_charging_stations.csv` |
| **Volume** | 5,000 records |
| **Dimensions** | 17 attributes |

**Key Attributes:**
`Station ID` · `Latitude` · `Longitude` · `Address` · `Charger Type` · `Cost (USD/kWh)` · `Availability` · `Distance to City (km)` · `Usage Stats (avg users/day)` · `Station Operator` · `Charging Capacity (kW)` · `Connector Types` · `Installation Year` · `Renewable Energy Source` · `Reviews (Rating)` · `Parking Spots` · `Maintenance Frequency`

---

## 🛠️ Technologies Used

| Category | Tools / Libraries |
|---|---|
| **Language** | Python 3.11 |
| **Data Manipulation** | `pandas`, `numpy` |
| **Visualisation** | `matplotlib`, `seaborn` |
| **Machine Learning** | `scikit-learn` |
| **Environment** | Jupyter Notebook (`.ipynb`) · VS Code |

---

## 📊 Key Analytical Findings

### 1. Exploratory Data Analysis (EDA)

| Chart | Finding |
|---|---|
| **Usage vs. Distance (Scatter)** | Stations within 5 km of urban centres achieve higher daily footfall; high-capacity DC Fast Chargers can partially offset peripheral locations |
| **Avg Cost by Charger Type (Bar)** | DC Fast Chargers command a higher per-kWh rate than AC Level 2 units, consistent with infrastructure cost and rapid-charge convenience |
| **Operator Market Share (Bar)** | Moderately fragmented market — EVgo and ChargePoint lead, but mid-tier operators hold viable positions |
| **Renewable Energy (Count Plot)** | Near-even split between green-powered and fossil-grid stations, indicating clear room for mandatory regulatory thresholds |

### 2. Predictive Machine Learning Model

- **Algorithm:** Logistic Regression (binary classifier)
- **Target:** `High_Utilization` — 1 if daily usage > median, else 0
- **Features:** Charging Capacity (kW) · Cost (USD/kWh) · Distance to City (km) · Parking Spots · Reviews (Rating)
- **Split:** 80% train / 20% test (stratified)
- **Preprocessing:** `StandardScaler` fitted on training data only (no leakage)
- **Metrics:** Accuracy · Precision · Recall · Confusion Matrix

### 3. Priority Scoring Framework

Utilization probabilities from `predict_proba` classified into three tiers:

| Tier | Probability Threshold | Action |
|---|---|---|
| 🔴 HIGH | ≥ 0.75 | Priority maintenance, capacity upgrades |
| 🟡 MEDIUM | 0.50 – 0.74 | Growth candidate, targeted improvements |
| 🟢 LOW | < 0.50 | Strategic review / redeployment |

Exported to → **`ev_station_priority_scores.csv`**

---

## ⚙️ Setup & Run Instructions

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Place the Dataset

Ensure `detailed_ev_charging_stations.csv` is accessible and update the path in **Block 2** of the notebook:

```python
CSV_PATH = r'path\to\detailed_ev_charging_stations.csv'
```

### 3. Run the Notebook

Open `Kanishkaraj_RPR_EV_Charging_Station_Analysis.ipynb` in Jupyter and run:

```
Kernel → Restart & Run All
```

---

## 📁 Project Files

| File | Description |
|---|---|
| `Kanishkaraj_RPR_EV_Charging_Station_Analysis.ipynb` | Main analysis notebook (5 blocks) |
| `requirements.txt` | Python dependencies |
| `detailed_ev_charging_stations.csv` | Dataset |
| `chart1_usage_vs_distance.png` | Scatter — Usage vs. Distance to City |
| `chart2_avg_cost_by_charger_type.png` | Bar — Avg Cost by Charger Type |
| `chart3_top_operators.png` | Bar — Top 10 Operator Market Share |
| `chart4_renewable_energy.png` | Count plot — Renewable Energy Breakdown |
| `chart5_confusion_matrix.png` | Confusion Matrix — Logistic Regression |
| `Kanishkaraj_RPR_EV_Charging_Station_ProjectReport.docx` | Formal project report |

---

## 📓 Notebook Structure

| Block | Purpose |
|---|---|
| **Block 1** | Setup & Imports |
| **Block 2** | Data Loading & Inspection |
| **Block 3** | EDA & Visualizations (4 charts) |
| **Block 4** | Logistic Regression Model + Evaluation |
| **Block 5** | Priority Scoring & CSV Export |

---

*IBM SkillsBuild Data Analytics with AI Academic Internship · BharatCares × AICTE*
