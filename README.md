# Hypercube–Voron Trident Hybrid

This repository contains the Klipper configuration backup from a custom CoreXY 3D printer I built by combining a Hypercube Evolution motion system with a Voron Trident-inspired frame made from 2020 aluminium extrusion.

The project was designed around upcycling parts from a Prusa Mendel i3 clone I had built in 2015. The printer has since been dismantled, but many of its components remain available for reuse and this repository preserves its final configuration.

## Build overview

- Hypercube Evolution-derived CoreXY motion system
- Voron Trident-inspired 2020 aluminium-extrusion frame
- Arduino Mega 2560 with RAMPS 1.4
- TMC2208 stepper drivers in standalone step/direction mode
- Raspberry Pi 4 with 2 GB RAM running Klipper and Moonraker
- Prusa MK3S+ extruder adapted with a custom carriage
- 12 V aluminium heated bed with a magnetic base and removable PEI-coated build plate
- 12 V NPN normally-open inductive probe for Z homing and a 10 × 10 bed mesh
- Mechanical X and Y endstops
- Microswitch-based filament runout sensor
- Repurposed Sony Android phone running KlipperScreen, later used wirelessly over Wi-Fi

The Klipper configuration used CoreXY kinematics, input shaping, pressure advance, screw-tilt measurement, safe Z homing and bed-mesh compensation. The configured XY motion ceiling was 200 mm/s; the highest printing speed I achieved in practice was approximately 130 mm/s.

## Repository contents

The files under `printer_data/config` are a historical backup of the machine rather than a ready-to-use configuration for another printer. They include the printer, Moonraker, KlipperScreen, camera and related service configuration that existed on the Raspberry Pi.

Pin assignments, motor directions, driver current, thermistor types, probe polarity, heater power, serial paths and calibration values must be checked against the actual hardware before reuse. Do not copy the wiring or configuration to another machine without verifying it independently.

## Project story and wiring notes

The complete build story—including the upcycling goal, custom printed parts, RAMPS connections, 12 V probe interface, Android KlipperScreen setup and lessons learned—is documented here:

**[What I Tried to Achieve with My Hypercube–Voron Trident Hybrid](https://cagataykilinc.com.tr/2026/09/06/hypercube-voron-trident-hybrid/)**

## Printable parts

- [CoreXY printer electronics enclosure](https://makerworld.com/en/models/535666-corexy-printer-electronics-case)
- [Hypercube Evolution carriage for Prusa MK3S+ extruder](https://makerworld.com/en/models/535702-hypercube-evolution-carrige-prusa-mk3s-extruder)
- [Mechanical X endstop for the MK3S+ carriage](https://makerworld.com/en/models/535694-mechanical-x-end-stop-for-mk3s-carriage)
- [Cable-chain mount for 2020 extrusion](https://makerworld.com/en/models/535695-hypercube-evo-cablechain-mount-2020-extrusion)
- [Filament sensor for 2020 extrusion](https://makerworld.com/en/models/535703-filament-sensor-for-2020-aluminium-extrusion)
- [Mechanical Y endstop for 2020 extrusion](https://makerworld.com/en/models/535704-mechanical-y-end-stop-for-2020-aluminium-extrusion)

## Backup tooling

This repository was created with [klipper-backup](https://github.com/Staubgeborener/klipper-backup).
