# TEMPERATURE-MONITORING-SYSTEM
MENTOR NAME : NEELA SANTHOSH 
DOMAIN : EMBEDDED SYSTEMS 
INTERN ID: CT04DY586

TASK DESCRIPTION:

The task presented here is to design and implement a simple yet efficient temperature monitoring system using an Arduino
microcontroller, an LM35 temperature sensor, and a 16x2 Liquid Crystal Display (LCD) with I2C interface. The primary
objective of this project is to continuously measure the surrounding temperature and display the values on the LCD in
degrees Celsius, allowing users to observe changes in real-time.

At the beginning of the operation, the LCD is initialized by the Arduino and displays a startup message, which provides
visual confirmation that the system is functioning correctly. After initialization, the microcontroller repeatedly reads
the sensor data, performs necessary calculations, and updates the LCD with the latest temperature reading every two
seconds. This cyclic process makes the system dynamic and highly responsive to environmental changes.

The LCD used here operates on the I2C protocol, which reduces wiring complexity by requiring only two data lines (SDA and
SCL) to communicate with the microcontroller. This is a major advantage when compared to traditional parallel LCDs, as it
simplifies connections and improves reliability in compact circuits. The 16x2 configuration of the LCD allows for clear
and easy-to-read text output, displaying both the label (e.g., “Temp:”) and the measured temperature value with the unit
(°C).
The LM35 sensor, being a precision integrated circuit temperature sensor, provides an analog voltage output that is
linearly proportional to the temperature. This makes it an ideal choice for such applications because it offers
simplicity in interfacing, accuracy in measurements, and the ability to operate without extensive calibration. The
Arduino serves as the central processing unit, converting the raw sensor data into meaningful temperature readings using
its built-in analog-to-digital converter (ADC).

This task not only demonstrates the concept of sensor interfacing but also highlights important aspects of embedded
systems such as signal acquisition, data processing, digital conversion, and user interaction through display units. By
integrating the hardware and software components, this project shows how basic electronic elements can be combined into a
working system capable of solving a real-world problem like temperature monitoring.


Working Principle

The working principle of this system is based on the conversion of temperature into an electrical signal by the LM35
sensor, followed by processing of the signal using the Arduino microcontroller, and finally displaying the result on an
LCD module.

The LM35 temperature sensor is designed to provide a voltage output directly proportional to the surrounding temperature.
For every degree Celsius increase in temperature, the sensor outputs approximately 10 millivolts (mV). For example, if
the temperature is 30 °C, the output from the LM35 will be around 300 mV. This analog voltage is then fed into the
Arduino’s analog input pin (A0 in this case).

The calculated temperature is then sent to the LCD via the I2C interface. The I2C LCD requires only two communication
lines—Serial Data (SDA) and Serial Clock (SCL)—which makes it compact and efficient. The lcd.print() function is used to
display text and numerical values, so the user can clearly see the label "Temp:" followed by the actual temperature value
and the unit “C”.

The system is programmed to update the display every two seconds, which allows it to react to changes in temperature
while avoiding excessive flickering of the LCD. This refresh rate balances accuracy with readability. If the environment
gets warmer or cooler, the LM35 immediately responds with a new voltage, which is detected by the Arduino, processed, and
then displayed.

In essence, the working principle combines three stages: sensing, processing, and displaying. The LM35 acts as the
sensing element, the Arduino performs the processing through ADC and mathematical conversion, and the LCD serves as the
human–machine interface for displaying the information. Together, these components form a simple but powerful system that
demonstrates the basics of real-time embedded applications.
