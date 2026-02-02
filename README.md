# ESP32-Smart-Access-Control-IoT
An ESP32-based Smart Access Control System integrating RFID authentication, multi-sensor monitoring (DHT, Ultrasonic, PIR), and a remote management Web Dashboard.


## Featured Demo: IoT Smart Environment Monitor
This project demonstrates a complete end-to-end IoT solution that bridges the physical world with the web. It showcases the ability to capture real-time data from hardware and visualize it instantly.

### System Architecture
1.  **Edge Layer (ESP32 / MicroPython)**
    -   Devices collect environmental data (Temperature, Humidity) using sensors like **DHT11**.
    -   Data is serialized (JSON) and published via **MQTT**.
    -   *Key Files: `MicroPython/dht11_sensor.py`, `MicroPython/mqtt_pub.py`*

2.  **Network & Protocol Layer**
    -   Message exchange is handled by an MQTT Broker.
    -   **WebSockets** support allows web clients to listen to IoT topics directly.
    -   *Key Files: `MicroPython/wifi_connect.py`*

3.  **Visualization Layer (HTML5 / OpenLayers)**
    -   A web-based dashboard subscribes to relevant MQTT topics (`mqws`).
    -   Device locations and status are updated in real-time on an interactive map using **OpenLayers**.
    -   *Key Files: `HTML/mqws_olmap.html`, `HTML/mqws_json.html`*

## Project Structure

### Communication Protocols & Networking
- **ChatRoom/**: Simple Chat Room implementation (Python Client/Server).
- **CoAP/**: CoAP (Constrained Application Protocol) examples, including GET and PUT request implementations.
- **Socket/** & **Python/socket_*.py**: Basic Socket Programming examples (TCP/IP).
- **HTML/**: Web Client examples integrating with MQTT (`mqws` likely refers to MQTT over WebSocket) and OpenLayers map applications.

### IoT & Microcontrollers
- **MicroPython/**: MicroPython scripts for ESP32/ESP8266.
  - Features include: BLE communication, WiFi connection, sensor reading (DHT11, RFID RC522, Ultrasonic), OLED display, Servo motor control, MQTT Pub/Sub, etc.
- **ESPhome/**: ESPHome YAML configuration files for quickly integrating ESP32 devices into Home Assistant (Sensors, Switches, Lights, Displays, etc.).

### Backend & Automation
- **NodeJS/**: Basic Node.js examples and server tests.
- **NodeRED/**: Node-RED flow files and settings for visual flow-based development (located under `venv2025`).
- **Python/**: Various Python utilities and test scripts.
  - Includes: Font processing (`FontDump`, `SysFont`), Scrolling text display (`Marquee`), REST Server/Client, MQTT testing, etc.

### Others
- **folder-project/**: A TypeScript project template structure.
- **MapData/**: JSON data used for map applications.
