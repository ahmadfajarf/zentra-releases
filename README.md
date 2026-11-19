<div align="center">

# Zentra Music

**A next-generation, high-fidelity music & music video streaming ecosystem engineered for Android and Windows Desktop.**

[![Android Release](https://img.shields.io/badge/Android-v2.7.4--stable-10B981?style=for-the-badge&logo=android&logoColor=white)](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-v2.7.4-stable.apk)
[![Windows Desktop](https://img.shields.io/badge/Windows-v2.0.0%20(Rust%20%2B%20Tauri%20v2)-118EE9?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-x64-setup.exe)
[![Audio Engine](https://img.shields.io/badge/Audio-48kHz%20Opus%20%2B%20Mastering%20DSP-FF2E54?style=for-the-badge&logo=musicbrainz&logoColor=white)](#signature-mastering-sound-engine-punchy--warm-dsp-chain)
[![Video Engine](https://img.shields.io/badge/Video-Up%20to%204K%20%2F%201080p%20HD-8B5CF6?style=for-the-badge&logo=youtube&logoColor=white)](#true-server-synced-hd4k-music-video-engine-144p--2160p)
[![Ad-Free](https://img.shields.io/badge/Experience-100%25%20Ad--Free-059669?style=for-the-badge)](#one-click-direct-downloads)

</div>

---

## One-Click Direct Downloads

All official release binaries are hosted directly on **[GitHub Releases](https://github.com/ahmadfajarf/zentra-releases/releases/latest)** with deterministic SHA-256 verification.

| Platform | Edition / Package | Version | Direct Download Link | Size | SHA-256 Checksum |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Android Mobile** | Signed APK (`Android 8.0+`) | `v2.7.4-stable` | [Download `Zentra-v2.7.4-stable.apk`](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-v2.7.4-stable.apk) | `5.58 MiB` (`5,851,360` B) | `7c2a4f6aad52745515ab0713c7bdba0ea5a39e9f8c7dbd20b12d31f8952a7084` |
| **Windows Desktop** | NSIS Setup Installer (`Rust / Tauri v2`) | `v2.0.0` | [Download `Zentra-Music-2.0.0-x64-setup.exe`](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-x64-setup.exe) | `3.34 MiB` (`3,498,490` B) | `93fda0a3c737c77583828a60dbde110fd2a00e9bc3c8fdbfb631ed91936dd8f9` |
| **Windows Desktop** | Standalone Portable (`Rust / Tauri v2`) | `v2.0.0` | [Download `Zentra-Music-2.0.0-rust-portable.exe`](https://github.com/ahmadfajarf/zentra-releases/releases/latest/download/Zentra-Music-2.0.0-rust-portable.exe) | `8.36 MiB` (`8,766,464` B) | `5cb7ca63fc1d095b043c2a2f1378b255073668744e0cd2f397112a3abf78d82d` |

---

## Architectural Highlights & Feature Deep-Dive

### Signature Mastering Sound Engine ("Punchy & Warm" DSP Chain)
- **Unified Studio Audio Priority:** Prioritizes native **48kHz High-Bitrate WebM Opus (`itag 251`)** across both standalone music tracks and music video streams, backed by automatic `itag 140` (M4A) failover.
- **Unattenuated `1.0f` PCM Headroom:** Feeds a clean, unchoked `1.0f` digital signal directly into the mastering stage across standalone tracks and music videos alike.
- **5-Stage Studio DSP Pipeline:**
  1. Always-on **`+4.8 dB` Mastering Pre-Amp** (`LoudnessEnhancer`)
  2. Dedicated **`60Hz` Sub-Bass Harmonic Exciter** (`BassBoost`)
  3. **5-Band Musical Equalizer** (`60Hz`, `230Hz`, `910Hz`, `3.6kHz`, `14kHz` with 9 studio presets & custom profiles)
  4. **3D Spatial Stereo Widener** (`Virtualizer`)
  5. **Soft-Knee Brickwall Mastering Limiter** for crisp, distortion-free headroom

### 3-Tier Adaptive Cold-Start Fast-Path (`< 800ms` Instant Playback)
- Engineered with a non-blocking **3-tier adaptive client waterfall** matching desktop & mobile playback cores:
  - **Cold Start:** Uses cipher-free native **`ANDROID_VR` / `IOS`** streams for sub-second first-track playback right after a fresh install or cache clear while `PoToken` BotGuard and `base.js` cipher engines warm up asynchronously in the background.
  - **Seamless Escalation:** Automatically promotes subsequent playback to authenticated web/TV profiles once background warmup completes, with zero UI-thread stalls.

### True Server-Synced HD/4K Music Video Engine (`144p` – `2160p`)
- Instant 1-tap switching between **Audio Track** and **Full-Bleed Music Video**.
- **`MergingMediaSource` Split-Stream Architecture:** Combines authentic server-reported adaptive video tiers (`144p` – `2160p` / `4K`) with `itag 251` Opus (or `itag 140` fallback) and self-healing `PoToken` recovery.

### Synchronized Lyrics, Smart Discovery & Music Recognition
- Real-time time-synced & plain lyrics across multiple lyric providers with optional translation.
- **ShazamKit-powered ambient music recognition** (Android) with persistent recognition history.
- Endless adaptive radio queues, sleep timer, library backup/restore, and **offline song downloads**.

### Ultra-Lightweight Rust + Tauri v2 Desktop Core (Windows)
- Rebuilt from the ground up in **Rust + Tauri v2** (replacing Electron) for near-instant cold launch, minimal RAM usage, and ~90% smaller binaries (`3.34 MiB` installer / `8.36 MiB` portable).
- Native **Windows System Media Transport Controls (`SMTC`)**, background system tray integration, local Rust HTTP Range/CORS media proxy, and QuickJS embedded cipher engine.

---

## System Requirements & Quick Installation Guide

<details open>
<summary><strong>Android (<code>Zentra-v2.7.4-stable.apk</code> — Android 8.0+)</strong></summary>

1. Download **`Zentra-v2.7.4-stable.apk`** from the [Direct Downloads](#one-click-direct-downloads) table above.
2. Open the downloaded `.apk` file on your Android device (**Android 8.0 Oreo / API 26** or newer).
3. If prompted by Android, enable **"Allow from this source"** (*Install unknown apps*) for your browser or file manager.
4. Tap **Install** and launch **Zentra**.

</details>

<details open>
<summary><strong>Windows 10 / 11 64-bit (<code>Zentra-Music-2.0.0-x64-setup.exe</code> / <code>Zentra-Music-2.0.0-rust-portable.exe</code>)</strong></summary>

- **Choose your edition:**
  - **`Zentra-Music-2.0.0-x64-setup.exe`** — Standard Windows installer with Start Menu & uninstall integration.
  - **`Zentra-Music-2.0.0-rust-portable.exe`** — Zero-install single executable ready to run from any folder or USB drive.
- **Runtime Requirement:** Uses the built-in **Microsoft Edge WebView2 Runtime** (pre-installed on Windows 11 and most updated Windows 10 systems; automatically bootstrapped by the installer if missing).
- **Windows SmartScreen Notice:** Because Zentra Music is an independent, self-published release without a commercial EV code-signing certificate, Windows Defender SmartScreen may display *"Windows protected your PC"* on first launch. Click **"More info"** -> **"Run anyway"** to launch safely.

</details>

---

## SHA-256 Integrity Verification

Verify any downloaded binary against the checksum table above before running:

**Windows PowerShell:**
```powershell
Get-FileHash .\Zentra-Music-2.0.0-x64-setup.exe -Algorithm SHA256
```

**Linux / macOS / Git Bash:**
```bash
sha256sum Zentra-v2.7.4-stable.apk Zentra-Music-2.0.0-x64-setup.exe Zentra-Music-2.0.0-rust-portable.exe
```
