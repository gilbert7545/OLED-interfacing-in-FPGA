# OLED-interfacing-in-FPGA
This is to demonstrate how to interface an OLED to an Spartan 7 FPGA Board using Verilog (or VHDL). It covers the complete process of connecting, initializing, and controlling popular OLED modules (such as SSD1306) via standard protocols like I2C or SPI. 

# Hardware Requirements

-Spartan 7 FPGA board (e.g., Digilent Arty S7, Edge Spartan 7)

-OLED display module (SSD1306 or similar, with I2C or SPI interface)

-Jumper wires or Pmod connector

-PC with Vivado installed

# Steps to Interface OLED
1. Hardware Connection
   
-Identify which pins on your FPGA board are available for GPIO, SPI, or I2C (refer to your board manual).​

-Connect the OLED display to the corresponding IO pins or the Pmod connector using jumper wires.

-Power the display from the 3.3V supply available on the FPGA board.

2. Design HDL Modules
   
-Write Verilog/VHDL modules for communication protocol (I2C or SPI Master).​

-Write the OLED controller logic that initializes the display and sends data/commands to render text or graphics.

-Generate FSM (finite-state machine) for command sequencing and pixel addressing.

3. Vivado Project Setup

-Create a new project in Vivado for your FPGA board.

-Add your HDL source files and set constraints to map IO pins to physical FPGA pins used for OLED connectivity.

-Synthesize, implement, and generate the bitstream.

4. Programming and Debugging

-Program the FPGA with the bitstream using Vivado Hardware Manager.​

-Test the display by sending initialization commands and simple test patterns or text.

5. Display Data
    
-Modify the HDL code to display custom graphics, images, or real-time data from other FPGA modules.

-Advanced: Use block RAM as a frame buffer to store multiple screens/pages and switch using board switches.


# Troubleshooting
Confirm correct wiring and pin mapping.

Check OLED datasheet for power and timing requirements.

Debug signal waveforms in Vivado using simulation tools.

