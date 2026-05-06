[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Y5lYn2wb)

# a11g-final-submission

**Team Number: 30**

**Team Name: Cooped Up**

| Team Member Name | Email Address | GitHub Username |
| ---------------- | -------------------------- | --------------- |
| Alexander Yu     | ayu2126@seas.upenn.edu     | lerntuspel      |
| Ben Sirota       | sirotab@seas.upenn.edu     | 21bsirota       |

**GitHub Repository URL:**

## 1. Video Presentation

## 2. Project Summary

## 3. Hardware & Software Requirements

### Hardware Requirements Specification (HRS)

| ID     | Description | Validation Outcome|
| ------ | ------------------------------------------- | ---------------------------------------- |
| HRS-01 | The temperature sensor shall measure temperature of a 1 cubic meter enclosed space within 1 degree C accuracy. | ✅ |
| HRS-02 | Ambient light sensor shall record outdoor brightness between 0 and 100000 lux | ✅ |
| HRS-03 | Automatic door shall be fully open within 30 seconds of request | ✅ |
| HRS-04 | Automatic door shall be fully closed within 30 seconds of request | ✅ |
| HRS-05 | Humidity control ducts shall fully open within 30 seconds of request | ✅ |
| HRS-06 | Humidity control ducts shall fully close within 30 seconds of request | ✅ |

### Software Requirements Specification (SRS)

| ID     | Description | Validation Outcome|
| ------ | ------------------------------------------- | ---------------------------------------- |
| SRS-01 | Temperature and humidity reading shall be recoreded in logs at a frequency of at least 4 times per hour over I2C. | ✅ |
| SRS-02 | On request from user application, latest log recording shall be sent to user over wifi. | ✅ |
| SRS-03 | The MCU shall detect when temperature inside coop is at or below 0C and singal outdoor watering bowls to start heating. | ❌ |
| SRS-04 | MCU shall recieve sunrise and sunset times from weather forcast once a day and retry 5 times if failed, to then fall back to using light sensor to determine when to open door | ✅ |
| SRS-05 | MCU shall recieve weather forcast once a day and retry every half hour if failed | ✅ |
| SRS-06 | Chicken activity level shall be logged with motion sensor trigger counts at a range of 0-3 meters. | ❌ |
| SRS-07 | Ambient Light Sensor shall communicate over I2C and start logging light level every 5 minutes starting from 30 minutes from sunrise/set times are predicted | ✅ |
| SRS-08 | The system shall do a calculate the difference between measured humidity of coop and outside humidity. If the coop is more humid, motors shall open the ducts automatically. If the coop is less humid, the ducts shall remain closed unless user override | ✅ |

## 4. Project Photos & Screenshots

## 5. Codebase

[Final Embedded C Firmware Codebase](https://github.com/ese5160/final-project-firmware-s26-t30-coopedup/tree/main/A09G/wifi_embedded_mqtt_client_soc)
[Node-RED Dashboard Code](https://github.com/ese5160/final-project-firmware-s26-t30-coopedup/blob/main/A09G/node-red.json)
