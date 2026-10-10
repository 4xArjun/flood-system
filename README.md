# flood-system
# 🌊 FloodReady: Flood Early-Warning & Relief Prioritisation System

**IBM Z Datathon 2026 — Week 6 Mini Challenge Submission**

FloodReady is an automated, lightweight data pipeline that bridges IoT river sensor telemetry with village demographic data. It predicts river flooding 48 hours in advance and dynamically prioritizes emergency relief resources for at-risk populations.

---

## 🎯 Problem Statement

When heavy rainfall hits, emergency response teams face two critical bottlenecks:
1. Detecting river overflows before water breaches safety thresholds.
2. Directing limited rescue and relief resources to the most vulnerable villages first.

---

## ⚡ Core Features

* **48-Hour Predictive Modeling:** Combines real-time river levels with forecasted rainfall and runoff rates to project water levels 48 hours into the future.
* **Dynamic Relief Prioritisation:** Calculates a unified **Priority Score** combining flood risk, population density, and local vulnerability scores.
* **Automated Actionable Alerts:** Translates raw risk scores into plain-language dispatch instructions for emergency coordinators.
* **Zero External Dependencies:** Built with pure Python standard library for instant execution and high operational reliability.

---

## 🏗️ System Architecture
+------------------------+      +--------------------------+
|   IoT River Sensors    |      |  Demographic & Village   |
|   & Rain Forecasts     |      |   Vulnerability Data     |
+-----------+------------+      +------------+-------------+
|                                |
+----------------+---------------+
|
v
+-------------------------------+
|   48h Hydrological Engine     |
|   (Threshold & Flood Check)   |
+---------------+---------------+
|
v
+-------------------------------+
| Prioritisation & Alert Engine |
| (Priority Score & Dispatch)   |
+-------------------------------+


## 🧮 Logic & Formulation

### 1. 48-Hour River Level Prediction
$$\text{Predicted Level}_{48\text{h}} = \text{Current Level} + (\text{48h Rain Forecast} \times \text{Runoff Coefficient})$$

If $\text{Predicted Level}_{48\text{h}} \ge \text{Danger Threshold}$, the river is flagged as an active flood hazard.

### 2. Village Relief Prioritisation
$$\text{Priority Score} = \text{Flood Status (1 or 0)} \times \text{Vulnerability Score} \times \text{Population}$$

Villages are sorted in descending order of their Priority Score so rescue efforts prioritize high-density, highly vulnerable regions.


