# Closed-Loop DC Motor Speed Control Using ESP32

A closed-loop motor speed control system built with an ESP32 
microcontroller. The system regulates DC geared motor speed using 
incremental encoder feedback and a proportional control algorithm. 
Supports three input modes: keypad, potentiometer, and Bluetooth.

## How It Works
The encoder generates pulses proportional to motor rotation. The ESP32 
counts pulses to calculate actual RPM, compares it to the target speed, 
and adjusts the PWM duty cycle via proportional control. If the motor 
runs slow, PWM increases; if too fast, PWM decreases — maintaining stable 
speed under varying load conditions.

## Components
- ESP32 Microcontroller
- DC Geared Motor: JG25-370-CE with integrated encoder
- Motor Driver: L298N / L238 H-Bridge
- Potentiometer (analog speed reference)
- LCD Display (I2C — SDA/SCL)
- Keypad & Bluetooth module

## Pin Connections
| Component | ESP32 Pin | Function |
|---|---|---|
| Motor Driver ENA | GPIO 23 | PWM speed control |
| Motor Driver IN1 | GPIO 18 | Motor direction |
| Motor Driver IN2 | GPIO 19 | Motor direction |
| Encoder Channel A | GPIO 5 | Speed feedback (interrupt) |
| Encoder Channel B | GPIO 13 | Direction detection |
| Potentiometer | GPIO 34 | Analog speed reference |
| LCD SDA | GPIO 21 | I2C data |
| LCD SCL | GPIO 22 | I2C clock |

## Technologies
`ESP32` `Arduino Framework` `C Programming` `PWM Control` 
`Incremental Encoder` `Proportional Control` `L298N H-Bridge` 
`Bluetooth Serial` `I2C LCD`

## Repository Contents
- `/code` — ESP32 Arduino sketch (.ino)
- `/schematics` — Wiring diagram and pin map
- `/report` — Full project report (PDF)
