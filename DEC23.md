# Simple Flashing LED controller for LEGO train

## Purpose
I own LEGO set number #7938, motorized modern passanger train and wanted to add festive lighting to its passanger compartments.

In order to achieve my stated goals I designed, assembled and tested a simple control board on perfoboard in the two days before Christmas.

## A bit of circuit theory
The circuit I built to control several low power 5mm LEDs is designed around an RC relaxation oscillator. The oscillator should normally be built using a comparator, but such a component was not available in my pile of random components.

This is how the oscillator looks like:

<br>
  <p align="center">
    <img height = "550" src = "OSC_SS.png">
    <br>
    <br>
    <a><b>Relaxation oscillator</b></a>
</p>
<br>

The oscillator produces a square wave signal with frequency determined by the series RC network formed by R1 and C, according to the formula $f_{osc} = \frac{1}{1.38 \cdot R_{1}\cdot C}$. A proper derivation of the timing formula is provided <a href="https://www.ti.com/lit/ab/snoa998/snoa998.pdf?ts=1704275294118&ref_url=https%253A%252F%252Fwww.google.ru%252F">here .</a>

This circuit is useful at both higher and lower frequencies. For my uses a 50K potentiometer and a 10uF capacitor sufficed.

This is how the control boards look like at component level:

<br>
  <p align="center">
    <img height = "550" src = "ZUG_XMAS.png">
    <br>
    <br>
    <a><b>Implemented led control board</b></a>
</p>
<br>

The for screw terminals ST1 to ST4 are used to control colored leds placed in different corners of the train wagon. To connect the LEDs to the control board I used male to female Dupont cables. ST5 provides access to the positive rail of the circuit to increase the number and 
brightness of controllable LEDs.

## Some preliminary conclusions

## Bibliography