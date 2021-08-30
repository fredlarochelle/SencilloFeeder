# Sencillo Feeder
From the Spanish word for "simple", the Sencillo is a fully featured SMT Feeder following the KISS principle. The aimed is to design a fully featured dual-bank SMT feeder for less than 5$ per bank. This project is currently a work-in-progress, anything or everything could change at any moments.

## Project ideas
The goal for the Sencillo project are the followings:
* Try to keep the price as low as possible with the aim to be under 5$ USD per bank.
  * Adapt the tape peeling mechanism from the [Ploopy PNP Feeder](https://github.com/ploopyco/pnp-feeder), since it doesn't require a motor to cut on cost.
  * Make the feeder dual bank to divide the cost of the electronics between multiple "channels".
* Limit to 10cmx10cm 2 layers PCB that can be made cheaply by [JLCPCB](https://jlcpcb.com/).
* 3D printed part don't required any supports.
* As slim a profile as possible.
* Compatible with the [Index ecosystem](https://github.com/index-machines/index).

## Reasoning of the component choice
### Mechanical
#### Actuator
At this price point, the only alternative is to use a electric motor and stepper aren't slim enough, soo we will go with good old N20 format of motors.
#### Index wheel
The index wheel will be made of an 1mm PCB manufactured by PCB fab.

### Electronics
#### Microprocessor
MCU | Manufacturer | Clock speed | Processor | Packaging | Pricing (1+) | Pricing (10+)
--- | ------------ | ----------- | --------- | --------- | ------------ | -------------
[ESP32-C3](https://www.espressif.com/en/products/socs/esp32-c3) | Espressif | 160 MHz | RISC-V | QFN-32 (5x5mm) | 1.35 | 0.98
[ATSAMD10D13](https://www.microchip.com/en-us/product/ATSAMD10D13) | Microchip | 48 MHz | Cortex-M0+ | SOIC-20 (12.8x7.6mm) | 1.11 | *
Atmega 328p |
Attiny |
STM32 | 
NXP | 

#### Motor driver
TI DRV8833 Dual H-Bridge

Allegro A3910 Dual Half-Bridge

Allegro A3916 Dual H-Bridge

#### RS-485 Transceiver
MAX307

#### Reflective sensor
Vishay VCNT2020 0.91 0.61

OnSemi QRE133 1.08 0.52

Sharp GP2S60A 0.91 0.43

Everlight ITR8307 * 0.13 


