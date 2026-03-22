# Digital Alarm Clock using PIC16F877A

This repository contains an embedded systems mini-project for a Semester 6 course. It is a fully functional Digital Alarm Clock built using a **PIC16F877A Microcontroller** and a **DS3231 Real-Time Clock (RTC)** module.

## 🌟 Features

*   **Real-Time Clockkeeping:** Uses the highly accurate DS3231 RTC module (I2C) to keep track of the time and date.
*   **LCD Interface:** Displays the current time (`HH:MM:SS`) and the scheduled alarm time (`HH:MM`) on a 16x2 character LCD.
*   **Programmable Alarm:** Features a user-friendly interface with 5 push-buttons to set and toggle the alarm time.
*   **Audible Alert:** Triggers a piezoelectric buzzer when the alarm time matches the real time.

## 🛠️ Hardware Requirements

1.  **Microcontroller:** PIC16F877A
2.  **Oscillator:** 20MHz Crystal Oscillator
3.  **RTC Module:** DS3231 (I2C Protocol)
4.  **Display:** 16x2 Character LCD (HD44780 compatible)
5.  **Inputs:** 5x Tactile Push Buttons (with pull-up resistors enabled on Port B)
6.  **Output:** 5V Active Buzzer

## 🔌 Pin Mapping

### LCD Display (PORT D)
*   **RS:** RD2
*   **EN:** RD3
*   **D4:** RD4
*   **D5:** RD5
*   **D6:** RD6
*   **D7:** RD7

### Navigation Buttons (PORT B)
*   **Left Button (LB):** RB0 (Move cursor left)
*   **Middle Button (MB):** RB1 (Toggle/Enter alarm setup mode)
*   **Right Button (RB):** RB2 (Move cursor right)
*   **Upper Button (UB):** RB3 (Increase value)
*   **Bottom Button (BB):** RB4 (Decrease value)

### Miscellaneous
*   **Buzzer:** RD1
*   **DS3231 RTC:** Standard I2C pins (SCL: RC3, SDA: RC4)

## 💻 Software Prerequisites

*   [MPLAB X IDE](https://www.microchip.com/en-us/tools-resources/develop/mplab-x-ide)
*   [XC8 Compiler](https://www.microchip.com/en-us/tools-resources/develop/mplab-xc-compilers)

## 🚀 How to Build and Flash

1.  Open **MPLAB X IDE**.
2.  Go to `File > Open Project...` and select the `Alarm_Clock with PIC.X` directory.
3.  Ensure your XC8 compiler is configured in the project settings.
4.  Click **Build Project** (the hammer icon) to generate the `.hex` file.
5.  Use a programmer (like PICkit 3 or PICkit 4) to flash the generated hex file onto the PIC16F877A.
    *   *Note: If setting the time for the very first time, make sure `Set_Time_Date()` is uncommented in `main()`. Once set, comment it out and re-flash to avoid resetting the clock on every reboot.*

## 🎥 Demonstrations

Check out the included media files for hardware demonstrations:
*   [`Alarm Demo.mp4`](./Alarm%20Demo.mp4) - Shows the alarm setting process and the buzzer trigger.
*   [`final Mini project.mp4`](./final%20Mini%20project.mp4) - Overview of the completed physical hardware setup.
*   The project report can also be found in `21UG0623 21UG0618 final Report.pdf`.

## 📜 Credits & License
This project was developed as an academic embedded systems module (Semester 6). The base logic and LCD routines were inspired by [Circuit Digest](https://www.circuitdigest.com).