# Energy-Analysis-of-a-Home
This is a detailed analysis of all the energy consumed, and inside and outside temperatures of a house in Canada. The data is from a private home, from 2016 up till 2019, and has readings up to minute interval.
The house has a Gas furnace. Through MySQL the analysis here is majorly focused on the “Time of use” feature of the utility which pre-determines the “on peak” and “off peak” energy rates.
Based on the "Time of usage" rates as well as the outside weather, this study proved useful in conserving energy and minimizing overheating/overcooling of the house.
The electricity production is through a 5kW PV installation, these measurements can also be used to calculate the sun radiation each minute. The azimuth of the panels is 200° (S-SW) and the slope is 50°. The latitude of the house is 50.6.

The dataset contains 3 types of metrics:

T_* : temperature readings (° celcius)
M_*: energy consumption and production
F_*: on/off flag
These are the entries

T_bathroom: temperature in the bathroom, located first floor, N oriented
T_storage: located ground floor, blind walls
T_outside: outside temperature. NOTE: sensor has direct sunlight in the morning
T_desk: located first floor, S oriented and large window
T_kitchen: located ground floor, S oriented and large window
T_living: located ground floor, N-W oriented, open space with kitchen
T_bedroom1: first floor, S oriented
T_bedroom2: first floor, W oriented
T_bedroom3: first floor, N oriented
Meleccons: total electricity consumed in kWh
Melecprod: total electricity produced in kWh
M_water: total water consumed in m³
M_gas: total gas consumed in 0.1 m³*
Fheatingdownstairs: 1 means the pump of the central heating is on, 0 means it is off
Fheatingupstairs: 1 means the pump of the central heating is on, 0 means it is off
*gas metrics: a reading of eg 70.000 means 7.000 m³ gas consumed
To calculate the kWh from the metric cube, use the following coefficients:

2016: 10.11
2017: 10.1720
2018: 11.1410
2019: 11.3075
Eg: in 2019, 600m³ equals 6784,5 kWh
