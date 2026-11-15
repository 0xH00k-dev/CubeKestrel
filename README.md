# CubeKestrel

Lightweight and stealthy client-side utility mod for **Minecraft 1.21 (Fabric)** featuring a deep panic mode (concealing the mod from in-game menus and mod lists), 5-second anticheat auto-calibration, and smart AutoWaterDrop.

---

## ⚙️ Installation
Installation instructions are also available at 0xH00K-dev.github.io/cheats/CubeKestrel/index_us.html
1. Install **Fabric Loader** for **Minecraft 1.21**.
2. Download **Fabric API** for your game version and the compiled `cubekestrel-1.0.0.jar` file from the [Releases](https://github.com) page.
3. Place both `.jar` files into your game's `mods` directory:
   * **Linux:** `~/.minecraft/mods/`
   * **Windows:** `%appdata%\.minecraft\mods\`
4. Launch the game and open **Options → Controls → Key Binds** — the **CubeKestrel** menu will appear right at the top of the list.

---

## 🛠️ Building from Source (Compilation)

### 1. Installing and Configuring Java 25
To build the project, make sure **JDK 25** is installed on your system (or placed inside the project folder).

* **Install on Linux (Ubuntu / Mint / Debian):**
  ```bash
  sudo apt update && sudo apt install openjdk-25-jdk -y
  ```
* **Install on Arch Linux:**
  ```bash
  sudo pacman -S jdk25-openjdk
  ```

To ensure Gradle uses **Java 25** (even if another version is set as default on your system), find its path with:
```bash
readlink -f $(which java)
```
Open **`gradle.properties`** in the project root and add the path to your JDK directory (everything before `/bin/java`):
```properties
org.gradle.java.home=/usr/lib/jvm/java-25-openjdk-amd64
```
*(Alternatively, if you placed the `java25` folder directly inside the project root, set `org.gradle.java.home=./java25`).*

### 2. Compiling to `.jar`
Open a terminal in the project root directory (where `gradlew` is located) and run the build:

```bash
chmod +x gradlew
./gradlew build
```

Once the build finishes with `BUILD SUCCESSFUL`, the compiled mod file will be located at:
```text
build/libs/cubekestrel-1.0.0.jar
```
*(Use the main `.jar` file without `-sources` or `-dev` suffixes — drop it straight into your `mods` folder).*

---

## 🎮 Key Features & Default Hotkeys

* **Panic Mode (`P`)** — Instantly disables all modules, hides the HUD, strips the custom tab from the Controls settings, and conceals the mod from the Fabric mod list. Press again to restore everything.
* **AC Auto-Calibration** — A button in the menu header that automatically tests server physics for 5 seconds to find and lock in safe speed and jump limits.
* **FullBright (`G`)** — Maximum visibility in caves and at night without potion effects.
* **PlayerESP (`H`)** — Highlights player outlines through walls.
* **Glass X-Ray (`X` / `Z`)** — Renders terrain as transparent glass with a searchable ore and block filter.
* **Trajectories (`Y`)** — 3D flight paths and landing markers for Ender Pearls, Bows, Crossbows, Potions, and Snowballs.
* **Speed (`V`) / HighJump (`B`)** — Adjustable movement speed and jump height multipliers (`1.1x` – `2.0x`).
* **AutoWaterDrop (`N`)** — Automatically pulls a water bucket from your hotbar or main inventory on falls of 4+ blocks, places water before impact, and picks it back up.
* **AutoFish (`J`)** — Automated bite detection, reel-in, and recast.
* **BowAimbot (`R`)** — Smooth FOV-based bow target tracking.

---

## 📄 License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPLv3)** — see the [LICENSE](LICENSE) file for details.

