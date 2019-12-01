# Digital adjusted regulator output

## Keywords
Voltage regulator, supply, PWM/DAC controlled output, calculation formula

## Abstract
In some cases is a digital controllable output voltages of a V<sub>FB</sub> or V<sub>REF</sub> input regulator desirable. The calculation and dimensioning of the feedback network is described in this article.


## Topology

<br />
<center><img src="./inc/dig_ctrl_vout_topology.svg" height="75%" width="75%" alt="Regulator topology with digital controlled output via feedback manipulation" title="Regulator topology with digital controlled output" /></center>
<br />



## Dimensioning



## Derivation

The voltage regulator can rewritten in a equivalent voltage sources circuit as follows:
<center><img src="./inc/reguator_voltage_src_equivalent_circuit.svg" height="50%" width="50%" alt="VFB controlled regulator as voltage source equivalent circuit, regulator itself is substituted by voltage sources" title="VFB controlled regulator as voltage source equivalent circuit" /></center>
<br />

To allow the calculation of the circuit is the substitution of the voltage sources mandatory. Rewritten with current sources:
<center><img src="./inc/reguator_current_src_equivalent_circuit.svg" height="50%" width="50%" alt="VFB controlled regulator as current source equivalent circuit" title="VFB controlled regulator as current source equivalent circuit" /></center>
<br />

Replace the resistance by conductance:

<img src="https://latex.codecogs.com/svg.latex?G_{1}=\frac{1}{R_1};%20\quad%20G_{2}=\frac{1}{R_{2}};%20\quad%20G_{3}=\frac{1}{R_3}" title="G_{1}=\frac{1}{R_1}; \quad G_{2}=\frac{1}{R_{2}}; \quad G_{3}=\frac{1}{R_3}" />


Convert voltage sources to corresponding current sources:

<img src="https://latex.codecogs.com/svg.latex?I_{out}=I_{q1}=\frac{V_{out}}{R_1};%20\quad%20I_{DAC}=I_{q2}=\frac{V_{DAC}}{R_3}" title="I_{out}=I_{q1}=\frac{V_{out}}{R_1}; \quad I_{DAC}=I_{q2}=\frac{V_{DAC}}{R_3}" />


All conductances assigned to V<sub>FB</sub> follows with Kirchhoff's current law:

<img src="https://latex.codecogs.com/svg.latex?V_{FB}\left(G_{1}+G_{2}+G_{3}\right)=I_{q1}+I_{q2}" title="V_{FB}\left(G_{1}+G_{2}+G_{3}\right)=I_{q1}+I_{q2}" />


Current sources back transformed to voltage sources and the basic formula is ready:

<img src="https://latex.codecogs.com/svg.latex?\boxed{V_{FB}\left(G_{1}+G_{2}+G_{3}\right)=V_{out}%20\cdot%20G_{1}%20+%20V_{DAC}%20\cdot%20G_{3}}" title="\boxed{V_{FB}\left(G_{1}+G_{2}+G_{3}\right)=V_{out} \cdot G_{1} + V_{DAC} \cdot G_{3}}" />










https://latex.codecogs.com/svg.latex?


## Used Tools

