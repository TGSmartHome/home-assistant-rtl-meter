# Home Assistant RTLAMR Gas & Water Meter Integration

This project integrates **gas and water meters** into Home Assistant using [RTLAMR](https://github.com/bemasher/rtlamr) and MQTT. It provides **real-time utility tracking** and integrates cleanly with the **Home Assistant Energy Dashboard**.

---

## 🏠 Features

- 🔌 MQTT-based smart meter readings using `rtlams2mqtt`
- 💧 Water usage tracking in **gallons (gal)**
- 🔥 Gas usage tracking in **cubic feet (ft³)**, with virtual sensor converting to **CCF**
- 📊 Daily, weekly, and monthly utility tracking
- ⚡ Compatible with the **Energy Dashboard**
- ✅ Clean single-file configuration (`configuration.yaml`)

---

## 📁 Repository Contents

- `configuration.yaml` – Home Assistant config:
  - MQTT sensors for raw meter values
  - Template sensors for cleaned/converted values
  - Utility meter setup for tracking usage over time

- `rtlams2mqtt.yaml` – Config for RTLAMR2MQTT to broadcast meter data over MQTT

Each of these files can be dropped directly into your setup with minimal modification.

---

## ⚙️ Energy Dashboard Integration

To view usage in Home Assistant's Energy dashboard:

- Add **`sensor.water_meter_clean`** as a water source (unit: gallons)
- Add **`sensor.gas_meter_ccf`** as a gas source (unit: CCF)

Make sure these sensors are updating with current data before adding.

---

## 🔧 Requirements

- RTL-SDR USB dongle
- [rtlams2mqtt](https://github.com/allangood/rtlams2mqtt)
- MQTT broker (e.g. Mosquitto)
- Home Assistant (any version with MQTT + template support)
- Compatible meters:
  - **Water:** R900 protocol
  - **Gas:** SCM/SCM+ protocol

---

## 🧑‍💻 Need Help?

If you need help setting this up, troubleshooting MQTT, or want a full Home Assistant configuration built:

📧 **Email:** flankerdevelopment@gmail.com  
🧑‍💼 **Upwork Profile:** https://www.upwork.com/freelancers/tgsmarthome

---

## 🪪 License

MIT License — free to use, modify, and share.
