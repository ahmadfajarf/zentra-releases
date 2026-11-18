<div align="center">

# Zentra Music

**Pure, 100% Ad-Free Music & Music Video Streaming Ecosystem for Android and Windows Desktop**

No ads. No subscriptions. No tracking. Native studio-grade audio DSP paired with up to 4K/1080p full-bleed music videos.

[![Latest Release](https://img.shields.io/badge/Releases-Download%20Latest-FF2E54?style=for-the-badge&logo=github)](https://github.com/ahmadfajarf/zentra-releases/releases/latest)
[![Android](https://img.shields.io/badge/Android-9.0%2B%20(v2.7.0)-10B981?style=for-the-badge&logo=android&logoColor=white)](https://github.com/ahmadfajarf/zentra-releases/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-10%2F11%20x64%20(v2.0.0%20Rust)-118EE9?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/ahmadfajarf/zentra-releases/releases/latest)

</div>

---

## Direct Downloads

All official release binaries are hosted on **[GitHub Releases](https://github.com/ahmadfajarf/zentra-releases/releases/latest)**. Always verify SHA-256 checksums after downloading.

| Platform | Package Type | Filename | Size | Requirements | SHA-256 Checksum | Download |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Android** | APK (`stable`) | `Zentra-v2.7.0-stable.apk` | `5.53 MiB` | Android 9.0+ | `168ff066c882003dc7e06830721559e87db8fabe5a98636d80eb7748c1f49ad0` | [Download APK](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-v2.7.0-stable.apk) |
| **Windows Desktop** | NSIS Installer (`Rust / Tauri v2`) | `Zentra-Music-2.0.0-x64-setup.exe` | `3.34 MiB` (`3,498,490` bytes) | Windows 10 / 11 (64-bit, WebView2) | `93fda0a3c737c77583828a60dbde110fd2a00e9bc3c8fdbfb631ed91936dd8f9` | [Download Installer](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-x64-setup.exe) |
| **Windows Desktop** | Portable App (`Rust / Tauri v2`) | `Zentra-Music-2.0.0-rust-portable.exe` | `8.36 MiB` (`8,766,464` bytes) | Windows 10 / 11 (64-bit, zero install) | `5cb7ca63fc1d095b043c2a2f1378b255073668744e0cd2f397112a3abf78d82d` | [Download Portable](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-rust-portable.exe) |

---

## What's New in Desktop `v2.0.0` (Native Rust / Tauri v2)

- **~90% Smaller Desktop Footprint:** Rebuilt from Electron (`v1.1.0`, ~79–88 MiB) to native **Rust + Tauri v2 + WebView2** — delivering a **`3.34 MiB`** installer and an **`8.36 MiB`** standalone portable executable.
- **Instant Cold-Start Playback (`< 400ms`):** Native adaptive client waterfall + persistent public cipher cache starts audio/video playback immediately without blocking on startup warmup, paired with an isolated offscreen BotGuard PoToken worker (`potoken_worker`) for zero UI-thread freezes.
- **Studio-Grade Audio & "Gurih & Punchy" 5-Stage DSP:** High-bitrate **48kHz Opus (`itag 251`)** streaming piped through a 5-band parametric Equalizer, Sub-Bass Boost, Virtualizer, Loudness Normalization (`-14.0 LKFS`), and hard limiter.
- **Full-Bleed Music Video Streaming (`144p` – `2160p` / `4K`):** Synchronized adaptive video + Opus audio via a local Rust Axum `127.0.0.1` HTTP Range/CORS proxy, clean Song/Video stage switching, and timed video captions.
- **Embedded QuickJS Cipher + Multi-Chunk Offline Downloads:** Built-in Pure-Rust/QuickJS YouTube player decipherer, range-chunked offline download manager with instant offline playback and folder sync, External Playlist Sync (Spotify / YouTube Music / Apple Music), Synchronized Multi-Source Lyrics, and QRIS community support.

---

## Installation Notes

### Android (`Zentra-v2.7.0-stable.apk`)
1. Download `Zentra-v2.7.0-stable.apk` from [Releases](https://github.com/ahmadfajarf/zentra-releases/releases/latest).
2. Open the `.apk` file on your Android device (Android 9.0+).
3. If prompted, allow **"Install unknown apps"** for your browser or file manager, then tap **Install**.

### Windows (`Zentra-Music-2.0.0-x64-setup.exe` / `Zentra-Music-2.0.0-rust-portable.exe`)
- Choose **`Zentra-Music-2.0.0-x64-setup.exe`** for a standard Start Menu & desktop installation, or **`Zentra-Music-2.0.0-rust-portable.exe`** to run directly with zero installation.
- **Windows SmartScreen Notice:** Because Zentra Music is an independent, self-published release without a commercial EV code-signing certificate, Windows Defender SmartScreen may display *"Windows protected your PC"* on first launch. Click **"More info"** -> **"Run anyway"** to launch safely.
