# ESP32 Wi-Fi Penetration Tool

A compact, open-source Wi-Fi penetration testing tool powered by the ESP32. This project is built for **educational and ethical hacking purposes**, allowing users to explore and understand wireless network vulnerabilities.

> **Note:** Use responsibly. This tool is intended for security researchers, students, and penetration testers on authorized networks only.

---

## Features

- **Deauthentication Attacks** – Disconnect targeted devices from Wi-Fi
- **WPA/WPA2 Handshake Capture** – Capture authentication handshakes for offline analysis
- **PMKID Capture** – Extract PMKID values without client interaction
- **Denial-of-Service Mode** – Target specific access points or broadcast interference
- **PCAP/HCCAPX Export** – Export capture files for tools like Hashcat or Wireshark
- **Web-Based Management AP** – Control the tool from a browser using your phone or laptop
- **Modular Architecture** – Easily extend with new attack types or interfaces

---

## Hardware Requirements

- ESP32 Development Board (e.g., ESP-WROOM-32)
- Micro-USB Cable
- External Antenna (optional, for better range)

---

# Usage Instructions for ESP32 Project

### 1. Build and Flash the Project onto ESP32
- Build the project as per the instructions in the repository.
- Flash the compiled code onto the ESP32 (DevKit or module).

### 2. Power On ESP32
- Power the ESP32 device to start the process.

### 3. Management AP Initialization
- The Management AP will start automatically after boot.

### 4. Connect to the Management AP
- **SSID:** ManagementAP
- **Password:** mgmtadmin

### 5. Access the Web Client
- Open a browser and visit: `http://192.168.4.1`
- You should see the web client interface to configure and control the tool.

### 6. Configure and Control the Tool
- Use the web client to configure and manage the tool as per your requirements.


---

## Installation

### 1. Clone the Repository
```bash
[git clone https://github.com/your-username/esp32-wifi-pen-tool.git](https://github.com/Hardpansara/esp32-wifi-penetration-tool)
```

### 2. Build with ESP-IDF

```bash
idf.py build
```

### 3. Flash with ESP-IDF

```bash
idf.py flash
```

### 4. Alternative: Flash Prebuilt Binary with esptool.py

If you don't want to set up the full ESP-IDF toolchain, you can use the precompiled binaries located in the **build/** folder:
```bash
esptool.py -p /dev/ttyS5 -b 115200 --after hard_reset write_flash --flash_mode dio --flash_freq 40m --flash_size detect 0x8000 build/partition_table/partition-table.bin 0x1000 build/bootloader/bootloader.bin 0x10000 build/esp32-wifi-penetration-tool.bin
```

On Windows you can use official Flash Download Tool.

---
Contributing
Feel free to contribute. Don't hestitate to refactor current code base. Please stick to Doxygen notation when commenting new functions and files. This project is mainly build for educational and demonstration purposes, so verbose documentation is welcome.

Disclaimer
This project demonstrates vulnerabilities of Wi-Fi networks and its underlaying 802.11 standard and how ESP32 platform can be utilised to attack on those vulnerable spots. Use responsibly against networks you have permission to attack on.

---

# Credits & Author

- **Developed by:** [risinek](https://github.com/risinek/esp32-wifi-penetration-tool)
- **Modified by:** Hard Pansara
- **GitHub:** [Hardpansara](https://github.com/Hardpansara)
- **LinkedIn:** [Hard Pansara](http://linkedin.com/in/hard-pansara-22582a288)
