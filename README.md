# ShulkerBox - Minecraft Profile & Mod Manager

ShulkerBox is a lightweight, high-performance Windows desktop application built with C# and WPF. It acts as an instant profile switcher for Minecraft modifications, allowing players to organize, pack, and instantly hot-swap multiple mod setups with just a few clicks.

Inspired by the Shulker Box item from Minecraft, this app serves as an autonomous container storage for your modpacks, completely isolating your setups from conflicting with each other.

## Key Features

* **Two-Click Activation:** Instantly unpacks a selected box into your `%appdata%\.minecraft\mods` folder, automatically cleaning up previous setups.
* **Autonomous Profile Containers:** Mods are stored in dedicated local directories, preventing game crashes caused by mod overlap or version mismatch.
* **Smart Versioning & Tagging:** Add custom tags to your boxes (e.g., Forge, Fabric, 1.20.1, Optifine) to keep track of your modpack requirements.
* **WPF Data Converters:** Automatically parses cryptic `.jar` file names into human-readable mod titles directly inside the UI.
* **Shulker Profiles Sharing:** Export your profiles into independent `.shulker` package files to easily share your custom modpacks with friends.
* **Native Windows Shell Integration:** Automatically registers the custom `.shulker` extension in the Windows Registry with a dedicated icon.

## Project Architecture

The application is written strictly under the native **C# 7.3** specification and is highly optimized for legacy and modern **.NET Framework** runtimes. 

* **No Heavy Dependencies:** Avoids third-party JSON/YAML serialization frameworks by utilizing lightweight string-stream custom data indexing.
* **Resource Extraction Engine:** Dynamically extracts embedded binary icon resources (`.ico`) into the system data cache to provide cross-platform profile recognition.
* **Thread-Safe UI Operations:** Built entirely using asynchronous events to prevent application freezing during heavy file transfer operations.

## How It Works

1. **Pack Your Box:** Create a new profile, assign a version tag, and drop your `.jar` modification files into the box.
2. **Hot-Swap:** Select any created profile and click **Open in .minecraft**. The app handles directory cleaning and deployment instantly.
3. **Share:** Click **Share / Export** to generate a single `.shulker` file. Your friends can use the **Import Box** feature to play your pack instantly.

## Installation & Requirements

* **Operating System:** Windows 7/8/10/11
* **Runtime:** .NET Framework 4.7.2 or higher
* **Target Game:** Official Minecraft Launcher, TLauncher, Prism, or any standard directory wrapper.
