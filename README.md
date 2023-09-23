# How to Connect Dash IoT Dashboard App to an ESP32 with a One-wire temperature sensor

This guide will walk you through the process of connecting the Dash IoT Dashboard App to an ESP32 equipped with a one-wire temperature sensor, allowing you to read the temperature and create alarms:

- Demonstrates a TimeGraph control which is updated every 10 minutes on the Dash IoT app.
- The temperature is also shown on a TextBox control on the Dash IoT app.
- Compatible with Dallas one-wire temperature sensors.
- Communicates through a Dash MQTT connection.
- Requires the Dash MQTT server for continuous temperature storage.

## Prerequisites

Before you begin, make sure you have the following:

- An ESP32 dev board.
- Tempreature sensor attached to pin 13, but can be changed.
- Arduino IDE with the arduino-dashio library installed, [available on GitHub.](https://github.com/dashio-connect/arduino-dashio)
- The **Dash IoT** app available here:

Apple              | Android
:-----------------:|:------------------:
[<img src=https://raw.githubusercontent.com/dashio-connect/python-dashio/master/Documents/download-on-the-app-store.svg width=200>](<https://apps.apple.com/us/app/dash-iot/id1574116689>) | [<img src=https://raw.githubusercontent.com/dashio-connect/python-dashio/master/Documents/Google_Play_Store_badge_EN.svg width=223>](<https://play.google.com/store/apps/details?id=com.dashio.dashiodashboard>)


## Getting Started

1. **Clone or Download the Code**: You can clone the code provided in this repository or download it as a ZIP file. 

2. **Modify Arduino File**: Edit the esp32-temp-sensor.ino file and enter your WiFi (yourWiFiSSID & yourWiFiPassword) and Dash account credentials (yourMQTTuserName, yourMQTTpassword) for the MQTT connection.

3. **Install the Arduino File**: Install and run the esp32-temp-sensor.ino file on your ESP32.

4. **Access the DashIO Dashboard**: Open the Dash IoT Dashboard App on your mobile device.

5. **Log In to your DashIO account**: If you don't have a DashIO server account and subscription, you can create one in the Dash IoT app.

6. **View your IoT device**: Under 'All Devices' -> 'Find New Device' -> 'My Devices on Dash', You should see a device named "Temperature" in your dashboard. Tap on it to access your IoT device.

7. . **Watch the temerature**: You will see the current temperature and the temperature graph will be updated every 10 minutes. You can zoom in and out and scroll through the temperature graph.

8.  **Set Alarms**: You can set the maximum and minimum temperature alarms. When the temperature falls outside the alarm setpoint you will receive a notification on your mobile device.


## Additional Information

- Uses the serial monitor to show what is going on (115200 baud).

- A BLE connection could easily be added for provisioning and to locallly connect to your Iot device.

- Feel free to explore and modify the code to add more features or integrate it with other sensors and controls.

Congratulations! You've successfully connected your ESP32 with a temperature sensor to the Dash IoT Dashboard App.