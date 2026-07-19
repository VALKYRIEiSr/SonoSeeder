# SonoSeeder: Autonomous Agro-Technological Robot
**WRO International 2024 | Future Innovators Category | Izmir, Türkiye | 🥈 Silver Medal**

## Project Overview
SonoSeeder is a scaled-down proof-of-concept for a multi-functional, solar-powered agro-technological robot that integrates field preparation, precision seeding, irrigation, and ultrasound-assisted physiological seed enhancement into a single autonomous system. It was developed by LGS Defence Team B for the World Robot Olympiad (WRO) International 2024, where it was awarded the **Silver Medal** in the Future Innovators category.

The robot combines a subsurface thermal ploughing module for non-chemical weed elimination via conductive heat transfer, a servo-driven precision seeding mechanism, a mobile irrigation unit, and a custom-built ultrasound chamber experimentally validated to accelerate seed germination and prime antioxidant defense mechanisms. Built on an ESP32 microcontroller with sensor fusion and closed-loop PID-style control, SonoSeeder operates fully autonomously across a defined field area.

## Technical Research
The literature review, experimental validation, and full system design behind this project are documented in the accompanying paper:
* **Project Paper:** [`SonoSeeder.pdf`](./SonoSeeder.pdf) (includes self-validation trial data comparing ultrasound-treated and control seedling growth)

## Technical Specifications
* **Microcontroller:** ESP32 (Bluetooth-configured mission parameters, PWM/LEDC channel control)
* **Navigation:** Magnetometer-based heading (hard-iron/soft-iron calibrated) with encoder-derived RPM feedback and P-controller correction
* **Field Preparation:** Dual soldering-iron heating elements for subsurface thermal weed ploughing (mirrored servo-actuated compartment)
* **Seeding:** Servo-driven cylindrical seeding head with groove-based seed transport
* **Irrigation:** 6V DC water pump with rear-mounted sprinkler, funnel-shaped reservoir
* **Seed Enhancement:** Custom ultrasound chamber, 555-timer-driven transducer array (40kHz, 50% duty cycle) for acoustic cavitation/sonoporation
* **Drivetrain:** 4x high-torque 12V DC motors (224:1 gear reduction), 3D-printed traction tires, dual L298N H-bridge drivers
* **Power:** 11.1V 2200mAh 3S LiPo battery, actively recharged by two series-wired 6V solar panels
* **Chassis:** CNC-machined 1cm PVC baseplate (20cm x 30cm)

## Repository Structure
* `Code`: ESP32 firmware — navigation (yaw/heading calibration), traversal control, seeding mechanism, and full autonomous operation loop
* `3D Models`: Source/print files for the baseplate, field preparation compartment, seeding compartment, and chassis mounts
* `SonoSeeder.pdf`: Full project paper — literature review, mechanical/electrical design, control software breakdown, and self-validation results

## Self-Validation Summary
A prototype ultrasound subsystem was tested against a control group over a 5-day maize seedling trial:

| Day | Control (cm) | Treated (cm) | Gain |
|-----|-------------|--------------|------|
| 3   | 2.6         | 4.2          | +61.5% |
| 4   | 4.7         | 6.5          | +38.3% |
| 5   | 6.8         | 8.3          | +22.1% |

Full methodology and caveats are detailed in `SonoSeeder.pdf`.

## Licensing
No formal license has been applied to this repository yet. All rights reserved to the developers unless otherwise specified.

---
**Team Captain:** Hariz Zoran Farooq
**Team Vice-Captain:** Zoraiz Khalid
**Team Member:** Ali Ahmed
**Contact:** harizzoranfarooq@gmail.com
**Competition:** WRO International 2024, Future Innovators Category, Izmir, Türkiye — **Silver Medal**
**Contact:** harizzoranfarooq@gmail.com
**Competition:** WRO International 2024, Future Innovators Category, Izmir, Türkiye
