# 📡 AirbreakerX (v1.0)

**AirbreakerX** is a high-performance C++20 utility for low-level Wi-Fi network auditing (WPA/WPA2/WPS), optimized for Kali NetHunter on mobile devices.

## 🚀 Key Features
* **Monitor Mode:** Software-based conversion of external USB adapters to monitor mode.
* **Smart Scanning:** Automated background channel hopping during airwave scanning.
* **Deauth Injection:** Generates and injects raw deauthentication frames to disconnect target clients.
* **Handshake Capture:** Intercepts and validates 4-way EAPOL handshakes, saving captures to `.pcap` files.
* **WPS-Pinocchio:** Intelligent state machine for online WPS PIN brute-forcing with built-in WPS Lock bypass/protection.

## 📦 Installation & Build
Install the required dependencies for handling raw packets, then build the binary using CMake with `-O3` compiler optimization:

```bash
sudo apt update && sudo apt install build-essential cmake libpcap-dev
mkdir build && cd build
cmake .. && make
```

The compiled binary will be placed inside the `build` directory.

## 🦹 Usage
Execution strictly requires superuser (root) privileges to grant the antenna chipset access to raw sockets:

```bash
sudo ./AirbreakerX
```

After launching, an interactive text menu will open. On your first run, select **Option 1** to set your wireless interface (e.g., `wlan1`) into Monitor Mode.

## ⚠️ Disclaimer
This tool is created exclusively for educational purposes and authorized penetration testing. The author assumes no liability for any misuse or damage. Conduct audits only on networks you own or have official written permission to test.
