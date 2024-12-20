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

Processes sensor inputs using  logical blocks.
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
# 5.ThingSpeak Output

ThingSpeak is used to visualize real-time data from the system.

## Setup

1. **Create a ThingSpeak Channel** with two fields:
    - **Field 1**: Water pump status
    - **Field 2**: Light relay status

2. **Get the Channel ID and Write API Key** from your ThingSpeak channel after creation.

3. **Add the API Keys and Channel ID to Simulink Write blocks** for proper connectivity:
    - Use the **ThingSpeak Write** blocks in Simulink to send data to ThingSpeak.
    - Configure the **Field 1** for Water pump status and **Field 2** for Light relay status.

## ThingSpeak Output Example:

- Once the system is running, ThingSpeak will display the real-time data like this:

    ```
    Field 1: 1 (Water Pump ON)
    Field 2: 0 (Light OFF)
    ```

    Values will update automatically based on the status sent from Simulink.
  ## ThingSpeak Output Visualization

Below is an example of how the real-time data visualization might look on the ThingSpeak dashboard:

![ThingSpeak Dashboard Example](simulink/Thinkspeak_out.png)
# 6. Real-World Applications

The IoT Smart Farming system has a range of practical applications:

## 1. Precision Agriculture
- **Automating irrigation and lighting**: This helps to reduce water wastage while ensuring optimal crop growth.
- **Remote monitoring and control**: Farmers can use ThingSpeak to remotely monitor and control field conditions, optimizing resources and improving productivity.

## 2. Greenhouses
- **Real-time regulation**: The system can automatically regulate moisture levels and light conditions in controlled environments, resulting in better yields and healthier plants.

## 3. Urban Farming
- **Smart gardening**: The IoT system is ideal for urban farming in small spaces, especially in areas where manual plant care is difficult. It allows for efficient and automated care for plants, even in limited or non-traditional farming environments.

# 7.Conclusion

This IoT Smart Farming simulation demonstrates the potential for automated plant care using Arduino and cloud platforms like ThingSpeak. It provides a scalable solution for real-world farming automation.The system was designed and simulated using MATLAB and Simulink, with significant inspiration and components adapted from a MathWorks example model on the same topic.
