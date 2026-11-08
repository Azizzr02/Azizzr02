<div align="center">
  <img src="./assets/profile.png" width="132" alt="Portrait of Aziz Zouari">
  <h1>Aziz Zouari</h1>
  <p>Embedded Systems Engineer · Tunisia</p>
  <p>From sensor signals to firmware, Linux gateways, and live telemetry.</p>
  <p>
    <a href="https://www.linkedin.com/in/aziz-zouari/">LinkedIn</a>
    &nbsp;·&nbsp;
    <a href="mailto:Azizzouari@eniso.u-sousse.tn">Email</a>
    &nbsp;·&nbsp;
    <a href="https://github.com/Azizzr02?tab=repositories">Repositories</a>
  </p>
</div>

## 🧰 On my workbench

Firmware

![C, C++, STM32, Arduino, CMake](./assets/firmware.svg)

Linux &amp; gateways

![Linux, Yocto, Raspberry Pi, Python](./assets/linux.svg)

Connectivity &amp; tools

![Zigbee, MQTT, FastAPI, React, KiCad](./assets/connectivity.svg)

I work on MCU firmware, embedded Linux, and connected devices. I like following a signal all the way through a system, from an ADC sample or bus frame to a test result I can reproduce.

## 🔬 Featured build · STM32 ↔ Linux telemetry test bench

My final-year project at SEGULA Technologies ties a CAN-FD battery temperature emulator to a Raspberry Pi supervisor and a live dashboard.

```text
Analog input → STM32G0 firmware → CAN-FD → Raspberry Pi / SocketCAN
                                                    ↓
                                           DBC decode → Live dashboard
```

- [STM32 firmware](https://github.com/Azizzr02/BMS_STM32_Firmware) · TIM7 drives the 10 Hz update loop. The firmware filters ADC samples, evaluates temperature and fault states, sends FDCAN telemetry, and handles commands for fault injection and threshold changes.
- [Raspberry Pi supervisor and dashboard](https://github.com/Azizzr02/RPI-dashboard) · Linux receives CAN-FD frames via an MCP2517FD SPI controller. The FastAPI backend decodes frames using a DBC file and streams live readings to a React dashboard over WebSockets. The dashboard can also send commands back to the MCU.
- Verification · I checked the link using CAN loopback, `candump`, and logic-analyzer captures, and measured stable 10 Hz telemetry.

<p align="center">
  <a href="https://github.com/Azizzr02/RPI-dashboard">
    <img src="https://raw.githubusercontent.com/Azizzr02/RPI-dashboard/main/docs/images/telemetry.png" width="640" alt="Live CAN-FD telemetry in the Raspberry Pi dashboard">
  </a>
</p>

## 🌱 Currently learning · Zephyr RTOS

- [Zephyr course exercises](https://github.com/Azizzr02/zephyr-course) · My training fork includes a devicetree overlay, Kconfig, a ring-buffer module, and calculator and ring-buffer test suites.
- [Zephyr application workspace](https://github.com/Azizzr02/Zephyr-Workspace) · A template-based sandbox for studying `west` workflows, board configuration, producer/consumer threads, and MCUboot on STM32 Nucleo.

## 🛠 More projects

| Project | What it demonstrates |
| --- | --- |
| 🔌 [STM32 dual-board UART link](https://github.com/Azizzr02/Dual-Card-Data-Transmission-System-STM32-UART-) | Two STM32F4 boards exchange sensor values over interrupt-driven UART. The transmitter samples an analog input and the receiver mirrors LED states. |
| 🐧 [Yocto gateway and real-time motor control](https://github.com/Azizzr02/Adas-Project) | A team prototype with a custom Yocto layer, a Raspberry Pi UDP-to-CAN bridge, and an STM32F407 controller driving 50 Hz PWM. |
| 🌡️ [Temperature and gas monitor](https://github.com/Azizzr02/Temperature-and-Gas-Detector) | Arduino sensor-monitoring prototype with threshold logic, LED and buzzer alerts, and a circuit simulation. |
| 🎛️ [KiCad project and board templates](https://github.com/Azizzr02/kicad-project) | A project structure for organizing schematic and PCB revisions, with reusable board and worksheet templates. |
| 🎚️ [Python audio processing panel](https://github.com/Azizzr02/audio_processing_panel) | A Tkinter interface for recording, classification, text-to-speech, and real-time filtering and equalization. |

During my YUCCAINFO internship, I also worked on a Zigbee-to-MQTT sensor gateway. An STM32WB55 sent temperature, humidity, and vibration readings through a Raspberry Pi coordinator for live local monitoring.
