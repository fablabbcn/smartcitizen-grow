Soil and Water Probes
=====================

![](https://i.imgur.com/DT45dpM.jpg)


## Introduction

 This board have been designed to monitor the water temperature, the pH, the electrical conductivity and the disolved oxygen of an aquaponics system. It is meant to be used with the [Smart citizen kit](https://smartcitizen.me/). 
 
## Metrics and Sensors

 |  ID	 | 	Name	 | 	Description	 | 	Unit	 | 	Measurement	 | 	Description | 
 | ------| :-------- | :-------------| :---------| :-------------------- | :----------------------- |
 | 10	 | 	Battery	 | 	Custom Circuit	 | 	%	 | 	battery	 | 	The SCK remaining battery level in percentage. | 
 | 13	 | 	HPP828E031	 | 	Humidity	 | 	%	 | 	humidity	 | 	Relative humidity is a measure of the amount of moisture in the air relative to the total amount of moisture the air can hold. For instance	 | 		 | 	 if the relative humidity was 50%	 | 		 | 	 then the air is only half saturated with moisture. | 
 | 12	 | 	HPP828E031	 | 	Temperature	 | 	ºC	 | 	air temperature	 | 	Air temperature is a measure of how hot or cold the air is. It is the most commonly measured weather parameter. Air temperature is dependent on the amount and strength of the sunlight hitting the earth	 | 		 | 	 and atmospheric conditions	 | 		 | 	 such as cloud cover and humidity	 | 		 | 	 which trap heat. | 
 | 14	 | 	BH1730FVC	 | 	Digital Ambient Light Sensor	 | 	Lux	 | 	light	 | 	Lux is a measure of how much light is spread over a given area. A full moon clear night is around 1 lux	 | 		 | 	 inside an office building you usually have 400 lux and a bright day can be more than 20000 lux. | 
 | 15	 | 	MiCS-4514	 | 	NO2	 | 	kOhm/ppm	 | 	no2	 | 	Nitrogen dioxide is a toxic gas. It is a pollutant in some urban areas due the excess air required for complete combustion of fuels introduces nitrogen into the combustion of internal combustion engines (cars	 | 		 | 	 trucks	 | 		 | 	 ships...) and power stations. ⚠ Note: values are offered in RS (sensor resistance in kOhm) as a relative measurement from the R0 (sensor zero resistance). Due to sensor intra-model variability we recommend using this as a relative measurement within the same kit readings. | 
 | 16	 | 	MiCS-4514	 | 	CO	 | 	kOhm/ppm	 | 	co	 | 	Carbon monoxide is a colorless	 | 		 | 	 odorless	 | 		 | 	 and tasteless gas. It is a pollutant in some urban areas coming from the exhaust of internal combustion engines  (cars	 | 		 | 	 trucks	 | 		 | 	 ships...)  and incomplete combustion of various other fuels. ⚠ Note: values are offered in RS (sensor resistance in kOhm) as a relative measurement from the R0 (sensor zero resistance)	 | 		 | 	 we approximate R0 at 75kOhm. | 
 | 29	 | 	MEMS Mic	 | 	MEMS microphone with envelope follower sound pressure sensor (noise)	 | 	dBC	 | 	noise	 | 	dB's measure sound pressure difference between the average local pressure and the pressure in the sound wave.  A quiet library is below 40dB	 | 		 | 	 your house is around 50dB and a diesel truck in your street 90dB. | 
 | 42	 | 	DS18B20	 | 	Submergible Water Temperature sensor	 | 	°C	 | 	water temperature	 | 	Water temperature is a measure of how hot or cold the water is. | 
 | 46	 | 	AS EZO  Specific Gravity	 | 	Atlas Scientific EZO™ Specific Gravity	 | 	SG	 | 	specific gravity	 | 	The density of a substance to the density of a reference substance. | 
 | 49	 | 	AS  EZO Oxygen Saturation	 | 	Atlas Scientific EZO™ Oxygen Saturation	 | 	%	 | 	oxygen saturation	 | 	Relative measure of the concentration of oxygen that is dissolved in Water | 
 | 43	 | 	AS EZO PH	 | 	Atlas Scientific EZO™ pH	 | 	PH	 | 	pH	 | 	pH is a numeric scale used to specify the acidity or basicity of an aqueous solution. | 
 | 48	 | 	AS  EZO Dissolved Oxygen	 | 	Atlas Scientific EZO™ Dissolved Oxygen	 | 	mg/L	 | 	dissolved oxygen	 | 	Absolute measure of the concentration of oxygen that is dissolved in Water | 
 | 45	 | 	AS EZO Electrical Conductivity	 | 	Atlas Scientific EZO™ Electrical Conductivity	 | 	µS/cm	 | 	electrical conductivity	 | 	How strongly a given material opposes the flow of electric current.
 
## Hardware

### Full board 

<div style="text-align:center"><img src ="https://i.imgur.com/gQavZqU.png"/></div>


#### BOM

![PCB image](https://i.imgur.com/OWFIXiL.png)

| PCB name                                   | value      | 
| :--------:                                 |:--------:  |
| C1, C2, C5, C7, C8, C11, C13, C14, C17     | 10 µF     |
| C3, C4, C6, C9, C10, C12, C15, C16, C18    | 0.1µF       |
| R1-R3, R8-R10, R13-R15                     | 1.5kΩ      |
| R4-R7, R11-R12, R16-R21                    | 4.7kΩ      |
| ADM1-ADM3                                  | ADM3260    |
| DS2482S-100                                | DS2482S-100|
| I2C CONN            | Grove - Universal 4 pin connector |
| PH GTR / PH VPP                        | EZO pH circuit |
| EC GTR / EC VPP               | EZO conductivity circuit|
| DO GTR / DO VPP         | EZO  dissolved oxygen circuit |
| pH BNC, EC BNC, DO BNC        | pre-assembled female BNC|
| Water T | 3 pins terminal block, DS18B20 |

The sensors used came from [Atlas Scientific](https://www.atlas-scientific.com) but other analog sensors with BNC connection can be used.

In order to display locally the values of the differents sensors, a OLED screen from [Grove](https://www.seeedstudio.com/Grove-OLED-Display-1.12%22-p-824.html) can be added.
<div style="text-align:center"><img src ="https://i.imgur.com/YThjRUK.gif)"/></div>



###  Light board

If you are not interested in monitoring the pH, EC, DO, you can use only the water temperature sensor and / or the OLED screen with the smart citizen.

<div style="text-align:center"><img src ="https://i.imgur.com/KfpNZAj.png"/></div>

### The enclosure

<div style="text-align:center"><img src ="https://i.imgur.com/aowaWtl.png" /></div>

The enclosure of the monitoring board and the smart citizen have been designed on Onshape, you can either download the STL files or copy the project to your onshape account and modify them as you wish : [The Onshape documents of the monitoring case](https://cad.onshape.com/documents/50f1112a541136a65bec4a67/w/db735112a72871fb7c20053e/e/57e22425fb47d5e8030621de)

<div style="text-align:center"><img src ="https://i.imgur.com/tXNBC5e.png" /></div>


We have also designed a probe holder if you want to hold your probes on the side of you fish tank : [The Onshape document of the probes holder](https://cad.onshape.com/documents/8977ef824f45a910c0b8beaa/w/7ac458735dae629f0a5a73cd/e/be59d435418832bfe5f78afb)

![](https://i.imgur.com/6sM3sCY.jpg)


## The firmware

The Smart Citizen firmware has the support for the monitoring board built-in. To enable the sensors you just need to plug you board to the Smart Citizen kit aux port and reboot the Smart Citizen Kit and the sensors will be handled by the board and start to publish to the [web interface](https://smartcitizen.me/kits/).

## How to calibrate the sensors

For now in order to calibrate the sensors you will need to do use the command line interface. 

### The pH sensor

format of the command line

~~~
control atlas ph com,[point],[pH value at current temperature]
~~~

The pH value at current temperature can be found on the reference table on the calibration solution bottle. If the current temperature is not on it, use the closest value.

#### The 3 points calibration

First start a serial communication with the Smart Citizen Kit with `screen` or `pio device monitor`or even the serial monitor of the Arduino IDE.

Order of the calibration : 

1. mid point
2. low point
3. high point

***important ! :*** Always calibrate the mid point first because it calibration erase all the previous calibration done.

**Always clean the probe with distilled water between each calibration**

* **The mid point calibration :** Put the sensor in the pH 7 calibration solution and run the command below :

~~~
control atlas ph com cal,mid,[value of pH at current temperature]
~~~

<span style="text-decoration:underline">example at 30°C :</span> 

~~~
control atlas ph com cal,mid,6.99 
~~~

* **The low point calibration :** Put the sensor in the pH 4 calibration solution and run the command below :

~~~
control atlas ph com cal,low,[value of pH at current temperature]
~~~

* **The high point calibration :** Put the sensor in the pH 10 calibration solution and run the command below :

~~~
control atlas ph com cal,high,[value of pH at current temperature]
~~~

***Note :***  *(not tested)* If your calibration solutions are not 4, 7 and 10, you can still use them and replace `[value of pH at current temperature]` by your values.

### The EC Sensor

#### The 2 points calibration

Order of the calibration :

1. dry point
2. high point

* **The dry point calibration :** Check that the sensor is dry and run the command below :

~~~
control atlas ec com cal,dry
~~~

* **The high point calibration :** Put the sensor in the high point calibration solution (12,880 µS/cm) and run the command below :

~~~
control atlas ec com cal,high,[value of EC at current temperature]
~~~ 

<span style="text-decoration:underline">example at 30°C :</span> 

~~~
control atlas ec set cal,high,14,120 
~~~

***Important ! :*** Do not forget the `,` between the hundreds and the thousands or else the calibration will not occur !

***Note :***  *(not tested)* If your calibration solution is not 12880 µS/cm, you can use another one and replace `[value of pH at current temperature]` by your value of electroconducivity.

## The DO Sensor

### The 2 points calibration

Order of the calibration 

1. dry point
2. 0 mg/L point (optional)


* **The dry point calibration :** Check that the sensor is dry and run the command below :

~~~
control atlas do com cal
~~~

* **The 0mg/L point calibration :** Put the sensor in the 0mg/L calibration solution and run the command below :

~~~
control atlas do com cal,0
~~~

## Deployment


![](https://i.imgur.com/2EwPJJc.jpg)
![](https://i.imgur.com/2IHsDWq.jpg)
![](https://i.imgur.com/6w2y12F.jpg)


### Atlas-Scientific 

* [Atlas pH datasheet](https://www.atlas-scientific.com/_files/_datasheets/_circuit/pH_EZO_datasheet.pdf)
* [Atlas EC datasheet](https://www.atlas-scientific.com/_files/_datasheets/_circuit/EC_EZO_Datasheet.pdf)
* [Atlas DO datasheet](https://www.atlas-scientific.com/_files/_datasheets/_circuit/DO_EZO_Datasheet.pdf)


