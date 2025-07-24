# Heater_ControlSystem

# Heater Control System

## Overview

This project is a basic heater control system implemented on Mega Arduino (using Wokwi). It monitors temperature using a DS18B20 sensor and controls a simulated heater based on preset thresholds.

## Features

- States: Idle, Heating, Stabilizing, Target Reached, Overheat
- Automatic heater control based on temperature
- Serial logging for temperature, state, and heater status
- Easy to test using Wokwi simulator
- Modular and readable C++ code

## Components Used

- DS18B20 Temperature Sensor
- Microcontroller (Arduino Mega )
- Relay (simulated as digital output)
- Serial Monitor (for logging)

## How It Works

1. The system starts in **Idle** state.
2. When temperature crosses the heating threshold, it goes to **Heating**.
3. Once close to the target, it enters **Stabilizing**.
4. When target temperature is reached, the heater is turned off.
5. If temperature exceeds safety limits, it enters **Overheat** and shuts off the heater.

## Thresholds 

- **IDLE**          :- Temperature < 23.0°C  
                      Heater is OFF, waiting for heating condition.

- **HEATING**       :- Temperature ≥ 23.0°C and < 25.0°C  
                      Heater is ON to raise the temperature.

- **STABILIZING**   :- Temperature ≥ 23.0°C and ≤ 25.0°C  
                      Fine-tuning phase; heater remains ON.

- **TARGET_REACHED**:- Temperature > 25.0°C and ≤ 27.0°C  
                      Desired temperature range reached; heater is OFF.

- **OVERHEAT**      :- Temperature > 30.0°C  
                      Critical temperature exceeded; heater is turned OFF immediately.


## How to Run (Wokwi)

1. Open `https://wokwi.com/`
2. Paste the code into the editor.
3. Connect the DS18B20 sensor in Wokwi or as per circuit diagram.
4. Run the simulation and observe the serial monitor.

## Files

- `main.ino` – Main Arduino code
- `README.md` – This file

## Author

**Muthahar**  
For upliance.ai Internship Assignment
