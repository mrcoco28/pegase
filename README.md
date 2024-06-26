# pegase
# README

## Description

This project is a firmware application for an embedded system using an STM32 microcontroller. It integrates various peripherals including GPIO, UART, SPI, and TIM to control LEDs, read environmental sensors, and display data on a MAX7219 LED matrix. The code also includes basic serial communication for debugging purposes.

## Features

- LED control and animations
- Environmental sensor readings (humidity and temperature)
- Real-time clock (RTC) management
- UART communication for debugging
- SPI communication with the MAX7219 LED matrix driver
- Timer-based chronometer

## Hardware Requirements

- STM32 microcontroller (exact model unspecified)
- MAX7219 LED matrix display
- IKS01A3 environmental sensors (humidity and temperature)
- LEDs connected to GPIO pins
- Push buttons for user input
- RTC module

## Software Requirements

- STM32CubeMX
- STM32 HAL Library
- C standard library
- A serial terminal for UART communication (e.g., PuTTY, Tera Term)

## Setup and Configuration

### Clock Configuration

The system clock is configured with an HSI oscillator and LSE for the RTC. The PLL is used to achieve the desired system clock frequency. 

### Peripherals Initialization

1. **GPIO**: Configured for LED outputs and button inputs.
2. **UART**: Configured for serial communication at 115200 baud rate.
3. **SPI**: Configured to interface with the MAX7219 display driver.
4. **TIM6**: Configured for base timer with interrupt.
5. **RTC**: Configured for real-time clock functionalities.

### Pin Assignments

- LEDs are connected to GPIOB pins (L0 to L7).
- Buttons are connected to various GPIO ports (BTN1, BTN2, BTN3, BTN4).
- SPI_CS pin for MAX7219 is configured.

## Code Structure

### Main Function

The main function initializes all configured peripherals and enters an infinite loop to handle:

- LED control using buttons
- Display updates for environmental sensor data
- Serial communication for debugging

### Key Functions

- `switchLed`: Toggle a specific LED.
- `switchLedAll`: Toggle all LEDs.
- `K2000`: Execute a Knight Rider-style LED animation.
- `Chrono`: Update and display the chronometer value.

### Sensor Initialization

The environmental sensors (humidity and temperature) are initialized, and their values are read periodically to update the display and log data via UART.

## Usage

1. **Compile and flash the firmware**: Use STM32CubeIDE or a similar tool to compile and flash the firmware onto the STM32 microcontroller.
2. **Connect the hardware**: Ensure all sensors, LEDs, and buttons are connected as per the pin configuration.
3. **Open a serial terminal**: Connect to the microcontroller's UART port at 115200 baud rate to view debug messages.
4. **Interact with the system**: Use the buttons to control the LEDs and view the sensor data on the MAX7219 display.

### Button Functions

- **BTN1**: Initiate the K2000 LED animation.
- **BTN2**: Print "Hello World" message to the UART terminal.
- **BTN3**: [Reserved for additional functionality]
- **BTN4**: [Reserved for additional functionality]

## Debugging

The UART is used for debugging purposes. Messages related to sensor initialization, data readings, and chronometer values are printed to the terminal.

## Error Handling

An `Error_Handler` function is implemented to handle system errors. It disables interrupts and enters an infinite loop. Custom error messages can be added for more detailed debugging.

## Additional Notes

- Ensure that the LICENSE file is included in the root directory of the project.
- Modify the pin configurations and peripheral settings according to your specific hardware setup.
- The environmental sensor readings are displayed alternately for humidity and temperature based on the `switch_HT` flag.

## Contact

For further assistance, please refer to the official STM32 documentation or contact the project maintainer.
