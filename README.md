# STM32F4xx grblHAL driver (UWLab Fork)

## Overview
This is a custom fork of grblHAL for STM32F4xx, modified to support a 2-axis CNC plasma cutting system developed for the ME 481/482 capstone project at the University of Waterloo. These modifications adapt grblHAL to the specific needs of our plasma cutter by adjusting configuration settings and improving safety behavior.

## Key Modifications
- **Machine Configuration**: Adjusted settings for our CNC plasma cutter, including:
  - `Spindle` configured as an on/off output.
  - `Probe` functionality disabled (not needed for our machine).
- **Custom Core (core-UWLab)**:
  - Replaced `grblHAL/core` with a modified fork (`core-UWLab`).
  - Changed Feed Hold behavior so that it stops the spindle (torch) as well, even when not in laser mode.

## Building and Installation
- Built and uploaded the `nucleo_f446re_generic_uno` environment using **PlatformIO in VS Code**.
- Followed the original repository’s build instructions for setup details.

## Building and Installation
1. **Build and Upload**:  
   - Built and uploaded the `nucleo_f446re_generic_uno` environment using **PlatformIO in VS Code**.
   - Followed the original repository’s build instructions for setup details.
2. **Release (firmware.bin)**:
   - A pre-compiled `firmware.bin` file is available for download in the Releases section.
   - Once downloaded, copy the `firmware.bin` file to the root directory of the drive that appears when the NUCLEO-F446RE board is plugged into your computer.

## Date
March 12, 2025
