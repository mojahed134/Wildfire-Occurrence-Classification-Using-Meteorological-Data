🔥 Wildfire Occurrence Classification Using Meteorological Data
📌 Project Overview
This project aims to develop a binary classification model capable of predicting wildfire occurrence based on meteorological and Fire Weather Index (FWI) variables.
The project uses the Algerian Forest Fires Dataset, which contains daily observations of weather conditions and fire-related indicators collected from two regions in Algeria.
This repository represents Milestone 1 – Problem Definition & Dataset Understanding.

- 👥 Team Members
Mojahed Jaradat
Mohammad Alfageer
Bayan Albraiqi
Mutasem Ramadan
- **Milestone:** Milestone 1 – Problem Definition & Dataset Understanding

---

🎯 Business Problem & Motivation
Forest fires represent a catastrophic environmental hazard that causes loss of human lives, biodiversity destruction, and massive financial burdens on local authorities. A major operational challenge faced by civil protection and forestry management teams is the delayed detection and containment of sudden fire outbreaks. 

By utilizing real-time meteorological observations, this project aims to predict the immediate danger of fire occurrence. An early warning classification system enables authorities to allocate preventative firefighting resources and dispatch monitoring personnel proactively, mitigating damage before fires escalate.

---

🎯 Project Objectives
- **Supervised Learning Approach:** Develop a binary classification model that accurately predicts whether a wildfire will ignite (`fire` vs. `not fire`) on a specific day based on prevailing weather metrics.
- **Metric Prioritization:** Focus on high recall alongside accuracy to heavily penalize and minimize False Negatives (failing to predict an actual wildfire outbreak).
- **Interpretability:** Understand the primary weather parameters and fuel moisture codes that contribute most heavily to fire ignition.

---

📊 Dataset Understanding
### Source & Scope
- **Dataset Name:** Algerian Forest Fires Dataset
- **Source:** Kaggle (Uploaded by Nitin Choudhary) / Originally from the UCI Machine Learning Repository
- **Instances:** 244 daily observations (divided across two regions: Bejaia and Sidi Bel-abbes)
- **Features:** 14 attributes (13 input features and 1 target attribute, fitting the course recommended range of 5–15 features)

### Target Variable
- **Target Name:** `Classes`
- **Type:** Binary Categorical
- **Distribution:**
  - `fire`: 137 instances
  - `not fire`: 106 instances

### Feature Dictionary
1. **day / month / year:** Date indicators of the observation (June to September 2012).
2. **Temperature:** Noon temperature in Celsius (°C).
3. **RH (Relative Humidity):** Relative humidity percentage (%).
4. **Ws (Wind Speed):** Wind speed in km/h.
5. **Rain:** Daily rainfall accumulation in mm.
6. **FWI System Components:** Canadian Forest Fire Weather Index ratings:
   - **FFMC (Fine Fuel Moisture Code):** Moisture content of surface litter.
   - **DMC (Duff Moisture Code):** Moisture content of shallow organic layers.
   - **DC (Drought Code):** Moisture rating of deep organic layers.
   - **ISI (Initial Spread Index):** Numeric rating of fire spread potential.
   - **BUI (Buildup Index):** Cumulative rating of total available combustible fuel.
   - **FWI (Fire Weather Index):** Overall numerical danger rating of fire intensity.

---

## 5. Technical Submission & Verification
The data pipeline and schema verification are handled in `load_project_data.py`:
- Successfully loaded and parsed with `pandas`.
- Stripped unnecessary whitespace in feature headers and category labels.
- Verified missing values count (`0` nulls after cleaning extraneous header splits).
- Verified initial data dimensions: `(244, 14)`.

---

## 6. How to Run the Inspection Script
Ensure you have Python and `pandas` installed, then run:

```bash
pip install pandas
python load_project_data.py
