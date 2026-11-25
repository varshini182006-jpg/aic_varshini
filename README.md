# aic_varshini
# ☀️ Solar Panel Voltage Tracker

A low-cost solar panel voltage monitoring prototype using an ESP8266, a voltage divider and an I2C LCD to display measured voltage in real time.

## 📌 Overview
This project measures the solar panel output voltage using the ESP8266's built-in ADC. A voltage divider scales the panel output to a suitable ADC input range. The microcontroller processes the reading and displays the voltage on a 16×2 LCD through I2C.

## 🎯 Objectives
- Monitor solar-panel output voltage.
- Use the ESP8266 ADC and a voltage divider for measurement.
- Display voltage readings on a 16×2 LCD using I2C.
- Keep the monitoring design simple and cost-effective.

## 📷 Prototype
![Solar Panel Voltage Tracker prototype](images/prototype/prototype.jpg)

*Figure 1: Prototype showing the solar panel, ESP8266, LCD and power-supply board. The LCD shown in the photograph displays 5.01.*

## 🧩 Components

| Component | Specification (as stated in report) | Purpose |
|---|---|---|
| Solar panel | 10 W, 12 V polycrystalline | Solar source |
| IoT module | ESP8266 development board | Analog reading and processing |
| LCD | 16×2 HD44780 with backlight | Display voltage |
| Transformer | 230 V to 12 V, 1 A | Power supply circuit |
| Resistors | 220 Ω, 1/4 W | Circuit components |
| Capacitors | 100 µF, 25 V electrolytic | Circuit components |
| LEDs | 5 mm, red/green | Indicators |

![Components list](images/components/components-table.jpg)

*Figure 2: Components table supplied with the project report.*

## 🏗️ System Architecture
```text
Solar Panel
    │
    ▼
Voltage Divider
    │
    ▼
ESP8266 ADC ──► Voltage Processing
                    │
                    ▼
                 I2C LCD
                    │
                    ▼
             Voltage Readout
```

## ⚙️ Working Principle
1. The solar panel generates a DC output.
2. A voltage divider scales the output for the ESP8266 ADC input.
3. The ADC samples and digitizes the analog signal.
4. The program converts the ADC reading to a voltage estimate.
5. The voltage reading is shown on the LCD through I2C.

## 🔌 Circuit Diagram
The actual project circuit diagram has not been included in this repository package yet. Add it to `images/circuit-diagram/` and update the link below.

<!-- Uncomment after adding the diagram:
![Solar Panel Voltage Tracker circuit](images/circuit-diagram/solar-voltage-circuit.jpg)

*Figure 3: Circuit diagram of the voltage measurement and display system.*
-->

See [`images/circuit-diagram/README.md`](images/circuit-diagram/README.md) for instructions. The 555 timer schematic shared separately was not included because it does not match the described solar voltage tracker.

## 💻 Software
- Arduino IDE
- ESP8266 board support package
- Embedded C/C++
- I2C LCD library (compatible library required for the LCD module)

## 📊 Demonstration
The provided prototype photograph shows the assembled hardware and a voltage display reading of 5.01. This is a sample reading visible in the photograph, not a general performance or accuracy claim.

## 🌱 Applications
- Basic solar panel voltage monitoring
- Small solar demonstrations and educational prototypes
- Home-scale solar monitoring concepts

## 🚀 Future Enhancements
- Remote monitoring via IoT/cloud dashboard
- Add current and power measurements
- Mobile alerts and historical logging
- Further solar tracking functionality

## 👥 Team
- Shakthi K — 8115U24EC101
- Varshini S — 8115U24EC119
- Yukashini B — 8115U24EC123
- Shree Vidharshana S — 8115U24EC104

**Guide:** Mrs. N. Srividya, M.E., (Ph.D.), Assistant Professor/ECE

**Institution:** K. Ramakrishnan College of Engineering (Autonomous), Samayapuram, Trichy.

## 📚 References
1. Green, M. A. *Solar Cells: Operating Principles, Technology, and System Applications*. Prentice Hall, 1982.
2. Esram, T., & Chapman, P. L. “Comparison of Photovoltaic Array Maximum Power Point Tracking Techniques.” *IEEE Transactions on Energy Conversion*, vol. 22, no. 2, 2007, pp. 439–449.
3. Liu, B. Y. H., & Jordan, R. C. “The Interrelationship and Characteristic Distribution of Direct, Diffuse and Total Solar Radiation.” *Solar Energy*, vol. 4, no. 3, 1960, pp. 1–19.

## 📁 Repository Layout
```text
Solar-Panel-Voltage-Tracker/
├── README.md
└── images/
    ├── prototype/
    │   └── prototype.jpg
    ├── circuit-diagram/
    │   └── README.md
    └── components/
        └── components-table.jpg
```
mmmmm
