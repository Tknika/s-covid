# SCovid



## Introduction

**SCovid** is a NodeMCU (ESP8266 development board) based sensor for CO2 monitoring. 

It has been developed mainly for teachers (educational environments), in order to facilitate the measures of CO2 level at school.

![enter image description here](Sentsoreak.png "Sensors")

It measures the following magnitudes: 

	 - CO2 level    ppm 
	 - Tenperature  ºC 
	 - Humidity     %
	 - DEW point    ºC
 
![enter image description here](Muntaia.png "Muntaia")


## List of elements
|Elements| Quantity | Link | 
|---|---|---|
| Sense Air S8| 1 |[Sense Air - Digi Key](https://www.digikey.es/product-detail/es/senseair-north-america-inc/004-0-0017/2194-004-0-0017-ND/10416536?utm_adgroup=Gas%20Sensors&utm_source=google&utm_medium=cpc&utm_campaign=Shopping_Product_Sensors%2C%20Transducers&utm_term=&productid=10416536&gclid=CjwKCAjwxuuCBhATEiwAIIIz0dKA79hlJd5p6Pi6lWrorZQlp4i2TtIozsbHxj0ZyZ9SqScUC76-VBoC6QgQAvD_BwE)|
| DTH22 AM2302| 1 |[DTH22 - Electroson](https://electroson.com/producto/arduino-sensor-temperatura-y-humedad/ARDHT22)|
| Nodemcu| 1 |[Nodemcu - Electroson](https://electroson.com/)|
| Female-Female headers| 17 ||

> **Warning**: Try to buy locally ```nearest store```.

## Scheme
![enter image description here](eskemafzz_bb.png "Muntaia")

![enter image description here](eskemafzz_schem.png "Muntaia")

 - Connection pinout
 
|NodeMCU|DHT22|Sense Air S8|
|---|---|---|
| 3V3| VCC |-|
| GND| GND|-|
| D6| DATA |-|
| Vin|-|VCC|
| GND|-|GND|
| RX|-|TX|
| TX|-|RX|

  - (For a more detailed information, please refer to the following [link](https://senseair.com/products/size-counts/s8-residential/))


## Flashing process

Download and install [Tasmotizer software](https://github.com/tasmota/tasmotizer).


![enter image description here](Tasmotizer04.png "Tasmotizer")

Follow the steps. 

- Flash tasmota-sensors.bin latest firmware
- Send hardware, WiFi and MQTT configuration

![enter image description here](Tramotizer08.png "Tasmotizer")

- Get the device IP and access its web configuration tool, typing the IP address into any web browser: http://<ip_address>

![enter image description here](Tasmotizer10.png "Tasmotizer")

- Configure the sensors according to the next image:

![enter image description here](Tasmotizer12.png "Tasmotizer")

- The following template makes the configuration easier:

		{"NAME":"S-Covid","GPIO":[1,1600,1,1632,1,1,1,1,1216,1,1,1,1,1],"FLAG":0,"BASE":18}


## Result

 - Be sure that correct readings are displayed on the web interface of the Tasmota device.

![enter image description here](Tasmota100.png "Tasmotizer")


## Authors

(c) 2021 [Tknika](https://tknika.eus/) ([Aitor Iturrioz](https://github.com/bodiroga) ,  [Aitor Azpiroz](https://github.com/axpirina))

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
