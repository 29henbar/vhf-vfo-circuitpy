# vhf-vfo-circuitpy
# vhf vfo wtiten in circuitpython for raspi pi pico
  
# Copyright <2024> <N4CNR (Richard Neese) (n4cnr.ham@gmail.com)>

# Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), 
# to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, 
# and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

# The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

# THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, 
# WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# CircutPython 9

# Designing a VHF VFO 6M or 2m
# CircuitPython on a Raspberry Pi Pico with an SI5351 and an ST7735 
# SPI display involves several components and functionalities. 
# Below is a step-by-step implementation plan, followed by the complete code.

# Implementation Plan:
# Setup and Initialization:

# Initialize the SPI display (ST7735).
# Initialize the SI5351.
# Set up the encoders and buttons.
# Display Functionality:

# Display the current frequency, mode (USB/LSB), RIT status, and step size.
# Encoders and Button Handling:

# Handle frequency changes with the main encoder.
# Handle RIT changes with the RIT encoder.
# Change frequency steps with the step button.
# Toggle RIT with the RIT encoder button.
# Change mode (USB/LSB) with the main encoder button.
# Board Raspi Pico, flash screen red if ptt active

# Continuously update the display based on user interactions.
# Update the SI5351 frequency output based on the current 


# Parts needed
# 1) Rasberry Pi Pico Raspberry https://www.adafruit.com/product/4883 or https://www.adafruit.com/product/5525
# 2) si5351 breakout board https://www.adafruit.com/product/2045
# 3) 2 rotor encoders KY-040 Rotary Encoder Module Knob Push Button w Theaded Shaft + Nut
# 4) LCD Display https://www.adafruit.com/product/358
# 5) breakout breadboard like this https://www.ebay.com/itm/203042162648
# 6) some buttons for changing modes

# Download the latest CircuitPython https://circuitpython.org/board/raspberry_pi_pico/

# copy the uf2 file to the raspi pico .


# the encode for the freq also changes the mode lsb/usb
# the button on the rit encoder enables/disables rit.
# you will need a button for step/region/and band (band is if you plan to have 2m/6m)


# New Not working correctly 8/4/2022
# This updated code includes functions save_to_nvm and load_from_nvm for saving and loading the current band and frequency to and from non-volatile memory (NVM). 
# The values are saved whenever the band, frequency, or region is changed, and are loaded at the start of the program. This ensures that the device retains the 
# last used band and frequency settings across power cycles.