# Project: Ambient-Aware Adaptive Thermostat (A3T)

## Overview
The **Ambient-Aware Adaptive Thermostat (A3T)** is a DIY home automation project designed to bridge the gap between static scheduling and true personal comfort. Most smart thermostats rely on rigid setpoints; A3T aims to learn the user's "Thermal Comfort Zone" by analyzing the relationship between indoor/outdoor temperature and humidity.

## The Problem
In high-humidity environments (like Central Texas), a static temperature of 74°F can feel comfortable at 30% humidity but stifling at 65%. Current systems require manual intervention to "fix" the feeling, which defeats the purpose of "smart" technology.

## Project Goals
* **Contextual Intelligence:** Adjust ecobee setpoints based on Real-Feel (Apparent Temperature) rather than raw numbers.
* **Human-in-the-Loop Learning:** Implement a "Learning Mode" that treats every manual adjustment as a data point to refine a personalized comfort model.
* **Low-Cost Edge Interface:** Deploy a wall-mounted, small-form-factor touch display next to the existing thermostat for real-time telemetry and feedback.
* **Privacy-First:** All logic and data processing stay local (Home Assistant / MQTT / ESPHome).
