# SignalDrums - The Burner's Digital Message Board

A decentralized message board system using ESP32s in a mesh network. Designed for wide-area events like Burning Man, PlayaPost allows attendees to leave messages in the vastness of the playa.

## Getting Started

This guide will help you set up two PlayaPost terminals. You can extend it for more terminals by purchasing more of the necessary components.

### Prerequisites

- Familiarity with the Arduino IDE
- Basic knowledge of C/C++ for Arduino programming
- Knowledge of soldering

### Libraries & Software:

- **ESP-MESH**: Native support in the ESP32 for mesh networking. [Reference & Installation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/mesh.html)
- **GxEPD**: A library for e-paper displays, compatible with most popular e-paper modules. [Github Link](https://github.com/ZinggJM/GxEPD)
- **Keypad Library**: A library for interfacing matrix keypads. [Arduino Library Link](https://playground.arduino.cc/Code/Keypad/)
- **Arduino ESP32**: Necessary board definitions for programming the ESP32 with the Arduino IDE. [Github Link](https://github.com/espressif/arduino-esp32)

### Installation:

1. **Setting up Arduino IDE**: 
   - Install the Arduino IDE from [Arduino's website](https://www.arduino.cc/en/software).
   - Add ESP32 support: Go to `File > Preferences` and add `https://dl.espressif.com/dl/package_esp32_index.json` to the `Additional Boards Manager URLs` field.
   - Go to `Tools > Board > Boards Manager`, search for `ESP32`, and install.

2. **Installing Libraries**:
   - Open Arduino IDE and go to `Sketch > Include Library > Manage Libraries`.
   - Search for the mentioned libraries and install them.

### Assembly:

1. **Power**: Connect the solar panel to the TP4056 charger input and connect the battery to the respective terminals. Connect the TP4056 output to the ESP32's Vin (or 5V) and Ground.
2. **Display**: Connect the e-paper display to the ESP32 as per its datasheet. Common connections are Vcc, GND, SCK (to ESP32's SCK), MOSI (to ESP32's MOSI).
3. **Keypad**: Connect the rows and columns of the matrix keypad to the digital GPIO pins of the ESP32. Remember the pins for software configuration.
4. **LED & Buttons**: Connect LEDs and buttons to any digital GPIO pins of the ESP32. Note the pins for software configuration.

### Coding:

1. Set up the ESP-MESH configuration.
2. Use the GxEPD library to send messages to the e-paper display.
3. Set up button, LED, and keypad GPIO inputs/outputs in the code.
4. Handle messages, relaying, and TTL as per the network logic.
5. Implement a basic user interface for message input using the matrix keypad.

### Deployment:

1. After coding, compile and upload the sketch to the ESP32.
2. Place all components in the weatherproof box.
3. Deploy the terminals in your desired locations.

### Contribution:

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

## License

This project is open-source. Feel free to use, modify, and distribute.
