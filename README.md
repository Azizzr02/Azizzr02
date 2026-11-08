<div align="center">
  <img src="./assets/profile.png" width="132" alt="Portrait of Aziz Zouari">
  <h1>Aziz Zouari</h1>
  <p><strong>Embedded Systems Engineer</strong></p>
  <p>MCU firmware · Embedded Linux · Connected devices</p>
  <p>
    <a href="https://www.linkedin.com/in/aziz-zouari/">LinkedIn</a>
    &nbsp;·&nbsp;
    <a href="mailto:Azizzouari@eniso.u-sousse.tn">Email</a>
  </p>
</div>

## What I build

I'm an Industrial Electronics engineering graduate based in Tunisia. I build firmware that reads sensors and controls peripherals, Linux gateways that collect and decode telemetry, and tools that help verify the complete hardware-to-software path.

| Focus | Hands-on work |
| --- | --- |
| **MCU firmware** | Embedded C/C++, STM32 and ARM Cortex-M, interrupt-driven UART, ADC, timers and PWM |
| **Embedded Linux** | Raspberry Pi and Yocto Linux, SocketCAN, Linux-based supervision and diagnostics |
| **IoT and connectivity** | STM32WB55, Zigbee, MQTT, UART, SPI and I²C |
| **Integration and verification** | Board bring-up, loopback tests, logic analyzer captures, and test documentation |

## Selected work

### STM32 and Linux telemetry test bench

For my final-year project at SEGULA Technologies, I built an STM32 firmware and Raspberry Pi supervision stack. The Linux gateway received and decoded CAN-FD frames, and a FastAPI service streamed telemetry to a React dashboard over WebSockets. I verified stable **10 Hz telemetry** using loopback tests, `candump`, and logic analyzer captures.

`Embedded C` · `STM32` · `Raspberry Pi` · `SocketCAN` · `CAN-FD`

### [Interrupt-driven STM32 communication](https://github.com/Azizzr02/Dual-Card-Data-Transmission-System-STM32-UART-)

Two STM32 boards exchange data over UART. The transmitter samples an analogue input with its ADC, and the receiver handles incoming data through interrupts and mirrors LED states.

`STM32` · `Embedded C` · `UART` · `ADC`

### Zigbee sensor gateway

At YUCCAINFO, I implemented Zigbee communication on an STM32WB55 for temperature, humidity, and vibration telemetry. I integrated a Raspberry Pi coordinator with Zigbee2MQTT to make sensor readings available to a local MQTT broker.

`STM32WB55` · `Zigbee` · `Raspberry Pi` · `MQTT`

### [Temperature and gas monitoring prototype](https://github.com/Azizzr02/Temperature-and-Gas-Detector)

An Arduino prototype that samples environmental sensors and triggers visual and audible alerts when readings cross thresholds.

`Arduino` · `C++` · `Sensor integration`

## Currently learning · Zephyr RTOS

I'm learning how Zephyr structures MCU firmware. My focus is on building and flashing with `west`, describing board peripherals with devicetree, configuring features with Kconfig, and using threads and work queues to organise sensor sampling and telemetry.
