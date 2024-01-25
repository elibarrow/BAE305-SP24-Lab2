# Lab Report 2: For Good Measure: Basic Circuits
Eli Barrow & Isaac Stevens      
Jan. 25, 2024

## Summary of Lab ##
There were multiple goals of this lab, the most important goals were to learn how to solder and analyze circuits to further understand KVL and KCL. The work performed in this lab was very intriguing and it allowed us to stay focused on the bigger picture of the lab and what we were trying to accomplish. The soldering was a fun addition to the lab where we got to do some hands-on building rather than just aimlessly taking different measurements. At the end of the lab, it was easily seen that our group benefited greatly from the material presented, mostly because all of the topics we had only worked with conceptually and not had any hands-on experience with.

## Lab Schematics and Procedure
For Lab 2, the following materials are required:

•	A Digital Multimeter

•	A DC Power supply

•	A Soldering station

•	A small piece of solder

•	Resistors: 1kΩ, 2.2 kΩ, 5.1 kΩ, 4.7 kΩ, 6.8 kΩ, 15 kΩ, 220 kΩ

•	Soldering Breadboard (In our case, a DigiKey SolderFul BreadBoard)


Begin by turning on the soldering station to 400 °C and give it time to reach the designated temperature. Make sure the tip is in proper condition and if not either replace the tip or tin the tip if necessary.

Below is a picture of the soldering station our group used in class.

[<img src="https://github.com/elibarrow/BAE305-SP24-Lab2/blob/main/Soldering%20Station.jpg" width="1920" height="1080">]

![Soldering Station](https://github.com/elibarrow/BAE305-SP24-Lab2/blob/main/Soldering%20Station.jpg)

Grab the soldering breadboard and create the following circuit with the resistors in the same order as shown:

<p align="center">
  <img src="https://github.com/elibarrow/BAE305-SP24-Lab2/blob/main/Series%20Circuit%20Schematic.png">
</p>
![Series Circuit Schematic](https://github.com/elibarrow/BAE305-SP24-Lab2/blob/main/Series%20Circuit%20Schematic.png)


## Lab Assignment Specific Items ##

### Objective 1: Learn soldering techniques by building a simple circuit on a solder breadboard ###

#### Part 1 - Series Circuit


### Objective 2: Analyze a circuit to verify Kirchhoff’s voltage law (KVL) and Kirchhoff’s current law (KCL), and to apply Thevenin’s and superposition theorems to the analysis of electrical circuits. ###

#### Part 1 - Series Circuit

**Picture Here**

Using the DMM we measured the voltage drop across each resistor along with the current that is present in the circuit.
The results are shown in the table below.

|Type|Measured|
|---|---|
|Voltage Drop|  $R_1$ = 1.2V  |
|Voltage Drop|  $R_2$ = 2.675V  |
|Voltage Drop|  $R_3$= 6.125V  |
|Current|  I = 1.21mA |



#### Part 2 - Parallel Circuit
**Picture Here**    

Using the DMM we measured the voltage ($V_L$) drop across $R_5$ and measured the current ($I_L$) through $R_5$.
The results are shown in the table below

||Measured|
|---|---|
|$V_L$ (Voltage acrros $R_L$ / $R_5$)|  3.565 V  |
|$I_L$ (Current through $R_L$ / $R_5$)|  1.64 mA  |

**Picture Here of Step 5**

Using the DMM we measured the currents $I_1$, $I_2$, $I_3$ without $R_5$ in the circuit.   
|Current |Measured| Calculated|
|---|---|---|
|$I_1$ (For $R_1$) | 0.50 mA | |
|$I_2$ (For $R_2$) | 0.46 mA | |
|$I_3$ (For $R_3$) | 0.04 mA | |


#### Part 2.2 - KVL

This step begins with $R_5$ still removed from the circuit.   
Using the DMM we measured the voltage drop across all the resistors.


|Voltage |Measured Mag.| Calculated Voltages|
|---|---|---|
|$V_1$ |2.292 V | |
|$V_2$  | 3.026V | |
|$V_3$ | 6.686 V | |
|$V_4$ (same as $V_5$) | 9.70 V | |

**Discussion Question 1: How much power does each resistor dissipate? Each branch? Total power? Is the power in equal to the power out?**


#### Part 2.3 - Thevenin
Thevenin’s Theorem states that all linear circuits, regardless of the number of components, can be expressed as a circuit with one equivalent voltage source and one equivalent resistance. 

The original circuit that we were given is shown below:
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab2/blob/main/Screenshot%202024-01-23%20at%201.36.04%20PM.png width=50%>
</p>

The first step in the Thevenin process is to remove the load in the circuit. In this case, the load was $R_5$. The updated circuit is shown below: 
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab2/blob/main/Screenshot%202024-01-23%20at%201.36.39%20PM.png width=50%>
</p>


We then simplified the circuit to increase the ease of calculating our values $R_T$, $V_T$, $I_N$, $V_L$, and $I_L$. The updated circuit is shown below:  

<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab2/blob/main/Screenshot%202024-01-23%20at%201.38.17%20PM.png width=50%>
</p>


We then calculated $R_T$, $V_T$, $I_N$, $V_L$ and $I_L$ using the previously measured values for $R_1$, $R_2$, $R_3$, and $R_4$. Using nodal analysis we were able to calculate $V_T$.
||Calculated|
|---|---|
|$R_T $|3.800 k&Omega;|
|$V_T$|9.701 V|
|$I_N$|2.553 mA|
|$I_L$ |1.617 mA|
|$V_L$ |6.145 V|



**Discussion Question 2: Does $I_T$ = $I_L$?**

In this circuit that we were given the way that $I_T$ would be calculated would be to insert the load resistor back into the circuit, and then calculate the current running through the load by using Ohm's law using the Thevenin voltage and load resistor value. This would give you the Thevenin current, in the lab questions we were asked to calculate $I_L$ as well, and the previous steps listed above are what procedure was followed to get the value for $I_L$. So the answer to this discussion question is YES, $I_T$ = $I_L$.



