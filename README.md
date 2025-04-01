# STM32F407 + GUVA-S12SD Sunlight Sensor Interface

This project demonstrates how to interface the GUVA-S12SD sunlight sensor with the STM32F407 microcontroller to measure the intensity of sunlight. The analog output of the sensor is connected to the ADC channel 4 of the STM32F407. As sunlight falls on the sensor, the sensor generates a voltage that is proportional to the intensity of light. This voltage is read by the STM32F407's ADC (Analog-to-Digital Converter) and displayed in the CubeIDE terminal for monitoring.

# Project Overview:

The GUVA-S12SD is a photodiode-based sensor designed for measuring light intensity. The sensor outputs an analog voltage, which varies with the intensity of the light falling on it. By connecting the sensor's output to the STM32F407's ADC pin, we can read this voltage and convert it into a corresponding digital value that can be processed and displayed on a terminal.

# Key Features:

Analog Signal Acquisition: The GUVA-S12SD sensor provides an analog output that is fed into the STM32F407's ADC channel 4.

ADC Conversion: The STM32F407's ADC reads the sensor's output and converts it into a digital value that corresponds to the light intensity.

Real-time Output: The measured sensor value (as a digital number) and the corresponding voltage (in volts) are displayed in real-time on the CubeIDE terminal, providing immediate feedback about the light conditions.

# How It Works:

The GUVA-S12SD sunlight sensor generates a voltage that is proportional to the intensity of light falling on the sensor. As more light hits the sensor, the output voltage increases.

The sensor’s analog output is connected to ADC Channel 4 of the STM32F407. The microcontroller's ADC reads this voltage and converts it into a digital value.

In the firmware, the ADC value is read continuously and converted into a corresponding voltage using the ADC reference voltage and resolution.

The measured ADC value and the calculated voltage are printed to the CubeIDE terminal, providing real-time feedback on the light intensity.

The conversion formula used is:

Sensor voltage = (ADC_value/4095)*V_ref
 
where:

ADC_value is the digital value read from the ADC (12-bit resolution, ranging from 0 to 4095)

V_ref is the reference voltage used by the ADC (5V)
