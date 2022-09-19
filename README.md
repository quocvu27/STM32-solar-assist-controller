# STM32-solar-assist-controller
This is a microcontroller unit that will be used to govern how the solar system and grid system will supply power to the HVAC. Design 1: The microcontroller model used here is STM32G041F8P6. The microcontroller contained 8 sections and two headers for integrating with other parts of the system:

1. 2V-3.3V DC-DC converter that will step-down the voltage from the battery and supply it to the microcontroller since the maximum voltage rating of the chip is 3.3V.
2. Crystal oscillator circuit to provide a stable clock signal and allow the MCU (microcontroller unit) to measure the voltages and currents with high frequency.
3. Voltage divider circuits are included in the design in order to allow the microcontroller to measure high voltage (12V, and 24V).
4. LEDs installed to the board to signal if the microcontroller is running and start measuring.
5. Current sensing circuits to measure high currents from both converters (24A).
6. DAC circuit which uses I2C protocol to supply a small voltage to the feedback port of the solar converter and control the power through the system.
Design 2: STM32F446RE Nucleo board. Contains 4 sections:

1. STM32 Nucleo-F446RE
2. Battery voltage divider circuits, Solar Voltage divider circuit, Grid Voltage divider circuit.
3. DC converter circuit.
4. Solar and Grid current sensing circuit

Design 3: 

1. Use the STM32-F441RE developer board
2. External PCB voltage divider circuits for measurement.
