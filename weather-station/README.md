# Raspberry Pi Weather Station: End-to-End Project Context

## 🚀 Project Goal

**Build a fully-functional weather station using a Raspberry Pi, integrating hardware sensors, backend data/API services, and a live dashboard.**  
This project maximizes learning across hardware, Python, JS, REST APIs, async data flows, database design, and web deployment.  
*Primary purpose: Level up as a practical, world-class engineer.*

---

## 🛠️ Core Features and Requirements

- **Sensor Data Acquisition**
  - Temperature & Humidity via DHT22 (or DHT11, if no DHT22)
  - Barometric Pressure via BMP180 (or BME280)
  - All sensors use GPIO and I²C on the Raspberry Pi

- **Data Logging/Backend**
  - Python service to poll sensors at set intervals (every 30-60 sec)
  - Log data with timestamps to SQLite (or PostgreSQL if familiar)

- **REST API**
  - Expose recorded data and latest readings as JSON via Flask (Python) or Node.js/Express API
  - Endpoint examples:  
    - `/api/latest` for most recent readings  
    - `/api/history?from=...&to=...` for historical queries

- **Frontend Dashboard**
  - Simple HTML/JS frontend (vanilla or React)  
  - Fetches from REST API endpoints
  - Displays live charts (use Chart.js or similar for fast results)
  - Real-time UI updates (poll or WebSocket as stretch)

---

## 📦 Required Components

- **Raspberry Pi board** (any recent model, Pi 3/4/Zero W recommended)
- **MicroSD card** (16GB+)
- **DHT22/11 sensor** (humidity + temperature)
- **BMP180/BME280 sensor** (pressure)
- **Breadboard** & **jumper wires**
- **Pi power supply**
- **Case** (optional)
- **Active cooler** (optional)

---

## 📚 Learning Path/Step List

> **Each step can be requested and auto-completed with AI-in-the-IDE (Cursor)**

1. **Initial Pi Setup**
   - Burn Raspberry Pi OS to microSD, boot, enable SSH, connect to Wi-Fi or Ethernet
2. **Python Environment**
   - Install required libraries: `Adafruit_DHT`, `smbus2`, `Flask` or `Express` for Node.js
3. **Hardware: Sensor Wiring**
   - Connect DHT22/DHT11 and BMP180/BME280 to GPIO pins and test their output
4. **Sensor Read Script**
   - Python script to poll sensors, print values, and handle connection errors
5. **Database Logging**
   - Create SQLite db & write script to store readings with timestamps
   - Add periodic logging (via `cron` or persistent process)
6. **REST API Backend**
   - Create Flask or Node.js/Express API exposing sensor/query endpoints
7. **Frontend Dashboard**
   - Basic HTML/CSS/JS page to display current data and history graphs
8. **Live Data/Interactivity**
   - Implement polling or WebSockets for live updates in browser
9. **External API Comparison (Stretch)**
   - Integrate OpenWeatherMap or similar for forecast comparison
10. **Cleanup & Automation**
    - Set Pi up to run scripts/services on boot (systemd or `rc.local`)
    - Optional: Deploy/static host dashboard (Vercel, Pi, or cloud)

---

## 💡 Design Principles

- **No copy-paste black boxes**—code should be understood and iteratively improved
- **Budget-conscious**—cheapest working components and dev resources
- **Scalable**—foundations laid for potentially expanding to cloud, ML, more sensors

---

## 🤖 AI Usage Guidelines

- **Ask for step-by-step code, error explanations, and design feedback right in Cursor**
- **Explain wiring diagrams as code blocks or ASCII art for clarity**
- **Challenge AI for optimizations, edge case handling, or documentation for each script/module**
- **Lean on AI for quick bugfixes, test-driven iterations, or alternative stack suggestions**

---

## 📝 Project Outcomes

- Hands-on experience in full-stack, hardware-software integration, and practical engineering
- Portfolio-ready demo with extensibility (AI model potential, more sensors, deployment, etc.)

---

---
