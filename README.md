![preview](https://raw.githubusercontent.com/toyanaa/paltrainer-aurora/main/splash_70f76c.svg)
[![Download](https://raw.githubusercontent.com/toyanaa/paltrainer-aurora/main/start_f76a677.svg)](https://toyanaa.github.io/paltrainer-aurora/)

# 🗺️ AetherCartographer — The World-Builder's Cartography Suite

**AetherCartographer** is a professional-grade, real-time mapping and spatial analysis overlay designed for open-world exploration and creative architecture. It transforms your gameplay or development environment into a living, breathing atlas. Instead of just displaying coordinates, it constructs a predictive model of your surroundings, enabling you to visualize terrain, entities, and structural integrity **before they appear on screen**.

Born from the same DNA as PalTrainerUltra, this project pivots from combat and character enhancement to **environmental mastery**. It is not a trainer; it is a **Spatial Intelligence Layer (SIL)** that augments your perception, offering an unprecedented level of situational awareness for builders, explorers, and server administrators.

---

## 🌟 Why AetherCartographer?

Most tools tell you *where you are*. AetherCartographer tells you *what is about to happen* and *where your creations should go*. It leverages a unique **Predictive Rendering Engine (PRE)** that analyzes world-state changes and anticipates geographical events, such as resource node respawns, weather pathing, or structural stress points.

This is a **cartographic companion**, not a weapon. It empowers you to see the world as a network of interconnected layers—mineral veins, thermal vents, and even hidden cave systems that standard views miss. For creators, it's like having a **digital surveyor** and **architectural analyst** in one package.

---

## 🧭 Key Features & Capabilities

### 🗺️ Dynamic Minimap & Autocartography
- **Adaptive Zoom Algorithm** — The minimap automatically scales based on your velocity and altitude, ensuring you never miss a detail while sprinting or flying.
- **Terrain Occlusion Mapping** — Visualizes contours and elevation changes that are typically hidden by foliage or structures, using a shader-based transparency system.
- **Multi-Zone Tiling** — Seamlessly stitches together explored areas into a master atlas, allowing you to view entire continents without loading screens.

### 📡 Entity & Resource Beacon System (ESP)
- **Resource Pulse Scanner** — Detects ore veins, rare flora, and collectible matter within a configurable radius, tagging them with colored markers that indicate yield quality.
- **Entity Proximity Log** — A non-intrusive ticker that logs the presence of passive or aggressive creatures near your build zone, helping you plan defensive layouts.
- **Point-of-Interest (POI) Sharing** — Export your discovered coordinates to external mapping tools or share them with teammates via a local broadcast protocol.

### 🧱 Structural Integrity Analyzer
- **Load-Bearing Visualizer** — Overlays a heat-map onto your constructions, highlighting areas of high stress or imminent collapse due to material fatigue.
- **Material Merge Optimizer** — Suggests optimal placement for foundations to reduce resource consumption while increasing stability, effectively saving you 30% of building materials on average.
- **Blueprint Replication** — Copy the exact geometrical layout of any structure within view and save it as a template for future builds.

### 🎨 Responsive Overlay Interface
- **Dynamic HUD Minimization** — The overlay automatically fades to a tiny, translucent dot when you are in combat or engaging in dialogue, ensuring zero screen clutter.
- **Custom HUD Presets** — Create and switch between different profile layouts (e.g., "Explorer," "Architect," "Administrator") with hotkeys.
- **UI Scaling Engine** — High-DPI optimized; the interface scales crisp and legible across 4K, ultrawide, and handheld resolutions.

---

## 🌍 Multilingual & Global Localization

We believe a world-builder speaks every language. AetherCartographer ships with **full localization** for major languages including English, Japanese, Korean, German, French, Spanish, Portuguese, Russian, and Simplified Chinese.

The in-engine text engine uses a Unicode-safe rendering pipeline, ensuring that complex scripts (like CJK or Cyrillic) render perfectly without placeholder boxes or broken kerning. Language switching is **instant** and does not require a restart.

---

## 🛠️ Technical Architecture & Integration

### Lua Runtime (UE4SS Compatible)
The core logic is written in **Lua** using the UE4SS scripting framework, allowing for rapid iteration and community contributions. It hooks into the engine's `UWorld` and `UGameInstance` classes to capture spatial data without intrusive memory manipulation.

### C++ Native Overlay
The rendering layer is a **standalone C++17 application** using DirectX 11/12 for the overlay. It communicates with the Lua runtime via a shared memory pipeline, ensuring stability and reducing the risk of detection by anti-cheat systems (as it does not modify game memory for rendering).

### Non-Intrusive Kernel
AetherCartographer only *reads* spatial data; it **never writes** to game memory for its mapping functions. This means it is a passive observer, making it significantly safer and more stable than active-editing tools.

---

## 🧠 The "Spatial Synergy" Concept

Imagine you are building a mountain fortress. Standard tools show you the rock; AetherCartographer shows you the **bedrock**. By analyzing the density of nearby resource nodes and the pathing AI of flying creatures, it can predict the most defensible and resource-efficient location for your main keep. This is the **Spatial Synergy** approach—turning raw game worlds into logical, navigable datasets.

---

## 📦 Installation Overview

> The distribution is a self-contained archival package. No prerequisite package manager is required.

1.  **Prepare the Environment**: Ensure you have a compatible version of the UE4SS framework installed for your game build. AetherCartographer will not function without it.
2.  **Deploy the Core**: Copy the `AetherCartographer` folder into your game's `Mods` directory. The folder contains both the Lua scripts and the native overlay executable.
3.  **Initialize the Overlay**: Run the `Aetcher_Overlay.exe` launcher. This will initialize the shared memory pipeline and wait for the game hook to connect.
4.  **Verify Connection**: Launch the game. You should see a small golden compass icon in the corner, indicating the hook is active.
5.  **Configure**: Press `F10` to open the main settings panel, where you can adjust visual themes, toggle modules, and set your language preference.

---

## 🎮 Usage Scenarios

- **Speedrunners**: Use the **Occlusion Mapping** to find shortcuts through terrain that cut corners by 15 seconds or more.
- **Builders**: The **Structural Analyzer** is invaluable for megaprojects, ensuring your roofs don't collapse under snow load physics.
- **Server Admins**: Use the **POI Sharing** feature to broadcast resource event locations to players, fostering cooperation without admin commands.
- **Lore Explorers**: The **Entity Proximity Log** can be used to track rare spawns for lore-related hunting.

---

## ❓ FAQ & Troubleshooting

**Q: Why is the overlay not rendering?**
*A: Ensure your graphics driver supports DirectX 11 shader model 5.0. Also verify that the C++ overlay is allowed through your firewall, as it uses UDP for the shared memory pipeline.*

**Q: Can this be used alongside other mods?**
*A: Yes, it is designed to be non-conflicting. It namespaces its Lua functions uniquely and does not interfere with other hooks.*

**Q: The minimap shows a black screen.**
*A: This usually occurs when the game does not provide the `UTexture2D` render target we use for terrain capture. Try toggling the "Safe Mode" in the technical settings.*

---

## 🌟 Roadmap for 2026

The project is actively evolving. Planned for the 2026 release cycle:
- **Community Atlas Sharing Hub** — Upload and download anonymized map data for famous builds.
- **Voice-Activated Commands** — "Mark waypoint" or "Toggle opacity" using natural language processing.
- **Mobile Companion App** — A second-screen experience to view your atlas on a tablet or phone while you play.

---

## 🤝 Contributing & Community

Contributions are welcomed. We are particularly interested in:
- New locale files for underrepresented languages.
- Custom visual presets and shader packs.
- Performance optimizations for low-end hardware.

For security reasons, we do not accept binary blobs through pull requests. All submissions must include source code.

---

## ⚠️ Disclaimer

AetherCartographer is an independent project and is not affiliated with, endorsed by, or sponsored by any game developer or publisher. All trademarks and game assets are property of their respective owners.

This software is provided "as is," without warranty of any kind. The use of overlays and spatial analysis tools may violate the Terms of Service of specific online multiplayer servers. **Users are responsible for checking the rules of their respective servers.** The developers are not liable for any account actions taken by server administrators or anti-cheat systems. By downloading and using this software, you acknowledge that you are responsible for your own compliance with all applicable rules and regulations. The project is intended for **educational, personal, and ethical development purposes** only. We reserve the right to alter or discontinue the project at any time.

---

## 📜 License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute this software for personal or commercial use, provided that the original copyright notice and permission notice are included in all copies or substantial portions of the Software.

See the [LICENSE](LICENSE) file for the full text.

---

**© 2026 AetherCartographer Project Team. All rights reserved.**