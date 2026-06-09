### Helpful Documentation

- https://pcbsync.com/drone-pcb/ (general advice regarding controller components)

### Initial Research

- Microcontroller: Chose the STM32 over the ESP32 since the STM has a higher precision with it's use of ARM Cortex-M cores (elaborate) and has more power efficiency compared to that of the ESP. However, the STM32 does not come with inbuilt wireless capabilities, unlike the ESP32, so I will need to wire a separate wireless modules to the microcontroller. If I end up making the drone autonomous, I will likely use the STM32H7 series over the F7. Notes for choosing a specific package from the STM32H753 series, which has a single core:
	- LQFP100 for fewer GPIO, since 100 pins seems sufficient - this is also the cheapest package type
	- 2 MB flash
	- Temperature Range, -40 deg C to 125 deg C, can easily handle controlling multiple peripherals simultaneously
- Accelerometer: IMU-6000, which comes with faster speeds compared to the 6050 since it uses SPI vs I2C
- The control board will likely connect to an external 4 in 1 ESC board (something like the DShot)
- Motors: Emax ECO II Series 2807 1300Kv (?) or 1500Kv, research number of cells
- Flight Software: Ardupilot, with its Kalman Filter, seems to be the best fit for the H7

### Research Round 2

- Battery: 6S Lithium Po/Ion (haven't decided yet), this seems to be the norm for 7'' builds
- 