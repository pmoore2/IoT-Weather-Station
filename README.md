# IoT-Weather-Station
I created a weather station using IoT devices, including a Raspberry Pi 3, ESP8266 NodeMCU microcontroller, and DHT11, BMP280, and CCS811 sensors. I was motivated to do this project to create my first embedded system and leverage IoT devices to collect and transmit weather data over the MQTT protocol. The final breadboard of the weather station, showing the hardware and wiring, is shown in the image below.

![alt text](https://github.com/pmoore2/IoT-Weather-Station/blob/main/images/Picture1.png "Breadboard")

The weather station uses an ESP8266 NodeMCU as the publisher, equipped with a DHT11 sensor to measure temperature and humidity, a BMP280 sensor to measure pressure, and a CCS811 sensor to measure air quality. The Raspberry Pi 3 hosts the Mosquitto MQTT broker and Node-RED. The Arduino sketch in `ES_project.ino` file is the program that the ESP8266 board runs to read the temperature values from the sensors. Node-RED is a programming tool that connects nodes in a flow diagram for event-driven applications. I used Node-RED for this project to create the UI application and display the values that the sensor reads. The two images below show the MQTT server running on the Raspberry Pi 3 and the final UI application created with Node-RED, with sample temperature readings from the weather station.

![alt text](https://github.com/pmoore2/IoT-Weather-Station/blob/main/images/Picture3.png "MQTT Mosquitto Broker")
![alt text](https://github.com/pmoore2/IoT-Weather-Station/blob/main/images/Picture2.png "Node-RED UI Application")

This project taught me how to create an embedded system and use it in an MQTT network. I also read this paper1 to learn more about the MQTT protocol. MQTT is a lightweight protocol and is very flexible, making it ideal for developers creating IoT applications. However, the protocol has some security limitations, such as a lack of native encryption, which leaves data vulnerable to interception. The project provided hands-on experience with Arduino sketches, IoT hardware, and MQTT's publisher-subscriber model. Future work includes adding email notifications when certain temperature thresholds are met, exploring security vulnerabilities, and making the application more secure.

### References

[^1]: S. Andy, B. Rahardjo, and B. Hanindhito, "Attack Scenarios and Security Analysis of MQTT Communication Protocol in IoT System," *Proc. EECSI 2017*, Yogyakarta, Indonesia, 19-21 Sept. 2017