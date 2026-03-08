# Logic Flow & Automation



### State Machine
1.  **IDLE:** Monitoring sensors.
2.  **EVALUATE:** Check if $AT$ (Apparent Temp) has drifted outside the comfort threshold ($\pm 0.5$ degrees).
3.  **PREDICT:** Query the learned model: "Given current conditions, what is the user's preferred setpoint?"
4.  **PROPOSE:** (In Learning Mode) Display the suggestion on the wall screen: *"Adjust to 73? [Yes/No]"*
5.  **ACT:** Update ecobee via API.

### Variables to Track
```python
{
  "timestamp": "ISO8601",
  "outdoor_temp": "float",
  "outdoor_humidity": "float",
  "indoor_temp": "float",
  "indoor_humidity": "float",
  "user_override": "boolean", # Did the user manually touch the ecobee?
  "target_setpoint": "float"
}
