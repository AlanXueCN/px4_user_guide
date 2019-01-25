# Pixhack V3X

CUAV ** Pixhack V3x **Flight Controller Board is a flexible autopilot and an alternative to PIXHACK V3 for commercial system manufacturers.

>**tip**Because Pixhack v3 part of the chip is discontinued, the led driver chip has been changed to NCP5623C, and hmc5983 has been removed. For the sake of distinction, it has been named Pixhack v3x. Please do not use firmware below 1.80 version (it will Make your led not work)


The board is a variant of the SOLO Pixhawk<sup>&reg;</sup> 2 (PH2) flight controller, which is in turn based on the [Pixhawk-project](https://pixhawk.org/) **FMUv3** open hardware design. It runs PX4 on the [NuttX](http://nuttx.org) OS, and is fully compatible with both PX4 or ArduPilot<sup>&reg;</sup> (APM) firmware.

*Pixhack V3x* has significant improvements with respect to the original design, including better interface layout and the addition of vibration damping and a thermostat system.

![Pixhack v3x](../../assets/flight_controller/pixhack_v3x/pixhack_v3x.png)


## Quick Summary

* Microprocessor:
  * STM32F427
  * STM32F100 (Failsafe co-processor)
* Sensors:
  * Accelerometers (2): LS303D, MPU6000
  * Gyroscopes (2): L3GD20, MPU6000
  * Compass (2): LS303D
  * Barometer (2): MS5611 X2
* Interfaces:
  * MAVLink UART (2)
  * GPS UART (2)
  * DEBUG UART (1)
  * RC IN (for PPM, SBUS, DSM/DSM2)
  * RSSI IN: PWM OR 3.3ADC
  * I2C (2)
  * CAN BUS (1)
  * ADC IN: 3.3V X1 , 6.6V X1
  * PWM OUT: 8 PWM IO + 4 IO
* Power System:
  * PM POWER IN: 4.5 ~ 5.5 V
  * USB POWER IN: 5.0 V +- 0.25v
* Weight and Dimensions:
  * Weight: 63g
  * Width: 68mm
  * Thickness: 17mm
  * Length: 44mm
* Other Characteristics:
  * Operating temperature: -20 ~ 60°C

## Availability

The board can be purchased from:
* [store.cuav.net](http://store.cuav.net/index.php?id_product=8&id_product_attribute=0&rewrite=pixhack-v3-autopilot&controller=product&id_lang=3)
* [leixun.aliexpress.com/store](https://leixun.aliexpress.com/store)

## Building Firmware

> **Tip** Most users will not need to build this firmware!
  It is pre-built and automatically installed by *QGroundControl* when appropriate hardware is connected.

To [build PX4](https://dev.px4.io/en/setup/building_px4.html) for this target:
```
make px4_fmu-v3_default
```

## Pinouts and Schematics

* Open hardware files: https://github.com/cuav/CUAV_Hardware/tree/master/Pixhack_V3
* Documentation/wiring guides: http://doc.cuav.net/PixHack/pixhack-v3.html