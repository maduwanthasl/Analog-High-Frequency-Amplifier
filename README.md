# High Frequency Amplifier 🎛️

## Introduction 📚
An amplifier is an electronic device that can increase the power of a signal (a time-varying voltage or current). Depending on its frequency of operation, we have several types of amplifiers. As the name suggests, high-frequency amplifiers are designed to operate at high frequencies. These have a vast variety of applications like telecommunication, high-speed electronic measurements, laser research, and photonic research. When designing a high-frequency amplifier, factors like bandwidth, low noise, high gain, and noise immunity are extremely important. This project aims to build a high-frequency amplifier using transistors which can drive a headphone.

## Requirements/Outcomes 📋
- Design a high-frequency amplifier which can drive a load impedance of 8Ω (headphone).
- The design must be compatible with working at 12V.
- The design must be able to amplify a sine wave of 0.1V (peak-peak voltage).
- The design must work in the frequency range of 20 kHz – 100 kHz (Bandwidth requirement).
- The design must consist of a minimum of 3 transistors (usage of op-amps is prohibited).
- Apart from the demonstration, a datasheet must be provided for the design.

## Project Details 🔍

### General Guidelines 📝
- Main functionality of the project must be achieved with basic electronic components such as resistors, capacitors, inductors, diodes, transistors, and other analog integrated circuits.
- Using any other pre-built programmable ICs is prohibited.
- Microcontrollers can only be used for user interface operation.
- All circuits must be simulated using software (e.g., Multisim, LTSpice, PLECs, etc.)
- All circuits should be tested on the breadboard and reviewed by the assigned supervisor before moving further.
- Circuits must be designed using professional EDA software (e.g., Altium Designer, OrCAD, etc.)
- Schematics should be verified and evaluated by the assigned supervisor.
- Design for manufacturability should be considered when designing the PCB.
- Complete set of design and manufacturing documents – Schematics, Layout, 3D file, Gerber files, Assembly files, BoM must be generated and properly documented.
- Students are encouraged to procure components from international component distributors (e.g., Mouser, DigiKey, Arrow Electronics, LCSC, etc.)
- Students are encouraged to get the PCBs manufactured from international PCB manufacturers (e.g., JLCPCB, PCBway, etc.)
- Final implementation of the project needs to be done on a PCB.
- Enclosure design must be done using professional software (e.g., SolidWorks).
- Enclosure and 3D model of the circuit must be assembled and inspected before manufacturing.
- 3D printing, Laser cutting, and Sheet metal bending can be used to manufacture the enclosure.
- Students are encouraged to consider the 3D model and PCB co-design (design in parallel by taking their integration into consideration) when designing.

### Design Approach 🛠️
The design utilizes a two-stage amplifier with a cascading setup. In the first stage, a Bipolar Junction Transistor (BJT) is employed in a common emitter configuration. A capacitor is employed to connect this amplifier stage to the next. The second stage involves four Bipolar Junction Transistors arranged in an AB push-pull configuration. 

#### Class A Amplifier Stage 🔍
Class A amplifiers provide full amplification of the input signal and have a simple structure. They are inefficient and generate significant heat, making them unsuitable for high-power amplification needs.

#### Class B Amplifier Stage 🔍
Class B amplifiers conduct only half of the input signal due to biasing. Two of these amplifiers can be configured in a "Push Pull" arrangement where their output signals are combined, reducing power loss but causing slight distortion called zero crossing distortion.

#### Class AB Amplifier Stage 🔍
Class AB amplifiers solve the distortion issue found in class B amplifiers by always keeping the two transistors just inside the active region. This ensures an undistorted output waveform but leads to decreased efficiency compared to class B amplifiers.

#### Voltage Buffer Stage 🔍
To address the issue of insufficient gain in Class AB amplifier stages, voltage buffers using the common collector configuration are incorporated, helping to isolate each transistor in a push-pull amplifier setup.

### Prototype Design 📐
Proteus was used to develop the virtual prototype. The physical prototype's PCB was designed using Altium software. The enclosure was created using SolidWorks, crafted from PLA+ material for effective heat dissipation and prevention of amplifier overheating.

### Schematic Design
![schdoc](https://raw.githubusercontent.com/maduwanthasl/Analog-High-Frequency-Amplifier-V1/main/Schematic%20images/High%20%20Frequncy%20Amplifier%20-%20Schematic%20.png)

### PCB Design

### 2D View
<table>
  <tr>
    <td align="center">
      <strong>Top Layer</strong><br>
      <img src="https://raw.githubusercontent.com/maduwanthasl/Analog-High-Frequency-Amplifier-V1/main/PCB%20images/High%20%20Frequncy%20Amplifier%20-%20PCB%202D%20top%20layer%20.png" alt="top" style="max-width:100%;">
    </td>
    <td align="center">
      <strong>Bottom Layer</strong><br>
      <img src="https://raw.githubusercontent.com/maduwanthasl/Analog-High-Frequency-Amplifier-V1/main/PCB%20images/High%20%20Frequncy%20Amplifier%20-%20PCB%202D%20Bottom%20layer%20.png" alt="bottom" style="max-width:100%;">
    </td>
  </tr>
</table>

## Achieved Results 📊
- Open circuit gain: 21
- Gain with 8Ω load: 16.393
- Bandwidth: 700kHz
- Input Resistance: 2.188 kΩ
- Output Resistance: 8.0108 Ω
- Power Dissipation: 2.4 W

## Team Contributions 👥
- **Hirusha Maduwantha**: PCB design, Component Selection
- **Praveena Dimagi Hennadige**: Enclosure design, Breadboard Implementation
- **Praveen Chalanamini Dissanayaka**: Enclosure design, Soldering PCB, Breadboard Implementation
- **Dilshan N.L.**: Circuit design, Simulation in Proteus

## References 📚
- [Amplifier classes](https://www.electronics-tutorials.ws/amplifier/amplifier-classes.html)
- [2N2222A NPN transistor Datasheet](https://pdf1.alldatasheet.com/datasheet-pdf/download/956542/FCI/2N2222A.html)
- [TIP31C Datasheet](https://www.st.com/resource/en/datasheet/tip31c.pdf)
- [TIP32C Datasheet](https://www.st.com/resource/en/datasheet/tip32c.pdf)

