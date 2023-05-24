# Azure IoT Central  ESP8266 DHT project
- Send real time data on Azure IoT central USING esp8266 and DHT sensor.
## Steps.
### Create Azure IoT Account.
* [Free 200$ credit to get started with Azure](https://azure.microsoft.com/en-us/free/iot/?ef_id=_k_CjwKCAjw67ajBhAVEiwA2g_jEKmTrubEELGFt_WCZo4pVuSlGMyvH6mtm94XVOJZVJeu7qB0fkmfzBoC3VoQAvD_BwE_k_&OCID=AIDcmm4z26duq7_SEM__k_CjwKCAjw67ajBhAVEiwA2g_jEKmTrubEELGFt_WCZo4pVuSlGMyvH6mtm94XVOJZVJeu7qB0fkmfzBoC3VoQAvD_BwE_k_&gclid=CjwKCAjw67ajBhAVEiwA2g_jEKmTrubEELGFt_WCZo4pVuSlGMyvH6mtm94XVOJZVJeu7qB0fkmfzBoC3VoQAvD_BwE)

### Create Azure IoT Central applications.
* There are two ways to achieve this:
1. Through the Azure portal, by navigating to Azure market place and searching for Azure IoT Central Application.
- Click and provide the name and other mandatory details,
* <img width="869" alt="Screenshot 2023-05-24 210201" src="https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/assets/55284959/a09028fc-11cc-497d-8fdf-b6f1830c5686">

2. By login into the Azure IoT central and creating an application directly.

### Create Azure IoT Central dashboard and device.
- Configure the template.
- Configure the device.

### Coding, 
a). [Download the zipped file in this repository.](https://github.com/AronAyub/Azure-IoT-Central--ESP8266-DHT-project/blob/main/AzureIotCentralEsp8266DHT.zip)
b). Edits the mandatories in the Arduino Code.

#### Network Configuration 
- Copy paste your wifi creditials as below.
- You can create a wireless connection with your mobile phone. 
```
#define WIFI_SSID "name"
#define WIFI_PASSWORD "password"
```


