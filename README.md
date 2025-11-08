# 💧 Water Quality Monitoring System (Arduino + Tinkercad)

### 🧾 Overview
This project measures and monitors **water quality parameters** such as **temperature**, **turbidity**, and **pH**, and detects the presence of **fish**.  
The readings are displayed on a **16x2 I2C LCD**, and alerts are given using **LEDs** and a **buzzer**.

---

### ⚙️ Components Used

| Component | Description | Pin Connection |
|------------|-------------|----------------|
| Arduino UNO | Main microcontroller | — |
| TMP36 Sensor | Measures temperature | A0 |
| Potentiometer | Simulates turbidity sensor | A1 |
| Potentiometer | Simulates pH sensor | A2 |
| Slide Switch | Fish detection | D7 |
| I2C LCD (16x2) | Displays sensor values | SDA → A4, SCL → A5 |
| LED (Cold) | Blue LED for low temp | D3 |
| LED (Normal) | Green LED for normal temp | D5 |
| LED (Hot) | Red LED for high temp | D6 |
| Buzzer | Sounds alert for turbidity | D8 |

---

### 🌡️ Parameters Monitored

| Parameter | Sensor | Description |
|------------|---------|-------------|
| **Temperature** | TMP36 | Displays temperature in °C |
| **Turbidity** | Potentiometer | Simulates clarity of water (100% = clear) |
| **pH Level** | Potentiometer | Simulates pH from 0 to 14 |
| **Fish Detection** | Switch | Detects presence of fish |

---

### 🔆 System Behavior

1. **Temperature Indication**
   - ≤10°C → **Blue LED ON (Cold)**
   - 10°C–60°C → **Green LED ON (Normal)**
   - >60°C → **Red LED ON (Hot)**

2. **Turbidity Alert**
   - If turbidity > 70% → **Buzzer ON**
   - Else → **Buzzer OFF**

3. **Fish Detection**
   - If fish detected (switch pressed):
     ```
     Fish Detected!
     
     ```
     (Displays for 2 seconds)

4. **LCD Display Example** T: 28.5C PH: 7.0
Turb: 60%
5. **Serial Monitor Output Example**
---Temp: 28.5 C | Turbidity: 60% | pH: 7.0 | Fish: Detected



