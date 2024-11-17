# IOT-smart-farming
Smart farming leverages IoT technology to optimize agricultural practices. By utilizing sensors to collect data on soil moisture, humidity and light intensity,  farmers can make informed decisions. For the collection of data and visualising of the output thinkspeak platform is used.
The IoT Smart Farming system is designed to monitor and manage a plant watering system using Arduino and ThingSpeak there is also modules present that will give random values by rotating the knob. It integrates environmental sensors and uses algorithms to automate watering and light regulation based on predefined thresholds. The system's simulation was conducted in MATLAB Simulink.

## Objective
To simulate an intelligent plant watering system that:

-Ensures optimal soil moisture and light conditions.

-Sends real-time data to ThingSpeak for monitoring.


# 1. System Architecture

The system is divided into three main sections:

### Sensor Input:

Simulates sensor data for moisture, humidity, and light intensity.
Data sources are sliders in Simulink.
### Algorithm Module:

Processes sensor inputs using >= or <= logic blocks.
Outputs decisions (e.g., turn ON/OFF actuators).
### Actuator and Visualization:

Digital signals control the water pump and light relay.
Results are sent to ThingSpeak using Write blocks.

Simulink Model Overview:

<p align="center">
  <img src="simulink%20images/Smart_farming.png" width="800" alt="Example Image" >
</p>

# 2. Inputs and Outputs

## Inputs:

### Sensors:
- **Moisture sensor** (simulated data from sliders).
- **Light intensity sensor**.
- **Humidity sensor**.

### Threshold Values:
- User-defined thresholds for:
  - Moisture levels.
  - Light intensity.
  - Humidity.

## Outputs:

### Actuators:
- **Water pump**: ON/OFF based on moisture levels.
- **Light control relay**: ON/OFF based on light intensity.

### Visualization:
- Data sent to ThingSpeak fields for live monitoring:
  - **Field 1**: Water pump status.
  - **Field 2**: Light relay status.

## Subheading (Subsection 1.1)

This is a how algorithm looks like
![smart1](simulink%20images/Algorithm.png)
<img src="simulink%20images/Algorithm.png" width="500" alt="Example Image">

### Sub-subheading (Subsection 1.1.1)

This is a sub-sub-section under Subsection 1.1.
this is taken from matlab projects
