# Grove water sensor
A Python script to read data from the Grove water level sensor.

Grove's official website mentions only the use of an Arduino, thus the scripts are all in C++. 
All I do here is convert the scripts to Python and adapt them to the Rapsberry Pi Pico W. You can use the data coming out of the Grove and send over MQTT for actual monitoring. 

About the Grove:
"The Grove Water Level Sensor is a very accurate sensor that can be helpful in water level sensing applications. It is completely waterproof and uses capacitive pads to detect water levels up to 10cm."

It uses I2C bus to connect to the rpipicow. You need 4 Pins: 1 powerline (5V or 3V3), 1 ground, 1 SDA, 1 SCL. The SDA and SCL connect on bus 0 on the pico - GPIO 0 and GPIO 1. You don't need to use bus 0 nor GPIO pins 0 and 1, it's just what I used. You can check the Pico pinout to see which bus is connected to which pin. 


The script is based on MicroPython. 
- Install MicroPython to your rpipicow either manually or through Thonny.
- Open the script in your favorite IDE that can connect to the rpipicow.
- Run a couple of tests to make sure everything works. (I would recommend starts the script while the sensor is dry, and then dip it in water)
- Adjust the script to your likings (eg, adding a MQTT client)
- rename the script to main.py and copy paste to the Pico (make sure you copy it over in execute mode and NOT bootloader mode).  


