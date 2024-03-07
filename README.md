# Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor 

This project is a Subflow (ncd-dashboard) developed by **ncd.io** based on Node-RED and the Dashboard 2.0 module, which allows you to visualize the data provided by the Industrial IoT Long Range Wireless Environmental Temperature Humidity Pressure Air Quality Sensor in an intuitive way.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/8756160e-3db4-4cee-93af-3c0b9b138720)


## Sub-Flow Characteristics:

#### It allows an automatic local storage (from one or more connected devices of the same type) of the variables provided by the sensor in real time:

- Temperature.
- Pressure.
- Humidity.
- Gas resistance.
- Indoor Air Quality.
- Battery percentage.

#### Select the unit of measurement for the temperature variable:

- Celsius.
- Fahrenheit.

#### It is possible to view the relevant sensor data (Inspect button).

#### Download from web browser (tested in Chrome) of CSV files of each selected device filtered by date.

#### It automatically detects when a new Industrial IoT Long Range Wireless Environmental Temperature Humidity Pressure Air Quality Sensor is connected, obtains its MAC address and adds it in a dropdown so you can select the device you want to display the value of its variables, this is very useful for cases where you have more than one sensor of this type.

> [!IMPORTANT]
> This subflow currently only works with type sensors ("sensor_type": 27) which corresponds to the "Environmental Temperature Humidity Pressure Air Quality Sensor":
> 
> https://store.ncd.io/product/industrial-iot-long-range-wireless-environmental-temperature-humidity-pressure-air-quality-sensor/

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

> [!IMPORTANT]
> If you already have an ncd-dashboard (subflow) installed and configured in your current project, I recommend you review the **"Working with two or more ncd-dashboards in the same Node-RED project."** section later in this post.

> [!IMPORTANT]
> If you already have a dashboard 2.0 project created in your current workspace, I recommend you review the **"Import subflow to an existent dashboard 2.0 project"** section later in this post.

### Step 1 - Copy raw JSON file from Github repository
Copy the raw JSON file "@ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor" from this repository:
https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/tree/main

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a242e878-072a-4f08-8b18-a04ffdc138da)

### Step 2 - Import nodes
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

### Step 3 - Configure NCD.io nodes
The next step is to configure your ncd.io nodes (you may have already configured your nodes), but it is important to remember that this procedure only works for the "environmental" type:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/443c388d-e41b-4c21-8b52-f7bc20956800)

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

### Step 4 - Check your Dashboard
The next step is to go to your Dashboard to see the real time data coming from the sensor by clicking on the Dashboard 2.0 option in the sidebar:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/8dbb7799-6386-44e2-9dec-619168dae1f5)

> [!NOTE]
> In case you have deployed and cannot see the "Dashboard 2.0" window, you should reload the current page of the web browser with the "F5" key or the "Reload page".
>
> ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/31b6491b-c3db-4b0d-beb7-2158ca65c05d)


Then click on the "Open Dashboard" option:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/9d34c5c8-814d-4ea2-aa74-9c1b05da7f61)

Your Dashboard will automatically open in a new window, where you can see the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/c14db8b8-14ab-4818-b27f-6deda022ac94)


## ncd.io Dashboard Features

### Temperature Settings
The dropdown for temperature unit of measure (by default is Celcius):

**Celsius:**

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/45e5d802-a990-47ff-b1b5-8c23bf86658e)
![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/bb93dedb-f652-4851-86fc-cd84ac226d0e)

**Fahrenheit:**

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/cf122997-1752-4313-afe1-f0cb6d626812)
![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/436437c1-33ca-4621-a01b-d00504e9d5ee)

### MAC Device Selection
The dropdown where you can select the MAC device you want to display its information on the dashboard (in case you have two or more sensors connected to the subflow input).

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/127157ca-48a1-4ec5-a8a5-2522a0c159e5)

> [!NOTE]
> You will be able to see (in the dropdown) the list of the MAC address(es) of the devices connected to the subflow until you receive a new message after deploying, be patient.
### The main menu
You can navigate between the ui-pages (this menu allows you to navigate between two or more ncd-dashboards, in case you have configured different ncd-dashboards):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/ed97c4ed-924e-4b8d-89dc-e9f3dce310af)

> [!NOTE]
> For example if you have configured an ncd-environment-dashboard and you import an ncd-uptime-dashboard, you will be able to navigate between the subflows from the main menu:
>
> ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/7971257c-f9ec-4b6f-90db-7b79d46328a3)
>
> A step-by-step configuration for importing two or more ncd-dashboard subflows and accessing them from the main menu is presented later in this post.


### NodeID 
Corresponds to an identifier that you can configure from your IoT device, and displays its value on the Dashboard.

### Type of sensor
shows the type of sensor that is showing its value (for now only allows environmental).

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/5e14cd46-8ba7-4672-98d4-daaf46301814)

### Inspect Button
By pressing this button it is possible to access the information received from the sensor (NodeID, Firmware version, battery voltage, sensor type, MAC address, etc.), if pressed again it returns to the graphs and indicators view.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/d5c97824-0aea-440d-9c8c-08810a13e351)

### Gauges and Graphs
This is where historical and real time information is displayed.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a5a88fad-8aa7-4616-a296-207ae5f12eaa)

It is possible to connect two or more "Environment" type sensors to the input of this subflow, in order to visualize the data from a single ncd-dashboard:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/42cf6bb5-6ff7-4ce6-b5d3-3836119ce04e)

When you select any of the devices in the list (in case you have two or more sensors connected to the input of this subflow) the data from the local csv files will be automatically loaded, and the last 20 values stored in the graphs will be displayed.

> [!NOTE]
> The data storage is per day, in order to have a better data management.

## Download CSV files

It is possible to download the locally stored CSV files directly from the ncd-dashboard, which contain the historical data provided by the Environmental Temperature-Humidity Pressure Air Quality Sensor(s).

You can see the box at the bottom left, where we have two fields:

- **Date:** Corresponds to a date entry.
- **Download CSV button:** Activates the download of the corresponding CSV file from the web browser.
    
Format must be used:

- **mm:** for month.
- **dd:** for day.
- **yyyy:** for year.

To download a CSV file from the dashboard, the first thing to do is to select or enter a date of interest using the date picker, i.e. (with the current device selected using the MAC drop-down) the date of the stored data you are interested in downloading.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/ed7f3e90-8cab-4a78-a154-6a099ea888c4)


> [!IMPORTANT]
> It is important to verify that the date of interest entered corresponds to a valid date, i.e. that the subflow has been storing data (that there is a csv file corresponding to that date).

For example, assuming you have verified that the subflow has been storing data on the date **"March 5, 2024"**, and you need to download the CSV file generated on that date, then you would enter:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/48d2f584-16f1-4b25-a1a0-810e172e205a)

To display the date picker, click on the icon to the right of the date:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/4115c675-01c4-43bf-97c6-0849bb0916de)

Then click on the “Download CSV” button. If the subflow finds the file on that date, you should be able to see the download start (in the download icon of the web browser):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/138497b5-f6d2-4e10-b0bc-af2a3d4ea613)

In case you enter a date of interest, which there is no CSV file generated, and press the **"Download CSV"** button, you will see the following message:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/b421b06a-a826-48be-951d-7d4bdece56f6)

You should verify that a CSV file exists on that specific date.

> [!IMPORTANT]
> CSV file download is currently only available for the default data storage option (local in the path "./node-red").

## Working with two or more ncd-dashboards in the same Node-RED project

This instructions refers to the scenario where you have previously installed and configured an ncd-dashboard (subflow) and you want to import another ncd-dashboard (subflow) to the same project.

The procedure is the same as mentioned above, with the simple difference that as soon as you press the import button in the "Import nodes" window you will see the following message at the top of our Node-RED flow editor:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/7f89e293-b246-4143-9e91-25bf4f553beb)

This indicates that you are importing a subflow that contains one or more nodes that already exist in your current project (workspace). Specifically it refers to the configuration node **"ncd-ui-base"** which represents the base configuration of all our ncd-dashboards, simply click on the "Import copy" option. This shows us the detail of the elements that were imported in our project.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/cfaeb98e-238e-4720-be0e-92835271887b)

If everything is correct, the next step is to deploy in order to apply and execute the changes in our project, using the "Deploy" button:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/e15d0d20-7c89-483f-933e-884d76ab6885)

Now, if you go to the "Dashboard 2.0" tab and click on "Open Dashboard" or simply refresh the dashboard browser tab, you will see in the main dashboard menu the new imported ncd dashboard:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/b5c5e88f-7480-44da-9da2-21b478a7fca0) View from ncd-environment-dashboard            ![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/2d0a3bb2-7437-42c8-b96a-1afee9ffbf66) View from ncd-uptime-dashboard

## Import subflow to an existent dashboard 2.0 project.

This procedure refers to the scenario where you already have a dashboard 2.0 configured and you want to import an ncd-dashboard within the same Node-RED project.

For example, if you already have a dashboad 2.0 configured with some elements, in the dashboard you would have something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/44cc9048-0c76-4726-8158-e3c5983c5ac6)

To import an ncd-dashboard to your existing project you use the same steps mentioned above; copy the JSON file from the GitHub repository, use the import window (or Key shortcut Ctrl-i), paste the JSON and click on import, the imported elements will be shown at the top, but if you deploy inside the dashboard 2.0 you will have the following message:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/a6a314e7-177f-4480-8faa-25d628438adb)

To solve this you must return to the Node-RED flow editor, go to the "dashboard 2.0" tab and inside "Layout" you will be able to see something like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/f16d51c9-dc7f-4f71-9814-92830d8fb173)

You can identify the ui-pages of the ncd-dashboard by the fact that they are preceded by "ncd".

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/d9738a8d-edb4-4e55-b259-d7be6323e2b2)

Next to the "Your Page Name" identifier, if you hover the cursor you will see the "Edit" button, click on it:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/96db89b5-0df1-4797-8bc1-318cb6434eac)

This opens the page configuration window, in the UI property you will click on the "Edit" (pencil icon).

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/d35d4b29-dc6c-44d9-a145-553e16685203)

Now the configuration window of the "ui-base" configuration node opens, you should click on the "Delete" button (located in the upper left part of the window):

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/b02951c9-0efb-40b1-94d8-158cdfb4f975)

Automatically it returns to the ui-page window, and it shows us the box of the property "UI" with the outline in red color:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/f09b81ef-2bbc-49b8-9201-3408307d4395)

Click on the arrow and then select the property "ncd-ui-base[/dashboard]":

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/c6dcd6df-0dad-49e4-a1c6-805807e500d7)

Finally click on the "Update" button at the top right of the window:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/be030371-4b1a-4098-b86b-6418cec02a77)

> [!NOTE]
> this same procedure must be done if you have two or more pages previously configured in dashboard 2.0.

Now click on deploy button to apply the changes made to the project:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/93da7f6c-d76d-4770-b6b3-300d3025810d)

Go to the "Dashboard 2.0" tab and click on the "Open Dashboard" button:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/893c6c00-417a-461f-85f0-31ffc6b3e278)

You will notice that the identifier of the added ncd-dashboard has been added to the main menu of the dashboard 2.0:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/e4f76e68-a856-4a83-95f1-e043a4179ae7)

You can now navigate between your dashboard and the ncd-dashboard using the dashboard 2.0 navigation menu.

## Possible drawbacks during subflow import

### 1.- Import subflow without dependencies installed

If you import the flow without having previously installed Dashboard 2, you will get a message like the following:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/1607a7b0-0119-43cb-8920-48de92e3b968)

So you must delete the subflow and install the module "@flowfuse/node-red-dashboard" as mentioned at the beginning, and repeat the process. To delete the subflow you must double-click on the subflow in the Node-RED node editor to open its properties:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/bed47734-0ca7-4dd6-9950-975e31836ccc)

Then click on the "Delete" button at the top of the window:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/c143c969-e92e-445a-a42b-f436d777a637)

You must also delete the subflow node from the node palette in the "NCD" or "Sublows" group, double click on the node.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/bc21dc96-8010-4028-92d8-da6b2e7b259b)

This opens the subflow window, at the top click on the "delete subflow" button:

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/c4e499e5-c504-461a-b4a5-643b785b3a9f)

### 2.- Import the same subflow twice / delete subflow.

In case by mistake or by some procedure you have imported twice the same subflow, or you simply want to remove an ncd-dashboard subflow from the nodes palette, you must follow this quite simple procedure.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/ec5a8900-b033-4e8f-afa0-c8d9a22a5568)

1) Double click on the subflow node you wish to delete, the ncd-dashboard subflows are located in the node palette within the NCD group.
2) Once the "Edit subflow template" tab opens at the top, click on the "delete subflow" button.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/cbafc8ea-5e61-49dc-ade9-ea7277154e56)

This completely removes the subflow, as well as the associated configuration nodes, you will notice that it no longer appears in the nodes palette.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/0f033785-7678-4bf4-9f89-8fdb9635d659)

Do not forget to deploy in order to save and apply the changes made to your project.

![image](https://github.com/ncdcommunity/NodeRED-Dashboard-Environmental-Temperature-Humidity-Pressure-Air-Quality-Sensor/assets/159818736/3b79a41f-e8a3-4a4a-a93e-730fa767159a)

By. Eduardo from **ncd.io** team.













