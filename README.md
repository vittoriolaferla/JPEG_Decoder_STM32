# JPEG Decoding Library for Miosix and MixGui

This is repository contains the custom JPEG decoding library, designed for use with the Miosix system and specifically with MixGui. The library provides the capability to decode JPEG files optimized for STM32 controllers, enabling efficient reading and processing of images.

## System Requirements

Before using this library, make sure you have:

- The Miosix system with MixGui support.
- A C++ development environment compatible with STM32.

## Installation

To integrate this library into your Miosix project with MixGui, follow these steps:

1. Clone the library's repository into your project or add the library as a Git submodule (https://miosix.org/doxygen/mxgui_1.00/main.html).
2. Configure your development environment to include the library files.
3. Refer to the library documentation for further usage instructions.

## Application Flow

Our library follows a structured process to decode JPEG files optimized for STM32 controllers:

1. **Byte Reading:** The library begins by reading the JPEG file, detecting the SOI marker for the image's start.

2. **Interpretation of DQT and DHT Markers:** Subsequently, the DQT and DHT markers are interpreted to acquire the required quantization and Huffman tables for decoding.

3. **Image Scanning (SOS Marker):** The SOS marker initiates image scanning, and pixel data is processed, mapping each pixel to the table ID and coordinates within the MCU.

4. **Data Processing:** The application proceeds to manipulate the decoded image data, allowing effective processing and usage in STM32 applications.

For more technical details about the application flow and how the library specifically handles JPEG data, refer to the separate "Flow.md" document.
