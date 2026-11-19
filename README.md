<div align="center">

# Zentra Music

**An ad-free, high-fidelity music & HD music video streaming experience built for Android and Windows Desktop.**

[![Android Release](https://img.shields.io/badge/Android-v2.7.4-10B981?style=for-the-badge&logo=android&logoColor=white)](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-v2.7.4-stable.apk)
[![Windows Desktop](https://img.shields.io/badge/Windows-v2.0.0-118EE9?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-x64-setup.exe)
[![Ad-Free](https://img.shields.io/badge/Experience-100%25%20Ad--Free-059669?style=for-the-badge)](#one-click-direct-downloads)
[![License](https://img.shields.io/badge/License-GPL--3.0-FF2E54?style=for-the-badge)](./LICENSE)

</div>

---

## One-Click Direct Downloads

All official release binaries are hosted on **[GitHub Releases](https://github.com/ahmadfajarf/zentra-releases/releases/latest)** with deterministic SHA-256 verification.

| Platform | Package | Version | Direct Download Link | Size | SHA-256 Checksum |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Android Mobile** | Signed APK (`Android 8.0+`) | `v2.7.4` | [Download `Zentra-v2.7.4-stable.apk`](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-v2.7.4-stable.apk) | `5.61 MiB` (`5,884,100` B) | `72f3a40aea9d93d810de51109c36f6035a5e5905ce3cca4b1cb9c0d840323cf` |
| **Windows Desktop** | Setup Installer (`64-bit`) | `v2.0.0` | [Download `Zentra-Music-2.0.0-x64-setup.exe`](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-x64-setup.exe) | `3.34 MiB` (`3,498,490` B) | `93fda0a3c737c77583828a60dbde110fd2a00e9bc3c8fdbfb631ed91936dd8f9` |
| **Windows Desktop** | Standalone Portable (`64-bit`) | `v2.0.0` | [Download `Zentra-Music-2.0.0-rust-portable.exe`](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-rust-portable.exe) | `8.36 MiB` (`8,766,464` B) | `5cb7ca63fc1d095b043c2a2f1378b255073668744e0cd2f397112a3abf78d82d` |

---

## Core Features

- **Ad-Free Music & HD Music Video Streaming:** Seamless 1-tap switching between Song and Music Video with background playback.
- **Real-Time Synced Lyrics & Translation:** Fast multi-source synced & word-level lyrics with instant translation.
- **Studio Audio Equalizer & Sound Enhancement:** Built-in 5-band Equalizer, Bass Boost, and 3D Spatializer.
- **Offline Downloads & Smart Playlists:** Save songs offline, import playlists (Spotify / YouTube Music), sleep timer, and playback speed control.
- **Music Recognition & In-App Auto-Update:** Ambient song identification and seamless 1-tap app updates.
- **Cross-Platform Ecosystem:** Native Android app and lightweight Windows Desktop app (Setup & Portable).

---

## Quick Installation & Integrity Verification

### Android (`Android 8.0+`)
1. Download **`Zentra-v2.7.4-stable.apk`** from the downloads table above.
2. Open the `.apk` file on your Android device and allow **Install unknown apps** if prompted.
3. Tap **Install** and launch **Zentra**. Future releases update automatically in-app.

### Windows (`Windows 10 / 11 64-bit`)
- Run **`Zentra-Music-2.0.0-x64-setup.exe`** for a full Start Menu installation, or extract and launch **`Zentra-Music-2.0.0-rust-portable.exe`** anywhere with zero installation.
- Uses the built-in **Microsoft Edge WebView2 Runtime**. If Windows SmartScreen appears on first launch, select **More info** -> **Run anyway**.

### SHA-256 Verification
```powershell
Get-FileHash .\Zentra-v2.7.4-stable.apk -Algorithm SHA256
```
```bash
sha256sum Zentra-v2.7.4-stable.apk Zentra-Music-2.0.0-x64-setup.exe Zentra-Music-2.0.0-rust-portable.exe
```

---

## Credits & Acknowledgements

Zentra Music gratefully acknowledges the inspiration, open-source ecosystems, and services behind these communities and platforms:

- **SimpMusic**
- **Metrolist**
- **BitChord**
- **Mochi**
- **YouTube Music (YTM)**
- **Google**

---

## Disclaimer & Legal Notice

- Zentra Music is an independent, non-commercial open-distribution client developed for personal and educational use.
- This project is **not affiliated with, endorsed by, or officially connected to Google LLC, YouTube, or YouTube Music**.
- All trademarks, logos, audio tracks, music videos, artwork, and lyrics remain the sole property of their respective copyright owners.
- Zentra does not host or distribute any copyrighted media files; all content is streamed directly from public third-party sources. Users are responsible for complying with applicable local laws and platform Terms of Service.

---

## License

This distribution repository and project notices are provided under the **GNU General Public License v3.0 (GPL-3.0)**. See [`LICENSE`](./LICENSE) for the full license text.
