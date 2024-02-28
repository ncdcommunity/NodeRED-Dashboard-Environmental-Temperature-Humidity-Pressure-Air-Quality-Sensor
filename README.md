# Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor 

This project is a sub-flow developed by **ncd.io** based on Node-RED and the Dashboard 2.0 module, which allows you to visualize the data provided by the "Industrial IoT Long Range Wireless Environmental Temperature Humidity Pressure Air Quality Sensor" in an intuitive way.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/60985aa2-a8bb-489a-b315-641e0d5d989a)


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

Download from web browser (tested in Chrome) of CSV files of each selected device filtered by date.

It automatically detects when a new Industrial IoT Long Range Wireless Environmental Temperature Humidity Pressure Air Quality Sensor is connected, obtains its MAC address and adds it in a dropdown so you can select the device you want to display the value of its variables, this is very useful for cases where you have more than one sensor of this type.

> [!IMPORTANT]
> This subflow currently only works with type sensors ("sensor_type": 27) which corresponds to the "Environmental Temperature Humidity Pressure Air Quality Sensor":
> 
> https://store.ncd.io/product/industrial-iot-long-range-wireless-environmental-temperature-humidity-pressure-air-quality-sensor/

It is possible to view the relevant sensor data in a "Data" tab.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a9360f56-9cd3-43af-8a5b-e640d954a286)


## Requirements/Dependencies:

To import this subflow it is necessary to have previously installed:

- Node-RED
- @ncd-io/node-red-enterprise-sensors
- @flowfuse/node-red-dashboard

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

## For installing Dashboard 2.0:

FlowFuse's Node-RED Dashboard 2.0 is available in the Node-RED Palette Manager. To install it:

  - Open the menu in the top-right of Node-RED
  - Click "Manage Palette"
  - Switch to the "Install" tab
  - Search node-red-dashboard
  - Install the @flowfuse/node-red-dashboard package (not node-red/node-red-dashboard)

Source: https://dashboard.flowfuse.com/getting-started.html

## Procedure to import the Sub-flow:

Copy the raw JSON file "/EnvironmentalTemperatureHumidityPressureAirQualitySensor.json" from this repository:
https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/tree/main

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a242e878-072a-4f08-8b18-a04ffdc138da)

Go to Node-RED, you can add a new flow in the node editor of node-red (optional):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/af04036e-8c5f-4902-a9cd-f55f4cead3e2)

Then, go to the main menu, select the "Import" option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/3c35c197-3fdf-4562-ab4b-3ceadbd2fded)

This opens a field, where we right click and paste the JSON code just copied from GitHub:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/ad498561-012f-4c71-b5ed-5a40e9aa4044)

You will see the JSON code, now you can press the red "Import" button at the bottom right (by default the "current flow" option is selected):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/682ee323-cc17-4ab8-88fb-a744adc5aff2)

In the upper part of the node editor, you will see information of the subflow you just imported, and automatically you will have the subflow available inside the node editor, now you can position it inside the editor by left clicking.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/b1525c22-24e6-420b-bafa-d689ac1af95e)

You may also notice that the subflow has been added to the ncd.io node group.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/c5cea09d-484a-4518-ac99-a38cfbfdbe28)

The next step is to configure your ncd.io nodes (you may have already configured your nodes), but it is important to remember that this procedure only works for the "environmental" type:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/443c388d-e41b-4c21-8b52-f7bc20956800)

> [!NOTE]
> If you are interested in knowing the complete process for the configuration of your environmental sensor inside Node-RED you can go to: ...

Once you have the environmental sensor configured, the next step is to connect the sensor output (node) to the subflow input:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/87d1d489-4af3-4bb4-8c13-42fd6e0778c8)

If you double left click on the subflow you can open the settings:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/e9428449-0490-4075-9eee-100e986a13d6)

**Name:** you can assign an identifier to the subflow, and this will only serve to identify your specific flow within the node editor (to differentiate it from other nodes).

**Custom Path:** this property by default is static, that is, the subflow takes the data coming from your environmental sensor and will store it in a local location inside Node-RED:

> [!NOTE]
> Automatically the subflow stores the generated csv files of the sensor(s) inside the Node-RED folder.
> - Linux: $HOME/.node-red/log
> - Windows: $HOMEPATH/.node-red/log

So by default it is not necessary to assign a value to this property, but, if for some reason you need the data generated by the sensor to be stored in another local location, then you can assign this property to that new location and the stream will now take that path to store the data:

- Lunix:
  
![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/392c0014-d158-4c0d-a02c-a182b4e571c1)

- Windows:
  
![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/cfc2b2d0-4e60-42a9-970f-71742da8f703)

The next step is to delploy, in order to apply the changes to our flow, this is done by clicking on the "Deploy" button located at the top right of the Node-RED flow editor:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/b525fa46-a4b4-43e2-8741-2120002a654b)


> [!IMPORTANT]
> You must be careful to assign a valid route because if the subflow detects that it is not a valid route it will display an error message:
> 
> ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a8050a51-a877-4363-9584-9c58ffc6a227)
> 
> If the path you enter is correct or you leave the default path (leaving the property text field blank), then when new data arrives through the sensor at the subflow input you should be able to see that the data is being stored correctly:
> 
> ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/8abc68d8-4171-4e75-be32-3899bc4ee408)


The next step is to go to your Dashboard to see the real time data coming from the sensor by clicking on the Dashboard 2.0 option in the sidebar:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/8dbb7799-6386-44e2-9dec-619168dae1f5)

> [!NOTE]
> In case you have deployed and cannot see the "Dashboard 2.0" window, you should reload the current page of the web browser with the "F5" key or the "Reload this page" icon.

Then click on the "Open Dashboard" option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/9d34c5c8-814d-4ea2-aa74-9c1b05da7f61)

Your Dashboard will automatically open in a new window, where you can see the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/d2523214-a7f0-4e64-a348-fd9825710ed5)

## we have:

- **The dropdown for temperature unit of measure** (by default is Celcius):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/219f6212-d0fb-4f9c-9718-c6e9b6c5c648)

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/e65c9587-8f5a-49b5-aa61-2f0bba9f6316)

- **The dropdown where you can select the device you want to display its information on the dashboard** (in case you have two or more sensors connected to the subflow input).

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/7103c9cd-bdef-44e9-bb36-14198894e48b)

- **The main menu:** where you can navigate between the tabs (sensor and data):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/32e5b33a-474d-4546-a986-2837a3d37631)

- **NodeID:** which corresponds to an identifier that you can configure from your IoT device, and displays its value on the Dashboard.

- **Type of sensor:** shows the type of sensor that is showing its value (for now only allows environmental).

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/7c8f7179-7af7-47ea-88b2-d7f3af7c9620)

- **Gauges and Graphs:** Where historical and real time information is displayed.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a5a88fad-8aa7-4616-a296-207ae5f12eaa)

When you select any of the devices in the list (in case you have two or more sensors connected to the input of this subflow) the data from the local csv files will be automatically loaded, and the last 20 values stored in the graphs will be displayed.

The data storage is per day, in order to have a better data management.

## Download from web browser of CSV files (Tested in Chrome):

You can see the box at the bottom left, where we have two fields:

1.- **Date:** corresponds to a date entry.

2.- **Download CSV button:** activates the download of the corresponding CSV file from the web browser.

To start downloading a CSV file from the dashboard, the first thing to do is to enter a date of interest by keyboard, that is, with the current device selected (using the MAC dropdown), the date of the stored data you are interested in downloading.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/050e07f6-da79-4ace-86fb-136570eb0eb4)

Format must be used: 

- **mm:** for month.
- **dd:** for day.
- **yyyy:** for year.

> [!IMPORTANT]
> It is important to verify that the date of interest entered corresponds to a valid date, i.e. that the subflow has been storing data (that there is a csv file corresponding to that date).

For example, assuming you have verified that the subflow has been storing data on the date **"February 27, 2024"**, and you need to download the CSV file generated on that date, then you would enter:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/c140c524-a92c-4dd2-90d5-78f98f949e54)

Then click on the **"Download CSV"** button:

If the subflow finds the file on that date, you should be able to see the download start (in the download icon of the web browser):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/138497b5-f6d2-4e10-b0bc-af2a3d4ea613)

In case you enter a date of interest, which there is no CSV file generated, and press the **"Download CSV"** button, you will see the following message:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/b421b06a-a826-48be-951d-7d4bdece56f6)

You should verify that a CSV file exists on that specific date.

...

## Possible errors when importing:

If you import the flow without having previously installed Dashboard 2, you will get a message like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/1607a7b0-0119-43cb-8920-48de92e3b968)

So you must delete the subflow and install the module "@flowfuse/node-red-dashboard" as mentioned at the beginning, and repeat the process.

To delete the subflow you must double-click on the subflow in the Node-RED node editor to open its properties:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/bed47734-0ca7-4dd6-9950-975e31836ccc)

Then click on the "Delete" button at the top of the window:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/c143c969-e92e-445a-a42b-f436d777a637)

By. ncd.io













