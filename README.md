# LIC-1
# Experiment-1
## Aim:
To do the DC analysis,Transient and AC analysis of a CS amplifier circuit and 
extract the various parameters associated using LT Spice.
## Components required: 
Mosfet(nmos4 ,pmos4 ), Resistor(22k), voltage supply(1.8V,0.9V) and connecting wires.
## CIRCUIT DIAGRAM
![Screenshot 2025-02-17 230111](https://github.com/user-attachments/assets/80157130-46cd-43d2-8e9f-16981da155b2)
## Theory:
Mostfet is one of the most important compontent in electronics .

This importance is due to the fact of its compact design , low power consumption ,simple geometry and compatibilty in VLSI technology.\
There are three different configurations in which the mosfet can be connected (namely common drain,gate and source) the most popular being common source and common drain configurations.

The Mosfet acts as an amplifier in the saturation region of operation where Vgs > Vth,Vgd < Vth and Vds>=Vov for an N channel mosfet.
In the common source configuration there is a 180 degree phase shift between input and output. \
_There is very high input impedance (Ig=0) ideally infinite._

The drain current

**I<sub>d</sub> = 1/2 k<sub>n</sub> V<sub>ov</sub><sup>2</sup>** ; **V<sub>ov</sub>=V<sub>gs</sub>-V<sub>th</sub>** and **k<sub>n</sub>=u<sub>n</sub> C<sub>ox</sub> W/L**

Output is taken from the drain end rather than simply across the resistor to maintain the common ground referance.
### DC Analysis:
This is done ensure the mosfet operates in saturation and to calculate the DC operationg point of the transistor. This prevents signal distortion .\
This helps in the determination of the biasing resistors.\
This helps in getting a correct operating point despite the fluctuation in the other parameters.
![Screenshot 2025-02-17 225616](https://github.com/user-attachments/assets/9f0d6655-8f39-4e63-a2c1-9b3e0114dcf5)
### AC Analysis:
This is nothing but the small signal analysis of the circuit.This is done to determine the Gain of the amplifier circuit .\
This also helps to analyze the Frequency Reponse of the amplifier circuit.
the gain is given by **A<sub>v</sub> = -g<sub>m</sub> R<sub>d</sub>**
![Screenshot 2025-02-17 230029](https://github.com/user-attachments/assets/dfb4b64f-fcdc-4496-bf0a-c4f4ae1b683f)

### Transient Analysis:
This to done to analyse the response of the circuit to time varying signals. 

This is helpful to determine the signl distorton, DC shift between the input and the output.
This plays key role in detecting issues like phase distortion.This is essential for high speed applications like communication systems.
![Screenshot 2025-02-17 225918](https://github.com/user-attachments/assets/1fbb0fce-e49a-4a46-838c-d5f381f7d019)
## Procedure:
1.Create a new folder and name it as project file.Save the LT spice file in this folder.

2.Name the mosfet as CMOSN and the length as 180nm and width as 3um initially.

3.For the pmos name it as CMOSP and set the length as 180nm and width as 3um respectively

4.**DC Analysis:** Set up the circuit as per the circuit diagram with proper connections ensuring valid circuit for further analysis.
Apply the DC voltage of Vdd=1.8V and Vgs = 0.9 V . Go to simulate option in the tab and edit simulation command, click on DC analysis and press ok.(.op)
Click on Run in the tab menu to get the DC operating point ,Vout and Id.

5.**Transient Analysis:** Apply a sine wave input of Vgs=0.9V with an amplitude of 50mV and frequency of 1kHz by going to advanced menu in the voltage setting option.go to simulate option in tab ,edit simulation command 
, click on transient analysis and give the stop time as 3m and click ok.(.tran 3m) Now Run to visualise the response of the circuit to a time varying signal.

6.**AC Analysis:** Go to spice directive and give the library file path for the simulator to access the data through the path . Go to simulate option in the tab , edit simulation command , click on AC analysis 
and mention the time of sweep as decade , no of points as 20 and frequency as .1Hz to 1THzand click on ok.Now Run to analyze the gain and frequency response of the circuit.(.ac dec 20 .1 1T)
# Calculation :
Power = 180um

Loop Equation: V<sub>dd</sub>=V<sub>ds</sub>+I<sub>d</sub>*R<sub>d</sub>

P=I*V (I<sub>d</sub>=55.52 uA , V<sub>dd</sub>=1.8V)

clearly V<sub>ds</sub>=V<sub>out</sub>; V<sub>ds</sub>>=V<sub>gs</sub>-V<sub>th</sub>

R<sub>d</sub> (upon calculation) =1K

Widhth=0.1um(Vary width to get the current)

V<sub>ds</sub>=1.7447

gain=-17db(from AC analysis)

Q point is (0.552,55.52uA)
## Inference:
1. Current is directly Propotional to the Width of the Mosfet and the current varies with the change in width.

2. Mosfet saturation ensures the mosfet works as an amplifier and produces the desired negative gain as per the equation Av=-gm*Rd.

3. Q point stability is attained in saturation region thus helping in attaining linear amplification .

4. The Mosfet gain is increased in mid band frequency range (small signal analysis).

5. The Transient analysis reveleas the response of the circuit to time domain ssignal and determines how quickly the circuit responds to variation.\
This is essential in high speed applications.

6.AC Analysis helps in designing circuits with desired gain and helps in impedance matching.\
Also helps in understanding the frequency response and small signal behaviour of the circuit.









