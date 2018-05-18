# MiniEIS

The MiniEIS is an engine parameter monitoring tool designed for the Rotax 912 series engines.

The instrument is extremely compact and economical, using off-the-shelf components
extremely economical and reliable.

The instrument uses, when possible, the standard motor sensors. Additional sensors exist as an option.

The parameters are shown on a backlit LCD display with 4 lines and 20 characters.

The instrument generates alarms in case one of the critical parameters goes out of minimum or maximum margins. The out-of-margin parameter flashes on the display.

It is possible to generate visual and sound alarms of different types.

There is a function that cancels the audible / visual alarm until another alarm is generated. 

The out-of-bound parameter continues to flash on the display even when the alarm is canceled.

The instrument will monitor the following parameters and generate alarms if necessary.

- RPM
- cylinder head temperature 1 and 2
- oil temperature
- oil pressure
- supply voltage

it is possible to monitor the following parameters, installing the appropriate sensors:

- fuel pressure
- MAP
- air temperature.

The fuel pressure parameter generates an alarm if the pressure goes out of standard margins.

The minimum and maximum values of the various parameters that generate alarms are set
by firmware and can be customized on request. No initial settings are required.

The current version of the instrument is able to monitor the oil pressure using the old style
pressure switch. The new style pressure switch (4-20mA) will be implemented soon.

There is an optional battery that allows operation even in the absence of external power
supply. In this case, some sensors will cease to function.

The instrument connects to sensors, displays, power supply, etc. via a DB25 connector.
The 25 pins of the connector have the following functions:

1 - connection to the engine speed pickup.<br/>
2 - if grounded, reset the MiniEIS processor<br/>
3 - if grounded, cancels the visual / audible alarm<br/>
4 - 5V output for audible / visual alarm, maximum 20mA absorption (led and piezo buzzer).<br/>
5 - 5V output for audible / visual alarm, maximum 20mA absorption (led and piezo buzzer).<br/>
6 - SCL (data bus for connection to sensors and displays)<br/>
7 - SDA (data bus for connection to sensors and displays)<br/>
8 - optional sensor input temperature and air humidity DHT22 sensor<br/>
9 - optional petrol pressure sensor input<br/>
10 - connection to oil pressure sensor<br/>
11 - connection to oil temperature sensor<br/>
12 - connection to temperature sensor tested 1<br/>
13 - connection to the tested temperature sensor 2<br/>
14 - mass for visual / audible alarm, max 4A.<br/>
16 - NC<br/>
17 - NC<br/>
18 - NC<br/>
19 - NC<br/>
20 - general mass<br/>
21 - general mass<br/>
22 - regulated output 5V max 100mA (to be used for display and sensor power supply)<br/>
23 - regulated output 5V max 100mA (to be used for display and sensor power supply)<br/>
24 - input + 12V<br/>
25 - input + 12V<br/>

The temperature and air pressure sensor can be installed in the airbox to monitor possible
conditions of icing of the carburetor. The sensor must be powered by the regulated 5V coming
from feet 22-23. The DATA foot must be connected to pin 8 of the MiniEIS.

The fuel pressure sensor must be installed on the fuel circuit upstream of the carburettors
and must be connected as shown in the diagram. The sensor has a 1/8 NPT thread.

The optional absolute inlet manifold pressure sensor (MAP) must be connected to the intake
manifolds using a 6mm tube and connected to the MiniEIS as shown in the diagram.

These sensors must be enabled on the Firmware, the simple electrical connection does not
produce any reading on the instrument.

The 4x20 display must be installed on the panel and the 4 wires must be connected to the MiniEIS as
follows:<br/>
GND to ground<br/>
VCC to + 5V adjusted MiniEIS (pins 22-23)<br/>
SCL to pin 6 of the MiniEIS<br/>
SDA DB25 connector to pin 7 of MiniEIS DB25 connector

The potentiometer adjusts the contrast of the display.

The sound / visual alarm cancel button can be installed in any position using a common pushbutton switch.

It is recommended to install at least one red LED with high visibility to pin 4 or 5. A resistor of
suitable value must be installed in series with the LED positive. For red 5mm LEDs, a 330 ohm resistor is recommended. The LED positive must be connected to pin 4 or 5 of the MiniEIS, with the resistance inserted in series, the mass of the LED must be connected to ground.

Alarm activation thresholds:

laps: more than 5800<br/>
head temperature: more than 145 degrees<br/>
oil pressure: less than 1.5 and more than 7.0<br/>
bar oil temperature: more than 130 degrees<br/>
fuel pressure: less than 2 and more than 7<br/>
PSI voltage: less than 11.5 and more than 15 volts<br/>
Operating voltage: from 7 to 15 Volts.<br/>
Current: 150 mA maximum

Wiring diagram of the connections
numbering pins connector side cables, seen from behind
