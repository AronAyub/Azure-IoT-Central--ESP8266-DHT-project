<!-- vscode-markdown-toc -->
* 1. [Create Azure Account.](#CreateAzureAccount.)
	* 1.1. [Create Azure IoT Central application.](#CreateAzureIoTCentralapplication.)
	* 1.2. [Create Azure IoT Central dashboard and device.](#CreateAzureIoTCentraldashboardanddevice.)
* 2. [Circuit diagram.](#Circuitdiagram.)
* 3. [Coding,](#Coding)
	* 3.1. [DHT configuration](#DHTconfiguration)
	* 3.2. [Network Configuration](#NetworkConfiguration)
	* 3.3. [Device Configurations](#DeviceConfigurations)
* 4. [Troubleshooting](#Troubleshooting)
	* 4.1. [Arduino code not compiling !](#Arduinocodenotcompiling)
	* 4.2. [Showing null data on Serial monitor?](#ShowingnulldataonSerialmonitor)
	* 4.3. [Error in connecting to Azure IoT central ?](#ErrorinconnectingtoAzureIoTcentral)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->

# Azure IoT Central  ESP8266 DHT project
<img width="717" alt="realtime" src="https://github.com/AronAyub/Azure-IoT-Raspberry-Pi/assets/55284959/2244e9c5-de57-45a0-ad8d-6047c1b9f51a">

-  Send real time data on Azure IoT central using esp8266 and DHT sensor.
**Steps.**
##  1. <a name='CreateAzureAccount.'></a>Create Azure Account.

*[Free 200$ credit to get started with Azure](https://azure.microsoft.com/en-us/free/iot/?ef_id=_k_CjwKCAjw67ajBhAVEiwA2g_jEKmTrubEELGFt_WCZo4pVuSlGMyvH6mtm94XVOJZVJeu7qB0fkmfzBoC3VoQAvD_BwE_k_OCID=AIDcmm4z26duq7_SEM__k_CjwKCAjw67ajBhAVEiwA2g_jEKmTrubEELGFt_WCZo4pVuSlGMyvH6mtm94XVOJZVJeu7qB0fkmfzBoC3VoQAvD_BwE_k_gclid=CjwKCAjw67ajBhAVEiwA2g_jEKmTrubEELGFt_WCZo4pVuSlGMyvH6mtm94XVOJZVJeu7qB0fkmfzBoC3VoQAvD_BwE)

###  1.1. <a name='CreateAzureIoTCentralapplication.'></a>Create Azure IoT Central application.
* There are two ways to achieve this:
1. Through the Azure portal, by navigating to Azure market place and searching for Azure IoT Central Application.
- Click and provide the name and other mandatory details,
* <img width="869" alt="Screenshot 2023-05-24 210201" src="https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/assets/55284959/a09028fc-11cc-497d-8fdf-b6f1830c5686">

2. By login into the Azure IoT central and creating an application directly.

###  1.2. <a name='CreateAzureIoTCentraldashboardanddevice.'></a>Create Azure IoT Central dashboard and device.
- Configure the template.
- Configure the device.
* (Well explained in the video)

##  2. <a name='Circuitdiagram.'></a>Circuit diagram.
- The diagram is simple as below:
- Note that D4-GPIO2 as of the pinout

<img width="633" alt="Screenshot 2023-05-24 220030" src="https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/assets/55284959/6994a628-8f12-494a-90da-d0de9eca6ad7">

##  3. <a name='Coding'></a>Coding, 
a). [Download the zipped file in this repository.](https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/blob/main/AzureIotCentralEsp8266DHT.zip)

b). Edits the mandatories in the Arduino Code.

###  3.1. <a name='DHTconfiguration'></a>DHT configuration
- Edit your dht type - either as DHT22 or DHT11
- indicate the Digital pin you what to use, they are all in GPIOS, eg, D4 is GPIO2  hence assigned as 2.

* <img width="362" alt="Screenshot 2023-05-24 220030" src="https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/assets/55284959/81898100-8144-40a2-8658-061bf858bec8">

###  3.2. <a name='NetworkConfiguration'></a>Network Configuration 
- Copy paste your wifi creditials as below.
- You can create a wireless connection with your mobile phone. 
```

#define WIFI_SSID "name"
#define WIFI_PASSWORD "password"
```
###  3.3. <a name='DeviceConfigurations'></a>Device Configurations 
- From your created device on IoT Central copy paste the creditials as below:

```
const char* SCOPE_ID = "xoopjbjhvgyt";
const char* DEVICE_ID = "ynmhgtfyddyj";
const char* DEVICE_KEY = "ttttthhbytdcrgh";
```
##  4. <a name='Troubleshooting'></a>Troubleshooting 
###  4.1. <a name='Arduinocodenotcompiling'></a>Arduino code not compiling !
- Make sure you have installed old version of esp8266 library, do not use the latest version.

<img width="866" alt="esparduio" src="https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/assets/55284959/943f1139-5c1d-43c7-8ac6-eed2ae7ebd10">

###  4.2. <a name='ShowingnulldataonSerialmonitor'></a>Showing null data on Serial monitor?

- Confirm your wiring Circuit diagram.
- Check pin defination and DHT type you are using .

<img width="908" alt="nan" src="https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/assets/55284959/22af2108-8dfb-4721-8700-f7d52b474413">

###  4.3. <a name='ErrorinconnectingtoAzureIoTcentral'></a>Error in connecting to Azure IoT central ?
- Confirm your connection strings from your device on Azure IoT Central application.

<img width="761" alt="error get" src="https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/assets/55284959/b9eb3010-86e9-410d-9e13-906a2f680a3b">
