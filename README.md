# TevoTarantula | Firmware & Tools

The purpose of this repository is to host up-to-date ready to use Firmware for the Tevo Tarantula series of Prusa i3 3D Printers. All credit for the firmware and original configs go to the respective owners. All I have done is prepare a working configuration.h that fits the needs of my printer with good results.

## Versions

There are three versions hosted on this repository.The First version is "vanilla" and has very few customizations, Y direction is default and so is the wiring. One of them has the default extruder pins for *E0* swapped on the RAMPS.h file because on my particular board the E0 port was not driving the Extruder stepper. So, if you too have this issue, you can use that version.

## BED / NOZZLE PID Tuning

It is highly recommended that you tune your own PID's for the bed and the nozzle. This is very easy to do and should only take a few minutes. Please refer to [This Guide on PID Auto Tuning]('http://reprap.org/wiki/PID_Tuning') for more information.

## Thermal Runway / Hysterisis

I have set some very lenient terms on the thermal settings for this firmware because I was getting random *Thermal Runway* warnings over absolutely nothing. The way I have it set the controller will tolerate up to a *5 degree C* discrepancy for up to *10 seconds* before shutting everything down and warning of Thermal Runway. If these are too lenient for you, please consider revising those settings in the **Configuration.h* file.


### [Marlin 1.1 RC8 - Default Wiring - No Self Level - Default Y]('Marlin-Tevo-Firmware-NO-SELF-LEVEL-DefaultY-DefaultExtruder') [ RECOMMENDED FOR MOST ]

This version has default extruder/sensor wiring and default Y motor direction.

### [Marlin 1.1 RC8 - Swapped Extruder (E0) pins - No Self Level - Reverse Y]('Marlin-Tevo-Firmware-NO-SELF-LEVEL-ReverseY-SwappedExtruder')

This version of the software has special settings under pins_RAMPS.h to correct for a faulty stepper driver on the physical *E0* port on my controlboard. All I did was swap the pin numbers on RAMPS.h and swap the connector from **E0** to **E1**. Another thing to note is that config has also switched the pins for the *Hot End Thermistor*. If you are using this version swap your *Hot End Thermistor* connector from **A13** to **A15**.

**Y Axis direction is reversed**

### [Marlin 1.1 RC8 - No Self Level - Reverse Y]('Marlin-Tevo-Firmware-NO-SELF-LEVEL-ReverseY-DefaultExtruder')

Standard version of the Marlin 1.1 firmware configured for the Tevo Tarantula using the 200x200mm bed and no auto-level. The pin layout has not been modified on this version of the firmware

**Y Axis direction is reversed**
