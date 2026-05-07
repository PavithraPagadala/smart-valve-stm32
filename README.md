**Smart Valve — STM32WLE5 Wireless Valve Controller**

A wireless smart valve system that automatically regulates room temperature by adjusting a valve actuator based on real-time environmental sensor data. Built on the STM32WLE5JC microcontroller with LoRa radio for long-range, low-power communication — no Wi-Fi required.



**Project Overview**

This system is designed for large buildings and remote sites where Wi-Fi coverage is unavailable. The valve actuator is controlled based on temperature readings received over a LoRa network, enabling automated HVAC regulation across wide areas.

The device connects to The Things Network (TTN) via a LoRa gateway and supports Over-The-Air (OTA) firmware updates, making remote maintenance possible without physical access to the device.



**Hardware**

ComponentDetailsMicrocontrollerSTM32WLE5JC (ARM Cortex-M4, integrated LoRa)Communication LoRa radio (built-in), UART Actuator Valve motor (PWM controlled)Sensors Temperature sensor, end-stop switches Power Battery-powered with ultra-low-power optimization Debugger J-Link, ST-Link Test Equipment Logic Analyzer, Oscilloscope, NRF Power Profiler Kit



**Peripherals Used**

Peripheral Purpose GPIO (Output)Enable/disable valve driver GPIO (Input + EXTI)Read end-stop switch states, manual-override push-buttons ADC Battery voltage monitoring, motor current sensing, temperature measurement Timer 1 (PWM)Valve motor speed control with fine granularity Watchdog Timer System reset on firmware hang UART (115200 baud)Debug logging, OTA data transmission and reception LoRa Radio Long-range temperature data transmission to TTN gateway



**Key Features**



Wireless Control — LoRa-based communication (no Wi-Fi needed), connected to The Things Network

OTA Firmware Update — Remote firmware upgrades via UART without physical access

Low Power Operation — Ultra-low-power sleep/wake cycles optimized using NRF Power Profiler Kit

Motor Safety Logic — ADC-based motor current monitoring for overcurrent shutdown

Battery Monitoring — Continuous battery voltage tracking with safety thresholds

Interrupt-Driven I/O — Manual override buttons handled via EXTI interrupts

PWM Motor Control — Smooth valve transitions without motor stalling





**Software \& Tools**

ToolPurposeSTM32CubeIDEDevelopment and debugging IDESTM32 HAL API Peripheral driver layer Keil MDK Alternate build environment J-Link / ST-Link Firmware flashing and real-time debugging Logic Analyzer PWM waveform validation, protocol verification Oscilloscope Signal integrity, motor transition verification NRF Power Profiler Kit Active/sleep current measurement Putty / Real Term / Tera Term Serial communication and debug logging SVN Source code version control Code Beamer Bug tracking, feature requests, test case management



System Architecture

\[Temperature Sensor] --> \[LoRa Gateway] --> \[The Things Network]

&#x20;                                                   |

&#x20;                                           \[STM32WLE5JC MCU]

&#x20;                                                   |

&#x20;                             +---------------------+---------------------+

&#x20;                             |                     |                     |

&#x20;                        \[ADC Monitor]        \[Timer PWM]           \[GPIO/EXTI]

&#x20;                        Battery voltage      Motor speed           End-stop switches

&#x20;                        Motor current        Valve control         Manual override

&#x20;                        Temperature



**My Responsibilities**



Configured GPIO for digital outputs (valve driver enable/disable) and interrupt-driven inputs (manual override buttons)

Set up ADC for continuous monitoring of battery voltage, motor current, and temperature

Implemented UART at 115200 baud for debug logging and OTA firmware transmission

Configured Timer 1 in PWM mode for smooth valve motor speed control

Integrated LoRa gateway with The Things Network for reliable data transmission

Used logic analyzer and oscilloscope to validate PWM waveforms and verify wake-up sequences

Optimized wake/sleep intervals for ultra-low-power operation using NRF Power Profiler Kit

Managed source code and pull request reviews using SVN

Tracked bugs, features, and test cases in Code Beamer





**What I Learned**



Real-world embedded system design from schematic to deployment

Low-power firmware optimization techniques for battery-operated IoT devices

LoRa protocol integration and IoT network connectivity (TTN)

OTA firmware update implementation over UART

Hardware debugging with professional tools (J-Link, logic analyzer, oscilloscope)

Motor control safety logic using ADC-based current monitoring





Developer

Pavithra Pagadala

Embedded Software Engineer | STM32 | LoRa | IoT Protocols | Low Power Firmware



Email: pavithrapagadala25@gmail.com

LinkedIn: www.linkedin.com/in/pavithra-pagadala-3b52ba254

Location: Andhra Pradesh, India





Company

Developed during employment at Minebea Intec Pvt Ltd, Bengaluru (August 2022 – December 2023)



Note: Source code is proprietary and not shared in this repository. This README documents the technical work and skills applied during the project.

