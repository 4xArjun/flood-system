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
