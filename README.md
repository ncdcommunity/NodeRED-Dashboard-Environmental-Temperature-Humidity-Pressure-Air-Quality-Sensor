# Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor 

This project is a sub-flow developed by ncd.io, based on Node-RED and the Dashboard 2.0 module, which allows you to visualize the data provided by the "Industrial IoT Long Range Wireless Environmental Temperature Humidity Pressure Air Quality Sensor" in an intuitive way.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/577de3fc-9d73-484e-a48c-0dbedde0c0e1)


## Sub-Flow Characteristics:

It allows an automatic local storage (from one or more connected devices of the same type) of the variables provided by the sensor in real time:

- Temperature.
- Pressure.
- Humidity.
- Gas resistance.
- Indoor Air Quality.
- Battery percentage.

Select the unit of measurement for the temperature variable:

- Celsius.
- Fahrenheit.

It automatically detects when a new Industrial IoT Long Range Wireless Environmental Temperature Humidity Pressure Air Quality Sensor is connected, obtains its MAC address and adds it in a dropdown so you can select the device you want to display the value of its variables, this is very useful for cases where you have more than one sensor of this type.

It is possible to view the relevant sensor data in a "Data" tab.

## Requirements/Dependencies:

To import this subflow it is necessary to have previously installed:

Node-RED
@ncd-io/node-red-enterprise-sensors
@flowfuse/node-red-dashboard

## Install "ncd-io/node-red-enterprise-sensors":

Within your Node-RED instance go to the main menu (top right) and select the "Manage palette" option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a0c73443-c969-4c77-aa8d-6e421b629ec0)

In the window, select the "Install" tab:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/5b844567-a8de-47c7-80d2-d6131e7b3b3b)

In the search field enter "@ncd" you will see the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/4df7a163-2483-442d-b92b-78684166cb9e)

Click the "Install" button to start the installation process, a window will appear at the top of the screen, asking you to confirm the installation:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/27b2c1cb-f8dd-45c6-91b5-5cac58144329)

Once the process is completed you will see the following window:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/ba71c0f7-0689-4bde-8d49-ae415e485814)

## For installing dashboard 2.0:

...

## Procedure to import the sub flow:

Copy the raw JSON file "/EnvironmentalTemperatureHumidityPressureAirQualitySensor.json" from this repository:
https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/tree/main

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a242e878-072a-4f08-8b18-a04ffdc138da)

Go to Node-RED, you can add a new flow in the node editor of node-red:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/af04036e-8c5f-4902-a9cd-f55f4cead3e2)

Then, go to the main menu, select the "Import" option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/3c35c197-3fdf-4562-ab4b-3ceadbd2fded)

This opens a field, where we right click and paste the JSON code just copied from GitHub:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/ad498561-012f-4c71-b5ed-5a40e9aa4044)

You will see the JSON code, now you can press the red "Import" button at the bottom right (by default the "current flow" option is selected):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/682ee323-cc17-4ab8-88fb-a744adc5aff2)


...

Automatically the subflow stores the generated csv files of the sensor(s) inside the Node-RED folder.

- $HOME/.node-red/log
- $HOMEPATH/.node-red/log

But there is available the "Custom Path" field, where you can add a path to customize where the generated csv files are stored.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/ce60871b-6b7b-40a7-b836-02eb7123d4a4)

When you select any of the devices in the list (in case you have two or more sensors connected to the input of this subflow) the data from the csv files will be automatically loaded, and the last 20 values stored in the graphs will be displayed.

The data storage is per day, in order to have a better data management.

...

## Possible errors when importing:

If you import the flow without having previously installed Dashboard 2, you will get a message like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/1607a7b0-0119-43cb-8920-48de92e3b968)

So you must delete the subflow and install the module "@flowfuse/node-red-dashboard" as mentioned at the beginning, and repeat the process.

By. ncd.io













