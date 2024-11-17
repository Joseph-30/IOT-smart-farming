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

# 3. Algorithm Block Description

The algorithm block processes input sensor data and compares it with predefined thresholds. The logic includes:

- If **moisture < threshold**, the **water pump** is turned **ON**.
- If **light intensity < threshold**, the **light relay** is activated.
- Outputs are converted into digital signals and sent to **ThingSpeak** for visualization.

## Algorithm Block Diagram:

<img src="simulink%20images/Algorithm.png" width="500" alt="Example Image">

# 4. Steps for Simulation

## Step 1: Initialize Simulink Model
- Open the provided **Simulink model** and configure the sliders for sensor simulation.
### Simulink Model

The Simulink model for the intelligent plant watering system is located in the **SimulinkModel** folder. 

#### Model File
- **File**: [IOT_smart_farming.slx](simulink/IOT_smart_farming.slx)

#### How to Use the Model:
1. **Download or Clone** this repository to your local machine.
2. Open the **plant_watering_model.slx** file in **Simulink** (MATLAB).
3. Configure any sliders or input parameters as needed for simulation.
4. Run the model to simulate the intelligent plant watering system.

## Step 2: Define Thresholds
- Set desired values for **moisture**, **light intensity**, and **humidity thresholds** using the sliders.

## Step 3: Connect ThingSpeak
- Ensure the **ThingSpeak Write blocks** are configured with the correct **Channel ID** and **API keys**.

## Step 4: Run the Simulation
- Click **Run** to start the simulation.
- Observe the system's behavior in **Simulink** and **ThingSpeak**.

## Step 5: Analyze Outputs
- Check the **actuator responses** (pump and light) and verify **ThingSpeak charts** for visualization.

this is taken from matlab projects
