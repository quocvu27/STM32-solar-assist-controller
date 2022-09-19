# STM32-solar-assist-controller
This is a microcontroller unit that will be used to govern how the solar system and grid system will supply power to the HVAC. Design 1: The microcontroller model used here is STM32G041F8P6. The microcontroller contained 8 sections and two headers for integrating with other parts of the system:

2V-3.3V DC-DC converter that will step-down the voltage from the battery and supply it to the microcontroller since the maximum voltage rating of the chip is 3.3V.
crystal oscillator circuit to provide a stable clock signal and allow the MCU (microcontroller unit) to measure the voltages and currents with high frequency.
Voltage divider circuits are included in the design in order to allow the microcontroller to measure high voltage (12V, and 24V).
3 LEDs installed to the board to signal if the microcontroller is running and start measuring.
Current sensing circuits to measure high currents from both converters (24A).
DAC circuit which uses I2C protocol to supply a small voltage to the feedback port of the solar converter and control the power through the system.
Design 2: STM32F446RE Nucleo board. Contains 4 sections:

STM32 Nucleo-F446RE
Battery voltage divider circuits, Solar Voltage divider circuit, Grid Voltage divider circuit.
DC converter circuit.
Solar and Grid current sensing circuit
