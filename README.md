# Arduino Robotic Arm with Color Sensor

I built this robotic arm for my Circuits and Electronics course at Zewail City. Four potentiometers let me control the arm and gripper by hand. A TCS34725 color sensor mounted next to the gripper reads the color of nearby objects.

## Demo

[Watch the robotic arm in action on MediaFire](https://www.mediafire.com/file/t8biwkywt60htjv/20261102_210041.mp4/file)

## Components

- Arduino Uno
- 4 servo motors
- 4 × 50 kΩ potentiometers
- TCS34725 color sensor
- External 5 V power supply for the servos

## How it works

Each potentiometer controls one servo. The Arduino maps the knob readings to target angles and moves the servos in small steps. The color sensor communicates with the Arduino over I²C. The Serial Monitor displays the four commanded angles and the color result.

At startup, the program records the empty background as a reference. Keep objects away from the sensor during the first three seconds.

## Wiring

| Potentiometer input | Servo signal |
| --- | --- |
| A0 | D5 |
| A1 | D4 |
| A2 | D3 |
| A3 | D2 |

The color sensor connects to the Arduino through SDA (A4) and SCL (A5). Its VIN connects to 3.3 V and its GND connects to Arduino GND. The servos use a separate 5 V supply with a common ground shared with the Arduino.

## Acknowledgments

Thank you to Eng. Ahmed Abdel-Gawad Bilal and Dr. Mohamed Maher Ata.
