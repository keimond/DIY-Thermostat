# Hardware Specification

To keep the project budget-friendly and "wall-stealthy," we are utilizing ESP32-based hardware.

## Core Components
| Item | Model/Specs | Approx. Cost |
| :--- | :--- | :--- |
| **Microcontroller/Display** | ESP32-2432S028 ("Cheap Yellow Display") | $15 - $25 |
| **Power Converter** | 24V AC to 5V DC Buck Converter (Step-Down) | $8 |
| **Enclosure** | 3D Printed Low-Profile Wall Mount | ~$2 (Filament) |
| **Connectivity** | 2.4GHz Wi-Fi (Integrated) | Included |

## Power Integration
The device is designed to be mounted adjacent to an **ecobee thermostat**. 
* **Source:** Taps into the 24V AC 'C-Wire' and 'R-Wire' from the HVAC terminal.
* **Conversion:** The buck converter sits inside the wall gang box to provide clean 5V DC power to the ESP32 via micro-USB or pin headers.

## Software Stack
* **Firmware:** ESPHome or openHASP.
* **Controller:** Home Assistant (Raspberry Pi or Home Server).
* **Communication:** MQTT or Native API.
