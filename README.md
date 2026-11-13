# STM32 Bare-Metal UART Driver

## 📌 Project Overview

This project implements a UART (Universal Asynchronous Receiver-Transmitter) driver for the STM32F429ZIT6 microcontroller using bare-metal register-level programming in Embedded C.

The driver configures the USART1 peripheral to establish serial communication between the microcontroller and a PC terminal without using STM32 HAL libraries.

## 🛠️ Hardware and Software Requirements

- Microcontroller: STM32F429ZIT6
- UART Peripheral: USART1
- TX Pin: PA9
- RX Pin: PA10
- Alternate Function: AF7
- Baud Rate: 115200 bps
- Clock: 16 MHz
- IDE: STM32CubeIDE
- Terminal: Tera Term

## ⚙️ Features

- Direct register-level peripheral configuration.
- GPIO configuration for UART alternate function.
- USART1 peripheral initialization.
- Baud rate configuration.
- UART data transmission using polling.
- UART data reception using polling.
- Serial communication with a PC terminal.

## 🏗️ UART Configuration

| Parameter | Configuration |
|---|---|
| USART Peripheral | USART1 |
| TX Pin | PA9 |
| RX Pin | PA10 |
| Alternate Function | AF7 |
| Baud Rate | 115200 |
| Clock Frequency | 16 MHz |
| BRR Value | 0x008B |
| Communication | Polling |

## 🔍 Implementation Details

### 1. GPIO Configuration
- Enable GPIOA peripheral clock.
- Configure PA9 and PA10 in alternate function mode.
- Select AF7 for USART1 communication.

### 2. USART Configuration
- Enable USART1 peripheral clock.
- Configure the baud rate using the USART_BRR register.
- Configure transmitter and receiver enable bits.
- Enable the USART peripheral.

### 3. Data Transmission
- Check the TXE (Transmit Data Register Empty) flag.
- Write the data into the USART data register.
- Wait for transmission to complete.

### 4. Data Reception
- Check the RXNE (Read Data Register Not Empty) flag.
- Read the received data from the USART data register.

## 📚 Concepts Learned

- ARM Cortex-M microcontroller programming.
- STM32 peripheral register configuration.
- GPIO alternate function configuration.
- USART communication protocol.
- Baud rate calculation.
- UART transmission and reception.
- Polling-based peripheral communication.
- Bare-metal Embedded C programming.

## 🚀 Future Enhancements

- Interrupt-driven UART communication.
- DMA-based data transmission and reception.
- Circular buffer implementation.
- UART error handling.

## 👩‍💻 Author

**Sneha B.**

Embedded C | STM32 | Bare-Metal Programming | Microcontrollers
