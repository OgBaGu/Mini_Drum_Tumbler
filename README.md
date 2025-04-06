| Supported Targets | ESP32 | ESP32-C2 | ESP32-C3 | ESP32-C5 | ESP32-C6 | ESP32-C61 | ESP32-H2 | ESP32-P4 | ESP32-S2 | ESP32-S3 | Linux |
| ----------------- | ----- | -------- | -------- | -------- | -------- | --------- | -------- | -------- | -------- | -------- | ----- |

**In Progress - Do not use directly!**

**Note**: The project has only been tested with the ESP32 WROOM 32D. Other ESP32 variants have not been tested and may require additional adjustments.

# Hello World Example

Starts a FreeRTOS task to print "Hello World".

(See the README.md file in the upper level 'examples' directory for more information about examples.)

## How to use example

Follow detailed instructions provided specifically for this example.

Select the instructions depending on Espressif chip installed on your development board:

- [ESP32 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/stable/get-started/index.html)
- [ESP32-S2 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s2/get-started/index.html)


## Example folder contents

The project **hello_world** contains one source file in C language [hello_world_main.c](main/hello_world_main.c). The file is located in folder [main](main).

ESP-IDF projects are built using CMake. The project build configuration is contained in `CMakeLists.txt` files that provide set of directives and instructions describing the project's source files and targets (executable, library, or both).

Below is short explanation of remaining files in the project folder.

```
├── CMakeLists.txt
├── pytest_hello_world.py      Python script used for automated testing
├── main
│   ├── CMakeLists.txt
│   └── hello_world_main.c
└── README.md                  This is the file you are currently reading
```

## How It Works

1. **Stepper Motor Control**: The SP2502 NEMA17 stepper motor is controlled via the stepper expansion driver board, using PWM signals generated by the ESP32 WROOM 32D.
   
2. **Power Supply**: The LM2596S step-down converter regulates the power supply to the system components, providing a stable voltage for the motor and electronics.

3. **User Interface**: The SH1106 1.3-inch OLED displays the status of the drum tumbler machine. The EC11 rotary encoder is used for adjusting settings such as speed, and the two buttons (OK and ESC) are used to start/stop the tumbler and navigate settings.

## Troubleshooting

* **Program Upload Failure**

    * Hardware connection is not correct: Run `idf.py -p PORT monitor` and reboot your board to check for any output logs.
    * The baud rate for downloading is too high: Lower your baud rate in the `menuconfig` menu and try again.

* **Stepper Motor Not Moving**

    * Ensure that the stepper expansion driver is properly connected to the ESP32 and the motor.
    * Check power connections, particularly the LM2596S step-down converter and ensure it's providing the correct voltage.

## Technical Support and Feedback

Please use the following feedback channels:

* For technical queries, visit the [esp32.com](https://esp32.com/) forum
* For feature requests or bug reports, create a [GitHub issue](https://github.com/espressif/esp-idf/issues)

We will get back to you as soon as possible.