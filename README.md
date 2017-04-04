# TevoTarantula | Firmware & Tools

The purpose of this repository is to host up-to-date ready to use Firmware for the Tevo Tarantula series of Prusa i3 3D Printers. All credit for the firmware and original configs go to the respective owners. All I have done is prepare a working configuration.h that fits the needs of my printer with good results.

## Versions

There are two versions hosted on this repository. One of them has the default extruder pins for *E0* swapped on the RAMPS.h file because on my particular board the E0 port was not driving the Extruder stepper. So, if you too have this issue, you can use that version.

### [Marlin 1.1 RC8 - Swapped Extruder (E0) pins - No Self Level - Reverse Y]('./Marlin-Tevo-Firmware-NO-SELF-LEVEL-ReverseY-SwappedExtruder')

This version of the software has special settings under pins_RAMPS.h to correct for a faulty stepper driver on the physical *E0* port on my controlboard. All I did was swap the pin numbers on RAMPS.h and swap the connector from **E0** to **E1**. Another thing to note is that config has also switched the pins for the *Hot End Thermistor*. If you are using this version swap your *Hot End Thermistor* connector from **A13** to **A15**.

**Y Axis direction is reversed**

### [Marlin 1.1 RC8 - No Self Level - Reverse Y]('./Marlin-Tevo-Firmware-NO-SELF-LEVEL-ReverseY-DefaultExtruder')

Standard version of the Marlin 1.1 firmware configured for the Tevo Tarantula using the 200x200mm bed and no auto-level. The pin layout has not been modified on this version of the firmware

**Y Axis direction is reversed**
