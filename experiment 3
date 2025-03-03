
### **Differential Amplifier**

A differential amplifier is a key circuit in analog electronics that amplifies the difference between two input signals while rejecting common-mode signals (noise). It is widely used in operational amplifiers (op-amps), instrumentation amplifiers, and analog circuits.
A basic MOSFET differential amplifier consists of:

Two matched MOSFETs (M1 and M2) forming a differential pair

A current source I<sub>SS</sub> as a tail current

Two drain resistors R<sub>D</sub>

When the inputs V<sub>in1</sub> and V<sub>in2</sub> are equal, the circuit is balanced, and the current splits equally.

When V<sub>in1</sub> increases while V<sub>in2</sub> decreases, M1 conducts more current, and M2 conducts less, creating a voltage difference at the outputs.

The circuit rejects common-mode signals (same voltage at both inputs) and only amplifies the differential component

### **question:**

**V<sub>DD</sub>=3.3 V , p<=3 mW , V<sub>ICM</sub>=1.65 V, V<sub>ocm</sub>=1.7 V , V<sub>P</sub>=0.5 V**

**Circuit 1** <br>

![ci](https://github.com/user-attachments/assets/fcbc06b1-b816-4f9f-a97c-0958f0cc0b90)

**Step 1:Dc analysis design Rd and Rss**
C:\Users\laksh\OneDrive\Pictures\Screenshots 1\Screenshot 2025-03-03 121648.png


from the calculation we have finded I<sub>SS</sub>value as 0.909 mA <br>
I<sub>D1</sub> and I<sub>D2</sub> as 0.45 mA <br>
R<sub>D</sub> as 3.5 kohm <br>
R<sub>SS</sub> as 550 ohm <br>
V<sub>GS</sub>=V<sub>G</sub> - V<sub>p</sub> = 1.65 V - 0.5 V = 1.15 v <br>
V<sub>OV</sub> = V<sub>GS</sub> - V<sub>th</sub> = 1.15 V - 0.366 V = 0.784 V <br>

### **DC Analysis**

To set the operating point go to Configure Analysis and select Dc operating Point <br>

![dc2](https://github.com/user-attachments/assets/f76e42bb-74e2-496f-b76f-efc2412a4067)

to set correct operating point vary width and length values 
width = 208 u <br>
length = 6 u <br>


### **Analysis**

### Effect of VICM on Vout and VP

| **Common-Mode Input Voltage (V_ICM)** | **Output Voltage (V_out)** | **Voltage at Point P (V_P)** |
|--------------------------------------|--------------------------|--------------------------|
| **1.65V**                            | **1.70V**             | **0.5V**                |
| **1.3V**                            | **1.62V**                 | **0.59V**               |



As the common-mode input voltage \( VICM \) increases, the source voltage \( VP \) also increases, causing a shift in the operating point. This leads to a higher drain current, resulting in a greater voltage drop across \( RD \), which reduces \( Vout \).

### **Calculate Gain**

![image](https://github.com/user-attachments/assets/fd9ae479-071b-4594-b645-595a6984d270)


### **Calculate maximum input and output Swing**

![image](https://github.com/user-attachments/assets/f7a39423-0de0-439c-b98a-217d4620e004)


### **TRANSIENT ANALYSIS**
go to configure Analysis and select transient analysis then <br>
stop time as 1m ,time to start saving data as 0 <br>

• Waveform Type: Sine Wave
• DC Offset: 1.65 V
• Amplitude: 25 mV
• Frequency: 1 kHz

put the same values for V2 but change the phase angle.

And in V2 phi(deg) as 180

![image](https://github.com/user-attachments/assets/5f94dcd4-4c40-4ab4-93b0-b64ba6fabf10)

when the input voltage is more then the minimum swing or outside the allowable swing the output wave form deforms, ie it is in triode or cutoff region.

![diform](https://github.com/user-attachments/assets/afb2f26a-64ab-4c48-8c14-043b88c2a829)


### **AC Analysis**
• Type of sweep: Decade
• Number of points per decade: 10
• Start frequency: 0.1 Hz
• Stop frequency: 1 THz
AC Amplitude as 1 and AC Phase as 0 in V1 <br>
AC Amplitude as 1 and AC Phase as 180 in V2 <br>

![Screenshot 2025-03-02 220006](https://github.com/user-attachments/assets/ecfef7ef-22da-4aa5-93b4-74fba38dd18f)


### **Circuit 2** <br>

Replace the resistor with a current source=0.909mA. 

![image](https://github.com/user-attachments/assets/8203f89b-7990-4a8f-b090-9d715e7e6222)

### **DC Analysis**
![dc22](https://github.com/user-attachments/assets/ef1b0399-b421-40f2-973c-93915db96652)

### **TRANSEINT ANALYSIS**

![trans22](https://github.com/user-attachments/assets/b0262198-ccbb-4889-900c-58d6f15b76f6)

if Vin is more then the allowable swing.

![diform2](https://github.com/user-attachments/assets/409afb66-cbe0-4cf0-87f9-f32b815679fc)

### **AC ANALYSIS**

![Screenshot 2025-03-02 223315](https://github.com/user-attachments/assets/d0db6eb8-ab1e-4649-bf22-f65bace10bb8)

### **Circuit 3** <br>

Replace current Source with N-Channel MOSFET .

![image](https://github.com/user-attachments/assets/64a7f151-768e-4660-8494-d1c5031e9794)

V<sub>b</sub> should be less than V<sub>p</sub> as the drain voltage of MOSFET M3 is V<sub>p</sub>

and the V<sub>b</sub> should be greater than the V<sub>th</sub> , therefore the value of V<sub>b</sub> should be between 0.366 V and 0.5V.

### **DC Analysis**

set the operating point of M3 such that It is in saturation state.
V<sub>b</sub>=4 V

![image](https://github.com/user-attachments/assets/ce005922-5206-46ac-b060-955c431dadd9)

### **TRANSIENT ANALYSIS**

![image](https://github.com/user-attachments/assets/962d3337-ddcc-4651-9ba6-2586c9642cc8)

if vin is more then

![diform222](https://github.com/user-attachments/assets/9a288f53-8a88-4ae2-bc8e-c97f61d497d3)


### **AC Analysis**


![Screenshot 2025-03-02 223315](https://github.com/user-attachments/assets/d0db6eb8-ab1e-4649-bf22-f65bace10bb8)


### ""Result and Inference""

V<sub>DD</sub>=3.3 V

V<sub>p</sub>=0.5 V

V<sub>ICM</sub>=1.65 V 

V<sub>OCM</sub>=1.7 V

R<sub>D</sub>=3.5 kohm

R<sub>SS</sub>=550 ohm

I<sub>SS</sub>=0.909 mA

I<sub>D</sub>=0.45 mA

1. When V<sub>ICM</sub> changes there is a change in the output voltage and Drain current.

2. If the input voltage is more then the minimum swing or outside the allowable swing the output wave form deforms, ie it is in triode or cutoff region.

3. If R<sub>D</sub> value changes there will be a change in the output voltage,by selecting the resistance wecan control the output voltage.

4. V<sub>b</sub> should be less than V<sub>p</sub> as the drain voltage of MOSFET M3 is V<sub>p</sub>
and the V<sub>b</sub> should be greater than the V<sub>th</sub> .















































 
