# JÑĀNA-PARAMPARĀ AI — Dataset

## Project
**JÑĀNA-PARAMPARĀ AI: Intelligent Environmental Monitoring and Preventive Preservation of India's Palm-Leaf Knowledge Heritage**

**Track:** Hardware Track-3 — ESP32/Arduino (Intelligent Embedded Systems)  
**Application Domain:** Indian Knowledge System (IKS)

## Dataset Overview

This repository contains datasets used for the development of an environmental monitoring and preservation-risk classification system for palm-leaf manuscripts.

### Dataset 1 — Literature-Derived Environmental Evidence

**File:** `jnana_parampara_literature_evidence.csv`

This dataset summarizes environmental evidence derived from research literature on palm-leaf manuscript preservation.

It includes observations related to:
- Temperature
- Relative Humidity (RH)
- UV exposure
- Visible-light exposure
- Exposure duration
- Environmental fluctuations
- Observed deterioration

This evidence is used to guide the design of environmental scenarios, temporal features, and research-supported risk labeling.

### Dataset 2 — Synthetic Environmental Time-Series Dataset

**File:** `jnana_parampara_synthetic_timeseries.csv`

This dataset contains **6,000 synthetic one-minute environmental records** representing different preservation conditions.

Main fields include:

`timestamp, manuscript_id, scenario, temp_c, rh_percent, uv_index_sim, light_lux_sim, airflow_sim, risk_label`

Environmental scenarios include:
- Normal conditions
- High humidity
- Very dry conditions
- High UV/light exposure
- Poor airflow
- Combined environmental stress

The synthetic dataset is intended for initial development and testing of a **Random Forest-based preservation-risk classifier**.

## Machine-Learning Pipeline

Environmental Data  
→ Temporal Feature Extraction  
→ Random Forest Classification  
→ Preservation Risk  
→ **Alert + Reason + History**

The model is intended to classify preservation risk rather than directly diagnose physical deterioration.

## Future Dataset — Real Sensor Data

Real environmental readings will be collected using an **ESP32-S3-based prototype**.

Planned data collection:
- 1-minute sensor readings
- 5-minute aggregated environmental records

These data will be used for prototype evaluation and further refinement of the preservation-risk classification system.

## Important Note

The synthetic dataset and its risk labels are intended for prototype machine-learning development. They should not be interpreted as experimentally validated universal conservation thresholds.
