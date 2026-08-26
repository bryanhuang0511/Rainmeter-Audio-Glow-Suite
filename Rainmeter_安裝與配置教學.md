# 🌟 Windows Rainmeter 音效流光與工作列小工具安裝指南

本目錄專注於 **Rainmeter 輕量常駐系統**，包含 **360° 全螢幕四周邊框動態環繞流光 (`MusicAudioGlow`)**、**工作列音樂律動小工具 (`Taskbar_Music_Widget`)** 與 **彩虹頻譜 (`Rainbow_Spectrum_Visualizer`)**。

---

## 🚀 快速開始 (一鍵安裝)

### 步驟 1：下載並安裝 Rainmeter
* 若你的電腦尚未安裝 Rainmeter，請前往官方網站下載最新版本：
  🔗 **[Rainmeter 官方網站下載點](https://www.rainmeter.net/)** (建議下載 Final Release 或 Beta 版)。

### 步驟 2：一鍵安裝 `Packages/` 下的 `.rmskin` 套件包
本目錄的 `Packages/` 資料夾內已為你收納精選的核心套件包：
1. **`MusicAudioGlow_Suite_v2.1.rmskin`**：最新版 360° 螢幕四周環繞音效流光（支援 5 大主題風格與重低音狂飆加速）。
2. **`Taskbar_Music_Widget_v2.0.rmskin`**：工作列音樂控制器與律動小工具 2.0 版。
3. **`Rainbow_Spectrum_Visualizer_v2.1.rmskin`**：彩虹頻譜 Bar 條視覺化。
4. **`WebNowPlaying-3.0.0-alpha.5.rmskin`**：瀏覽器與網頁播放器音樂抓取核心插件。

> **安裝方式**：直接雙擊任何 `.rmskin` 檔案 ➜ 在彈出的視窗點擊 **「Install」** 即可自動安裝生效！

---

## 🎨 5 大燈光風格自由切換 (`MusicAudioGlow`)

本套件內建 5 種數學雙色漸變與彩虹光譜主題，可隨心所欲自由切換：

| 數值 (`ColorStyle`) | 風格名稱 | 配色特點 | 推薦聆聽曲風 |
| :---: | :---: | :---: | :---: |
| **`1`** (預設) | **全彩光譜閉環 (Rainbow 360°)** | 360° 連續無縫彩虹色盤旋轉 | 流行、K-pop、搖滾 |
| **`2`** | **賽博龐克 (Cyberpunk)** | 霓虹粉紫 + 科技電光青 | 電子舞曲 (EDM)、Synthwave |
| **`3`** | **落日金光 (Sunset Gold)** | 熾熱金橙 + 魅惑洋紅 | 抒情、爵士、R&B |
| **`4`** | **極光綠境 (Aurora)** | 翡翠碧綠 + 冰川冰藍 | 輕音樂、環境氛圍音 (Lo-fi) |
| **`5`** | **熔岩烈焰 (Lava Crimson)** | 烈焰赤紅 + 狂暴金黃 | 重金屬、重低音 Trap/Dubstep |

### 🛠️ 風格切換步驟：
1. 在螢幕右下角系統匣對 Rainmeter 圖示點擊右鍵 ➜ 點選 **「Skins」** ➜ **「MusicAudioGlow」** ➜ **「MusicAudioGlow.ini」** ➜ **「Edit skin」**。
2. 找到檔案開頭的 `[Variables]` 區塊：
   ```ini
   [Variables]
   ScreenWidth=1707
   ScreenHeight=960
   BloomDepth=32

   ; 將數值改為 1 ~ 5 即可
   ColorStyle=2
   ```
3. 存檔後對桌面流光按右鍵點選 **「Refresh skin (重新整理)」**，立刻生效！

---

## ⚙️ 進階核心參數自訂

* **螢幕解析度調整 (`ScreenWidth` / `ScreenHeight`)**：
  預設適配 1080p / 2K 縮放比例，若流光邊界未貼齊螢幕邊緣，請修改為你當前的實際像素寬高（例如 `ScreenWidth=1920`, `ScreenHeight=1080`）。
* **音效靈敏度 (`AudioSensitivity`)**：
  預設值為 `42`。若平時聽歌音量較小，可調高至 `48~55`；若音量極大容易滿格，可下調至 `35~40`。
* **重低音加速響應 (`MeasureBeatEnergy`)**：
  本套件採用 `[MeasureBass] * 1.6 + [MeasureLowMid] * 0.7` 的非線性爆衝演算法，在大鼓與重低音落下時瞬間提供高達 8~10 倍的流光狂飆速度！

---

## 📜 授權協議

本項目基於 MIT License 開源，歡迎自由使用、修改與二次開發！
