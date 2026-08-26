# 🎛️ Windows Rainmeter 音效視覺化與動態桌面套件庫

<div align="center">

![Rainmeter](https://img.shields.io/badge/Rainmeter-4.5%2B%20%7C%20144Hz-00b4d8?style=for-the-badge&logo=windows)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011-0078d4?style=for-the-badge&logo=windows)
![Audio Engine](https://img.shields.io/badge/Audio-WASAPI%20Direct%20Loopback-7209b7?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-f72585?style=for-the-badge)

**專為電競與極致聽覺打造的 3 大 Rainmeter 桌面動態音效視覺化模組**  
*Includes 360° Screen Perimeter Glow, Taskbar Wave Player Widget, and Dynamic Rainbow Spectrum Bar.*

[📦 一鍵安裝包下載](#-一鍵快速安裝包-packages) • [🛠️ 手動安裝源碼](#️-源碼手動安裝方法-skins) • [🎨 三大模組與代碼解析](#-三大核心模組介紹與參數設定) • [❓ 常見問題排解](#-常見問題排解-faq)

</div>

---

## 🌟 模組概覽 (Overview of the 3 Suites)

本專案收錄了三種不同形態的音效動態視覺化組件，無論是想要沉浸式全螢幕氛圍、簡約工作列音樂小工具，還是經典的頻譜跳動，都能自由組合搭配：

| 模組類別 | 模組名稱 | 特色亮點 | 對應 `.rmskin` 安裝包 | 原始碼目錄 |
| :--- | :--- | :--- | :--- | :--- |
| 🌊 **繞螢幕四周** | **MusicAudioGlow** | 360° 螢幕邊界動態跑馬流光、內建 5 種光譜風格、非線性低音爆衝加速、144Hz 極限流暢 | [`MusicAudioGlow_Suite_v2.1.rmskin`](Packages/MusicAudioGlow_Suite_v2.1.rmskin) | [`Skins/MusicAudioGlow/`](Skins/MusicAudioGlow/) |
| 🎛️ **工作列播放器** | **BMediaTaskbarWidget** | 工作列常駐音樂控制器、彩虹即時波紋、色帶旋轉邊框、歌曲跑馬燈、文字震動效果 | [`Taskbar_Music_Widget_v2.0.rmskin`](Packages/Taskbar_Music_Widget_v2.0.rmskin) | [`Skins/BMediaTaskbarWidget/`](Skins/BMediaTaskbarWidget/) |
| 📊 **動態頻譜條** | **Monstercat Rainbow Visualizer** | 經典條狀音頻頻譜 (Spectrum Bar)、彩虹漸變色隨時間流動、WASAPI 高精度 FFT 分頻 | [`Rainbow_Spectrum_Visualizer_v2.1.rmskin`](Packages/Rainbow_Spectrum_Visualizer_v2.1.rmskin) | [`Skins/monstercat-visualizer/`](Skins/monstercat-visualizer/) |

---

## 📦 一鍵快速安裝包 (Packages)

若你只想立刻在桌面上使用，推薦直接使用 `Packages/` 目錄下的 `.rmskin` 套件包：

### 步驟 1：安裝 Rainmeter 主程式
請先確認電腦已安裝 Rainmeter 桌面自訂軟體：
* 🔗 **[Rainmeter 官方網站下載](https://www.rainmeter.net/)** (建議下載 4.5.x 以上版本，免費且開源)。

### 步驟 2：下載並依序安裝 `.rmskin`
請前往 [**`Packages/`**](Packages/) 資料夾，雙擊安裝你所需的套件：

1. **必備通訊插件**：[`WebNowPlaying-3.0.0-alpha.5.rmskin`](Packages/WebNowPlaying-3.0.0-alpha.5.rmskin)
   * 用於抓取 Chrome/Edge 瀏覽器 (YouTube、Spotify Web、Apple Music Web 等) 當前播放的歌曲名稱、作者與專輯封面。
   * *註：瀏覽器端需搭配安裝擴充插件「WebNowPlaying-Companion」。*
2. **360° 螢幕邊框流光**：[`MusicAudioGlow_Suite_v2.1.rmskin`](Packages/MusicAudioGlow_Suite_v2.1.rmskin)
   * 雙擊 ➜ 點選 **「Install」** ➜ 桌面邊緣立即出現環繞流光。
3. **工作列音樂小工具**：[`Taskbar_Music_Widget_v2.0.rmskin`](Packages/Taskbar_Music_Widget_v2.0.rmskin)
   * 雙擊 ➜ 點選 **「Install」** ➜ 拖曳至 Windows 工作列適當位置即可。
4. **彩虹頻譜跳動條**：[`Rainbow_Spectrum_Visualizer_v2.1.rmskin`](Packages/Rainbow_Spectrum_Visualizer_v2.1.rmskin)
   * 雙擊 ➜ 點選 **「Install」** ➜ 即刻啟動桌面彩虹頻譜。

> 💡 **安裝提示**：Rainmeter Skin Installer 彈出視窗時，勾選 **「Apply included layout」** 或 **「Load skin」** 後點擊 **Install**，Rainmeter 即會自動解壓縮並載入。

---

## 🛠️ 源碼手動安裝方法 (Skins)

如果你想直接查看源代碼、修改 `.ini` 腳本，或是手動部署到 Rainmeter：

1. **定位 Rainmeter Skins 目錄**：
   在 Windows 檔案總管進入：
   ```text
   %USERPROFILE%\Documents\Rainmeter\Skins\
   ```
   *(通常路徑為 `C:\Users\你的使用者名稱\Documents\Rainmeter\Skins\`)*

2. **複製 Skins 資料夾**：
   將本專案 [`Skins/`](Skins/) 目錄下的子資料夾整包複製到上述的 Rainmeter Skins 資料夾中：
   * 複製 `Skins/MusicAudioGlow` ➜ `...\Rainmeter\Skins\MusicAudioGlow`
   * 複製 `Skins/BMediaTaskbarWidget` ➜ `...\Rainmeter\Skins\BMediaTaskbarWidget`
   * 複製 `Skins/monstercat-visualizer` ➜ `...\Rainmeter\Skins\monstercat-visualizer`

3. **重新整理 Rainmeter**：
   * 在螢幕右下角系統匣對 Rainmeter 綠色水滴圖示按右鍵 ➜ 點選 **「Refresh all (重新整理全部)」**。
   * 在清單中即可展開並加載對應的 `.ini` 檔案。

---

## 🎨 三大核心模組介紹與參數設定

---

### 1. 🌊 360° 螢幕四周邊框動態環繞流光 (`MusicAudioGlow`)

#### 📌 特色說明
採用非線性重低音物理加速曲線，將 360° 邊框無縫閉環，並結合外側純色邊條與內側柔和 Bloom 光暈。

```text
Skins/MusicAudioGlow/
├── MusicAudioGlow.ini       # 主配置文件 (可自由設定 1~5 號風格)
├── 1_全彩光譜閉環.ini        # 風格 1 獨立版 (Rainbow 360°)
├── 2_賽博龐克.ini           # 風格 2 獨立版 (Cyberpunk Neon)
├── 3_落日金光.ini           # 風格 3 獨立版 (Sunset Gold)
├── 4_極光綠境.ini           # 風格 4 獨立版 (Aurora Green)
├── 5_熔岩烈焰.ini           # 風格 5 獨立版 (Lava Flame)
└── @Resources/              # 邊緣柔和 Bloom 漸層遮罩 PNG 圖檔
```

#### 🎨 5 大光譜配色主題一覽

| 編號 (`ColorStyle`) | 風格名稱 | 配色基調 | 推薦情境 |
| :---: | :---: | :---: | :---: |
| **`1`** (預設) | **全彩光譜閉環 (Rainbow 360°)** | 360° 連續無縫彩虹色環動態旋轉 | 流行、K-pop、全曲風通用 |
| **`2`** | **賽博龐克 (Cyberpunk)** | 霓虹粉紫 `(255,20,147)` + 科技電光青 `(0,245,255)` | 電子舞曲 (EDM)、Synthwave |
| **`3`** | **落日金光 (Sunset Gold)** | 熾熱金橙 `(255,140,0)` + 魅惑洋紅 `(255,20,100)` | 爵士、R&B、抒情流行 |
| **`4`** | **極光綠境 (Aurora)** | 翡翠碧綠 `(0,255,128)` + 冰川天藍 `(0,200,255)` | 環境氛圍音樂 (Lo-fi)、輕音樂 |
| **`5`** | **熔岩烈焰 (Lava Crimson)** | 烈焰赤紅 `(255,30,0)` + 狂暴金黃 `(255,200,0)` | 重金屬搖滾、重低音 Trap/Dubstep |

#### ⚙️ 核心代碼與參數調整 (`MusicAudioGlow.ini`)
右鍵點擊流光 ➜ **「Edit skin」** 開啟編輯開頭的 `[Variables]` 區塊：

```ini
[Variables]
; 螢幕解析度設定 (請依顯示器實際像素填寫，例：1920x1080、2560x1440)
ScreenWidth=1920
ScreenHeight=1080

; 光暈深度 (像素，預設 32~40)
BloomDepth=32

; 主題風格切換：填入 1 到 5
ColorStyle=1

; 音訊靈敏度 (預設 42；小聲可調至 48~55，大聲可降至 35~40)
AudioSensitivity=42
```

---

### 2. 🎛️ 工作列音樂小工具 (`BMediaTaskbarWidget`)

#### 📌 特色說明
專為 Windows 工作列空間設計的輕量音樂面板，提供 6 種視覺排列組合：

```text
Skins/BMediaTaskbarWidget/
├── 彩色邊框_彩色波紋_原色.ini   # ★ 最推薦：彩虹旋轉邊框 + 律動波浪 + 深色文字
├── 彩色邊框_彩色波紋_淺底.ini   # 白霧玻璃底色 + 彩虹旋轉邊框 + 律動波浪
├── 彩色邊框_文字震動.ini        # 彩虹旋轉邊框 + 低音帶動歌名文字上下微震
├── 彩色邊框.ini                # 極簡純彩虹旋轉邊框
├── 彩色波紋_文字震動.ini        # 純彩色波紋 + 歌名文字震動
└── 彩色波紋.ini                # 經典底層彩色動態液體波浪
```

#### ⚙️ 核心技術機制
1. **動態波浪傳遞陣列 (`W0` ~ `W14`)**：
   透過 `[MeasurePropagate]` 逐幀將中央低音能量向左右兩側傳遞，形成如水波紋般的對稱漣漪。
2. **三相旋轉漸層色相法 (`MeasureColorShift`)**：
   邊框色彩採用三相 $120^\circ$ 錯開正弦曲線：
   $$\text{R} = \sin(\theta) \times 127 + 128$$
   $$\text{G} = \sin(\theta + 120^\circ) \times 127 + 128$$
   $$\text{B} = \sin(\theta + 240^\circ) \times 127 + 128$$
   並疊加低音加速項 `[MeasureBass] * 0.05`，達到歌曲重拍時色彩光環旋轉加速！

---

### 3. 📊 彩虹跳動頻譜條 (`monstercat-visualizer`)

#### 📌 特色說明
基於經典 Monstercat 頻譜演算法，結合 WASAPI 音訊分頻與彩虹漸變流光，隨音樂即時跳動。

```text
Skins/monstercat-visualizer/
├── visualizer_rainbow.ini   # 彩虹頻譜主程序
├── Settings/                # 設定面板
└── @Resources/              # 包含 Factory.lua 等動態生成 Bar 條腳本
```

#### ⚙️ 核心設定調整
在 `visualizer_rainbow.ini` 或 `@Resources\variables.ini` 中：
* `BarCount`: 頻譜 Bar 條數量（預設 40~60 條）。
* `BarWidth`: 單根 Bar 條寬度。
* `BarGap`: Bar 條之間的間隔距離。
* `Sensitivity`: 頻譜音訊靈敏度。

---

## ❓ 常見問題排解 (FAQ)

### Q1：安裝後邊框流光或頻譜完全沒有反應？
1. **檢查預設音訊輸出裝置**：
   * 確保 Windows 右下角播放裝置與 Rainmeter 取樣的聲卡一致。
   * 對皮膚按右鍵點擊 **「Refresh skin」**。
2. **音量太小**：
   * 開啟 Spotify / YouTube 並確認系統總音量在 30% 以上。

### Q2：工作列播放器無法顯示歌曲名稱或專輯封面？
1. 請確認已安裝 [`WebNowPlaying-3.0.0-alpha.5.rmskin`](Packages/WebNowPlaying-3.0.0-alpha.5.rmskin)。
2. 若使用 Chrome / Edge 瀏覽器聽歌，請至 Chrome 線上應用程式商店搜尋並安裝 **「WebNowPlaying Companion」** 擴充功能，並開啟權限。

### Q3：雙螢幕或 2K/4K 螢幕流光沒有貼齊邊緣？
* 請在 `MusicAudioGlow.ini` 找到 `[Variables]`，將 `ScreenWidth` 與 `ScreenHeight` 修改為該螢幕的實際解析度（例如 2K 螢幕填入 `ScreenWidth=2560`、`ScreenHeight=1440`），存檔後對流光按右鍵 **「Refresh skin」** 即可精準貼邊。

---

## 📜 專案結構一覽 (File Structure)

```text
├── README.md                      # 📖 本說明文件 (GitHub 導覽主手冊)
├── Rainmeter_安裝與配置教學.md      # ⚙️ 繁體中文詳細配置手冊
├── Packages/                      # 📦 官方一鍵安裝套件包 (.rmskin)
│   ├── MusicAudioGlow_Suite_v2.1.rmskin          # 360° 螢幕四周環繞流光
│   ├── Taskbar_Music_Widget_v2.0.rmskin          # 工作列音樂律動小工具
│   ├── Rainbow_Spectrum_Visualizer_v2.1.rmskin  # 彩虹跳動頻譜 Bar 條
│   └── WebNowPlaying-3.0.0-alpha.5.rmskin        # 瀏覽器音樂感知插件
└── Skins/                         # 🛠️ 原始碼目錄 (可直接放進 Rainmeter\Skins)
    ├── MusicAudioGlow/            # 360° 邊框流光源碼與 5 大風格
    ├── BMediaTaskbarWidget/       # 工作列播放器多種樣式源碼
    ├── monstercat-visualizer/     # 頻譜視覺化源碼與 Lua 腳本
    └── @Vault/                    # 共用插件庫 (Plugins)
```

---

## 📄 開源協議

本專案所有 Rainmeter 組件均基於 **[MIT License](LICENSE)** 開源分享。歡迎自由修改、分享或打造屬於你自己的專屬桌面風格！🌟
