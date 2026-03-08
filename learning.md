# Adaptive Learning Concepts

The "Learning" phase of A3T is divided into two distinct cycles: **Data Acquisition** and **Model Execution**.

## 1. Apparent Temperature (The Baseline)
The system calculates the "Heat Index" or "Real Feel" using the Rothfusz regression. 
* **Input:** Indoor Temp ($T$) + Indoor Humidity ($H$).
* **Output:** Apparent Temperature ($AT$).
* **Goal:** The thermostat targets a consistent $AT$ rather than a consistent $T$.

## 2. The Learning Mode (Human-in-the-Loop)
For the first 12 months, the system operates in **Observation Mode**:
1.  **Log State:** Every 5 minutes, the system logs Outdoor $T/H$, Indoor $T/H$, and the Current Setpoint.
2.  **Intercept Overrides:** When a user manually changes the ecobee, the system marks this as a "Correction Event."
3.  **Correlation:** The system analyzes what changed *outside* just before the user felt uncomfortable *inside*.

## 3. Weighting Factors
The model assigns weights to variables based on their impact on comfort:
* **Primary:** Indoor Humidity (The "Muggy" factor).
* **Secondary:** Solar Radiation (Time of Day / Window heat gain).
* **Tertiary:** Outdoor Temperature (Thermal lag of the house).
