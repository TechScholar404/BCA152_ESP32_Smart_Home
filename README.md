# BCA152 ESP32 Smart Home

A smart home prototype built on ESP32 and ESP RainMaker: a relay-controlled
smart plug and an environmental multisensor, both controllable from a mobile
app and Alexa.

## Features

- Smart plug: on/off from the app and a physical button, plus schedules and scenes
- Multisensor: temperature (BME280) and light (TSL2561), reported every 10 seconds
- Optional SSD1306 OLED showing time, readings, and cloud status
- Automation: for example, "if light is above X, turn the plug off"
- Alexa voice control
- Over-the-air firmware updates through ESP RainMaker

## Hardware

| Device | Board | Parts |
|---|---|---|
| Plug | ESP32 DevKit | 2-channel relay (channel 1 used), test load |
| Multisensor | ESP32-S3 DevKit | BME280, TSL2561, SSD1306 OLED (optional) |

## Project structure

| Folder | Purpose |
|---|---|
| `plug/` | Smart plug firmware |
| `sensor/` | Multisensor firmware |
| `ch9_common/` | Shared classes (AppDriver, AppNode) |
| `components/` | Third-party libraries (esp-idf-lib, esp-rainmaker submodule) |
| `docs/` | Wiring, setup, and test documentation |

## Getting started

    git clone --recurse-submodules https://github.com/TechScholar404/BCA152_ESP32_Smart_Home.git
    cd BCA152_ESP32_Smart_Home

Build each project from an ESP-IDF terminal:

    cd plug
    idf.py set-target esp32
    idf.py build

    cd ../sensor
    idf.py set-target esp32s3
    idf.py build

## Acknowledgments

Based on Chapter 9 of *Developing IoT Projects with ESP32, 2nd Edition*
(Packt Publishing), used under the MIT License. See [NOTICE.md](NOTICE.md).

## Author

TechScholar404, BCA152 course project
