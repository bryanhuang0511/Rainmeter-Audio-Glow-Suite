# Rainmeter Audio Glow Suite

[English](README.md) | [中文 (繁體)](README_zh.md)

適用於 Windows 10/11 的 Rainmeter 桌面動態音訊視覺化套件庫，整合 WASAPI Loopback 與 WebNowPlaying：包含 360 度螢幕邊框流光（`MusicAudioGlow`）、工作列音樂控制器（`BMediaTaskbarWidget`）與彩虹頻譜條（`monstercat-visualizer`）。

---

## 檔案清單與元件職責

| 模組名稱 | 功能說明 | 安裝封包 (`.rmskin`) | 原始碼目錄 |
|---|---|---|---|
| **MusicAudioGlow** | 360 度螢幕四周環繞流光，內建 5 種光譜風格與非線性重低音加速 | [`MusicAudioGlow_Suite_v2.1.rmskin`](Packages/MusicAudioGlow_Suite_v2.1.rmskin) | [`Skins/MusicAudioGlow/`](Skins/MusicAudioGlow/) |
| **BMediaTaskbarWidget** | 工作列常駐播放器，提供旋轉彩框、動態波紋與低音文字震動組合 | [`Taskbar_Music_Widget_v2.0.rmskin`](Packages/Taskbar_Music_Widget_v2.0.rmskin) | [`Skins/BMediaTaskbarWidget/`](Skins/BMediaTaskbarWidget/) |
| **monstercat-visualizer** | 基於 WASAPI FFT 分頻之經典彩虹漸變頻譜條 | [`Rainbow_Spectrum_Visualizer_v2.1.rmskin`](Packages/Rainbow_Spectrum_Visualizer_v2.1.rmskin) | [`Skins/monstercat-visualizer/`](Skins/monstercat-visualizer/) |
| **WebNowPlaying** | 瀏覽器播放資訊擷取插件（YouTube、Spotify Web、Apple Music Web） | [`WebNowPlaying-3.0.0-alpha.5.rmskin`](Packages/WebNowPlaying-3.0.0-alpha.5.rmskin) | — |
| [`Rainmeter_安裝與配置教學.md`](Rainmeter_安裝與配置教學.md) | 正體中文詳細安裝與配置手冊 | — | — |

---

## 模組參數與機制

### 1. MusicAudioGlow（`Skins/MusicAudioGlow/`）

包含主設定檔 `MusicAudioGlow.ini` 與 5 組獨立主題（`ColorStyle=1..5`：全彩光譜閉環、賽博龐克、落日金光、極光綠境、熔岩烈焰）。右鍵點選 **Edit skin** 可調整 `[Variables]`：

```ini
[Variables]
ScreenWidth=1920
ScreenHeight=1080
BloomDepth=32
ColorStyle=1
AudioSensitivity=42
```

### 2. BMediaTaskbarWidget（`Skins/BMediaTaskbarWidget/`）

提供 6 種 `.ini` 樣式組合，透過對稱波浪傳遞陣列（`W0..W14`）與三相 $120^\circ$ 正弦漸層色相（疊加 `[MeasureBass] * 0.05` 加速項）驅動邊框與波紋動態。

### 3. monstercat-visualizer（`Skins/monstercat-visualizer/`）

可於 `visualizer_rainbow.ini` 或 `@Resources\variables.ini` 調整 `BarCount`、`BarWidth`、`BarGap` 與 `Sensitivity`。

---

## 安裝與排解

### 一鍵安裝（`.rmskin`）

1. 先安裝 [Rainmeter](https://www.rainmeter.net/)（建議 `4.5+` 版本）。
2. 依序雙擊安裝 [`Packages/`](Packages/) 內的 [`WebNowPlaying-3.0.0-alpha.5.rmskin`](Packages/WebNowPlaying-3.0.0-alpha.5.rmskin) 與所需外觀套件，點選 **Install**。
3. 若使用 Chrome 或 Edge 播放網頁音樂，需另外安裝瀏覽器擴充功能 **WebNowPlaying Companion**。

### 手動部署原始碼

1. 將 [`Skins/`](Skins/) 底下的資料夾複製至 `%USERPROFILE%\Documents\Rainmeter\Skins\`。
2. 右鍵點擊右下角 Rainmeter 系統匣圖示並執行 **Refresh all**。

### 常見問題排解

* **流光或頻譜無反應**：確認 Windows 預設播放裝置與 Rainmeter 取樣裝置一致、確保音量可正常輸出，並執行 **Refresh skin**。
* **2K/4K 或多螢幕邊框未貼齊**：於 `MusicAudioGlow.ini` 的 `[Variables]` 將 `ScreenWidth` 與 `ScreenHeight` 改為實際顯示器像素後重新整理皮膚。

---

## 授權條款

本專案採用 [MIT License](LICENSE) 授權條款釋出。
