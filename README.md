# Rainmeter Audio Glow Suite

[English](README.md) | [中文 (繁體)](README_zh.md)

A collection of three Windows 10/11 Rainmeter desktop audio visualization suites powered by WASAPI loopback and WebNowPlaying: a 360-degree screen perimeter glow (`MusicAudioGlow`), a taskbar media bar widget (`BMediaTaskbarWidget`), and a rainbow spectrum bar visualizer (`monstercat-visualizer`).

---

## File List and Component Roles

| Module | Role | Package (`.rmskin`) | Source Directory |
|---|---|---|---|
| **MusicAudioGlow** | 360-degree screen perimeter glow with 5 color presets and nonlinear bass acceleration | [`MusicAudioGlow_Suite_v2.1.rmskin`](Packages/MusicAudioGlow_Suite_v2.1.rmskin) | [`Skins/MusicAudioGlow/`](Skins/MusicAudioGlow/) |
| **BMediaTaskbarWidget** | Taskbar media player with rotating color borders, wave bars, and text bounce | [`Taskbar_Music_Widget_v2.0.rmskin`](Packages/Taskbar_Music_Widget_v2.0.rmskin) | [`Skins/BMediaTaskbarWidget/`](Skins/BMediaTaskbarWidget/) |
| **monstercat-visualizer** | Rainbow spectrum frequency bar visualizer using WASAPI FFT bands | [`Rainbow_Spectrum_Visualizer_v2.1.rmskin`](Packages/Rainbow_Spectrum_Visualizer_v2.1.rmskin) | [`Skins/monstercat-visualizer/`](Skins/monstercat-visualizer/) |
| **WebNowPlaying** | Browser media companion plugin for YouTube, Spotify Web, and Apple Music Web | [`WebNowPlaying-3.0.0-alpha.5.rmskin`](Packages/WebNowPlaying-3.0.0-alpha.5.rmskin) | — |
| [`Rainmeter_安裝與配置教學.md`](Rainmeter_安裝與配置教學.md) | Extended Chinese configuration manual | — | — |

---

## Module Specifications

### 1. MusicAudioGlow (`Skins/MusicAudioGlow/`)

Includes `MusicAudioGlow.ini` and 5 standalone preset files (`ColorStyle=1..5`: Rainbow 360, Cyberpunk, Sunset Gold, Aurora Green, Lava Flame). Edit `[Variables]` via **Edit skin** to configure display dimensions and sensitivity:

```ini
[Variables]
ScreenWidth=1920
ScreenHeight=1080
BloomDepth=32
ColorStyle=1
AudioSensitivity=42
```

### 2. BMediaTaskbarWidget (`Skins/BMediaTaskbarWidget/`)

Provides 6 layout variants combining rainbow borders, symmetric wave propagation (`W0..W14`), and bass-modulated text bounce. Border color hue uses a 3-phase `120°` sine progression accelerated by `[MeasureBass] * 0.05`.

### 3. monstercat-visualizer (`Skins/monstercat-visualizer/`)

Configured via `visualizer_rainbow.ini` and `@Resources\variables.ini` (`BarCount`, `BarWidth`, `BarGap`, `Sensitivity`).

---

## Installation and Troubleshooting

### Quick Install (`.rmskin`)

1. Install [Rainmeter](https://www.rainmeter.net/) (`4.5+`).
2. Double-click [`WebNowPlaying-3.0.0-alpha.5.rmskin`](Packages/WebNowPlaying-3.0.0-alpha.5.rmskin) and the desired suite `.rmskin` files in [`Packages/`](Packages/), then select **Install**.
3. If reading media from Chrome or Edge, install the **WebNowPlaying Companion** browser extension.

### Manual Source Deployment

1. Copy the folders under [`Skins/`](Skins/) into `%USERPROFILE%\Documents\Rainmeter\Skins\`.
2. Right-click the Rainmeter tray icon and select **Refresh all**.

### Common Issues

* **No audio reaction**: Verify Windows default playback device matches the device sampled by Rainmeter, ensure system volume is audible, and click **Refresh skin**.
* **Screen perimeter misaligned on multi-monitor or 2K/4K displays**: Update `ScreenWidth` and `ScreenHeight` under `[Variables]` in `MusicAudioGlow.ini`, save, and refresh the skin.

---

## License

Released under the [MIT License](LICENSE).
