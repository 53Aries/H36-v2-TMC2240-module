# Stepper motor
[manual_stepper my_step]
step_pin: PB7
dir_pin: PA1
enable_pin: !PA14
microsteps: 16
rotation_distance: 40
velocity: 600
accel: 10000
endstop_pin: ^PC0        # adjust to your endstop pin
homing_speed: 50
position_min: -99999
position_max: 99999

# TMC2240 driver via software SPI
[tmc2240 manual_stepper my_step]
cs_pin: PA13
spi_software_mosi_pin: PB11
spi_software_miso_pin: PA15
spi_software_sclk_pin: PB10
run_current: 1.00       # adjust for your motor (A)
rref: 12000              # external resistor in ohms (12k default)
stealthchop_threshold: 999999
