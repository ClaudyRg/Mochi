# 🍡 Mochii (The Intelligent Dynamic Notch)
### *Next-Generation Fluid Notch Overlay & Desktop Companion for Windows 11* - *Currently doing a full migration to Rust.*

<div align="center">
  <h1>✨ MOCHII v1.2.1 ✨</h1>
  <p><i>"The ultimate dynamic island desktop companion, blending fluid ergonomics, living mascot physics, and real-time Windows intelligence."</i> 💫</p>

  <p align="center">
    <a href="https://github.com/ClaudyRg/Mochi"><img src="https://img.shields.io/badge/Tauri-v2-FFC131?style=for-the-badge&logo=tauri&logoColor=black" alt="Tauri v2"></a>
    <a href="https://github.com/ClaudyRg/Mochi"><img src="https://img.shields.io/badge/Rust-Native_Backend-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust"></a>
    <a href="https://github.com/ClaudyRg/Mochi"><img src="https://img.shields.io/badge/React-19.0-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"></a>
    <a href="https://github.com/ClaudyRg/Mochi"><img src="https://img.shields.io/badge/TypeScript-5.7-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"></a>
    <a href="https://github.com/ClaudyRg/Mochi"><img src="https://img.shields.io/badge/TailwindCSS-v4-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind"></a>
    <a href="https://github.com/ClaudyRg/Mochi"><img src="https://img.shields.io/badge/Windows-Win32_%26_WinRT-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Native"></a>
  </p>
</div>

---

## 🪐 Overview

**Mochii** is a native Windows 10 & Windows 11 **Living Notch & Dynamic Island Desktop Companion** crafted for power users, developers, and aesthetics enthusiasts. Powered by a lightweight **Tauri v2 + Rust** native backend alongside **React 19**, **TypeScript**, and **Tailwind CSS**, Mochii transforms the top bezel of your monitor into an organic, interactive command hub.

Equipped with pixel-accurate click-through transparency, Mochii stays completely out of your way until you hover, scroll, drag files, or receive notifications. From real-time WhatsApp push notification banners to live synced lyrics, daily wellness trackers, Bluetooth peripheral battery peeks, and an adorable living mascot, Mochii redefines the desktop experience on Windows.

---

## 🚀 Key Features & Architectural Highlights

### 🫧 1. Living Mascot ("Mochii Eyes") & Organic Fluid Island
*   **Expressive Living Mascot:** Features Mochii, an animated desktop companion with glowing pill eyes, one-eye wink, playful boing-boing bounce, and a dynamic `ω` cat mouth.
*   **Startup Drop-In & Hold:** Smoothly drops into the top bezel on launch and stays in mascot idle mode for 3 seconds before transitioning into active media/status mode.
*   **Unified Ambient Aurora:** Shimmers with a seamless horizontal Blue → Indigo → Violet → Pink bottom aurora glow in idle state.

### 💬 2. Real-Time WhatsApp & Windows Notification Banner
*   **Zero-Latency Native Watcher:** Intercepts incoming WhatsApp and Windows toast notifications directly from the Rust WinRT / database watcher.
*   **Offline Profile Avatars:** Caches sender profile pictures locally so avatars render crisply inside the notch without external network failures.
*   **Quick Reply & Action Controls:** Hover over incoming notifications to expand and reply or jump straight into the conversation.

### 🎵 3. Now Playing Deck & Split Synced Lyrics Island
*   **Universal Windows GSMTC Sync:** Seamlessly tracks Spotify, Apple Music, YouTube / Chrome / Edge, VLC, and local players with zero API keys required.
*   **Dynamic Collapsed Lyrics Pill:** Displays the active lyric line cleanly inside the collapsed notch with smooth width morphing.
*   **Full Split Synced Lyrics:** Powered by **LRCLIB** with clickable karaoke-synced lines, interactive seek bar, and album art color extraction.

### ⚡ 4. Productivity Hub & Daily Wellness Suite
Effortlessly switch between pages via mouse wheel scroll, `<` / `>` pagination controls, or numeric hotkeys:
1.  **Music Deck:** Media playback controls, interactive seek timeline, and split synced lyrics toggle.
2.  **Focus & Pomodoro:** 4-round focus & break timer with animated progress bar and finish-time preview.
3.  **Prayer Times:** Automatic daily prayer schedule (**Fajr, Dhuhr, Asr, Maghrib, Isha**) with live countdown via Aladhan API.
4.  **Hydration Tracker:** Daily water intake logger (`ml` & glasses) with customizable bottle size and gentle reminders.
5.  **TodoList:** Minimalist daily task tracker with scheduled reminders, completion counters, and quick add/edit pills.
6.  **Widgets & Hardware HUD:**
    *   **This Week Calendar:** 7-day compact schedule strip with task indicators.
    *   **Bluetooth & System Battery:** Real-time battery ring and peripheral status detection (including earbuds/headsets via Windows PnP & Bluetooth watchers).
7.  **Shelf & Clipboard History:** Universal drag-and-drop file/folder shelf paired with automatic clipboard history cards.

### 🔄 5. Standalone Settings & In-App Updater
*   **Dedicated Settings Window:** Manage General, Music & Lyrics, Notifications, To-do, Pomodoro, Water, Prayer, Shelf, and HUD & Popups cleanly from the system tray or notch header.
*   **One-Click Software Updates:** Check for new GitHub Releases and download & install updates directly from **Settings → About → Check for updates**.

---

## ⚙️ Interactive Controls & Shortcuts

| Action | Control |
| :--- | :--- |
| **Expand Notch** | Hover or click the top-center notch pill |
| **Collapse Notch** | Move cursor outside the notch or press `Esc` |
| **Switch Pages** | Mouse wheel scroll over notch, `<` / `>` buttons, or keys `1`–`7` |
| **Pin to Shelf** | Drag any file or folder over the top-center notch |
| **Open Settings** | Click the gear icon in the expanded notch or right-click the Tray icon |
| **Check for Updates** | Open **Settings → About → Check for updates** |

---

## 📦 Installation (Windows)

Download the latest release directly from the [Releases](https://github.com/ClaudyRg/Mochi/releases) page:

- **Recommended:** `Mochii_1.2.1_x64-setup.exe` (NSIS Windows Installer)
- **MSI Package:** `Mochii_1.2.1_x64_en-US.msi`

---

## 🛠️ Building from Source

### Prerequisites
*   **Windows 10 or Windows 11** (64-bit)
*   **Node.js 20+** and **npm**
*   **Rust** (stable MSVC toolchain)

### Setup & Development

```bash
git clone https://github.com/ClaudyRg/Mochi.git
cd Mochi
npm install
npm run dev:tauri
```

### Build Windows Installers

```bash
npm run build:tauri
```

Built installers are generated at:
*   `src-tauri/target/release/bundle/nsis/Mochii_1.2.0_x64-setup.exe`
*   `src-tauri/target/release/bundle/msi/Mochii_1.2.0_x64_en-US.msi`

---

## 👥 Founders & Core Developers

The team driving the engineering and aesthetics of Mochii:

<table align="center">
  <tr>
    <td align="center" width="50%">
      <a href="https://github.com/ClaudyRg">
        <img src="https://github.com/ClaudyRg.png" width="120px;" alt="Claudy" style="border-radius: 50%;"/><br />
        <b>Claudy</b>
      </a><br />
      👑 <b>Lead Developer & Architect</b><br />
      <i>Lead architect in charge of core desktop architecture, native Windows Rust/Win32/WinRT bridges, Tauri system integration, fluid UI layout, and real-time event pipelines.</i>
    </td>
    <td align="center" width="50%">
      <a href="https://github.com/Kwacyy">
        <img src="https://github.com/Kwacyy.png" width="120px;" alt="Yunna" style="border-radius: 50%;"/><br />
        <b>Yunna</b>
      </a><br />
      🌸 <b>Co-Developer & Interface Designer</b><br />
      <i>Creative designer and aesthetic mentor managing mascot personality, fluid animation choreography, sound design, color harmonies, and emotional UX nuances.</i>
    </td>
  </tr>
</table>

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer" width="100%" />
</div>
