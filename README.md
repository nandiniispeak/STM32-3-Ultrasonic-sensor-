# STM32 Triple Ultrasonic Sensor System

This repository contains an embedded C firmware project developed in **STM32CubeIDE** for an **STM32F103C8T6 (Blue Pill)** microcontroller. It reads distance data from three HC-SR04 ultrasonic sensors simultaneously and outputs the results over a virtual serial terminal.

 🛠️ Tools & Hardware Simulated
* **IDE:** STM32CubeIDE (HAL Library)
* **Simulator:** PICSimLab (Blue Pill Board + Spare Parts)
* **Microcontroller:** ARM Cortex-M3 (STM32F103C8T6)
* **Sensors:** 3x HC-SR04 Ultrasonic Distance Sensors (Front, Left, Right)

---

 📌 Pin Configuration (PICSimLab Setup)
To map the hardware correctly in the PICSimLab **Spare Parts** window, link the sensor pins to the following GPIOs on the Blue Pill:

* **Front Sensor:** Trigger -> `PA0` | Echo -> `PA1`
* **Left Sensor:** Trigger -> `PA2` | Echo -> `PA3`
* **Right Sensor:** Trigger -> `PA4` | Echo -> `PA5`
  
---

🚀 How to Run the Simulation

1. Compile the project in **STM32CubeIDE** to generate the `.bin` file.
2. Launch **PICSimLab** and select the **Blue Pill - stm32f103c8t6** board.
3. Open the **Spare Parts** window and add three ultrasonic sensors.
4. Configure the pin mappings as shown in the section above.
5. Go to **File -> Load Bin** and select the compiled binary file.
6. Open the **Virtual Terminal** (configured at `115200` baud rate) to view the real-time distance calculations in centimeters (`cm`).
