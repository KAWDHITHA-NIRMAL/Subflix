<p align="center">
  <img src="src/image/logo.png" alt="SubFlix Logo" height="60">
</p>

# SubFlix — Advanced Subtitle Browser Extension

SubFlix is a premium, lightweight browser extension for Google Chrome, Microsoft Edge, and Chromium-based browsers. It allows users to load, overlay, style, and synchronize external subtitle files directly over any HTML5 video player inside the browser. SubFlix is processed completely locally, ensuring absolute privacy.

---

## ✨ Features

- **Multi-Browser Support**: Architected for Chrome Web Store and Microsoft Edge Add-ons using Manifest V3.
- **Robust Subtitle Parser**: Handles `.srt` and `.vtt` formats with support for multiple formats to be added easily.
- **Unicode & Language Support**: Fully compatible with Unicode character sets including Sinhala, Tamil, Arabic, Hindi, Chinese, Japanese, Korean, and European languages. Handles RTL layouts gracefully.
- **Drag & Drop Interface**: Drag a subtitle file directly onto the browser extension popup, or drop it anywhere on the webpage containing a video player to load it instantly.
- **Smart Video Detector**: Automatically scans and detects HTML5 video players on the page, with seamless support for dynamically loaded players on Single Page Applications (SPAs).
- **Responsive Custom Overlay**: Renders custom subtitle nodes absolute-positioned over video screens, automatically scaling size and offsets relative to the video frame's width and height.
- **Live Sync & Delay Calibration**: Offset subtitle latency with fine adjustments (-10s to +10s in 0.1s steps, or custom delays) and quick-sync action buttons.
- **Advanced Appearance Styling**: Modify font families (including scripts like Noto Sans Sinhala/Tamil/Arabic), sizes, weights, colors, background box opacity, text outline thickness, and soft drop shadows.
- **Fullscreen Synchronization**: Intercepts native fullscreen actions to ensure custom subtitle nodes overlay correctly when full-screening videos.
- **Persistent Preferences**: Saves styling adjustments, alignment defaults, and behavioral options automatically across tabs using `chrome.storage.local`.
- **Keyboard Shortcuts**: Control video playback synchronization, styling scale factors, and visibility directly using hotkeys.
- **Zero Privacy Friction**: Processes all files locally on your computer. SubFlix does not upload subtitles, scrape browsing histories, or require registration.

---

## 🌐 Supported Browsers & Installation

Get SubFlix directly for your preferred browser:

| Browser | Supported Version | Download & Install Links |
| :---: | :--- | :--- |
| <img src="https://cdn.jsdelivr.net/npm/@browser-logos/edge/edge.png" width="28" height="28" valign="middle" alt="Microsoft Edge"> **Microsoft Edge** | v88+ | [![Get on Edge Store](https://img.shields.io/badge/Microsoft%20Edge-Get%20it%20on%20Edge-0078D7?style=for-the-badge&logo=microsoft-edge&logoColor=white)](https://microsoftedge.microsoft.com/addons/detail/subflix/ljkaiecamafkhpbajhhkgmdbebmmahlp) |
| <img src="https://cdn.jsdelivr.net/npm/@browser-logos/chrome/chrome.png" width="28" height="28" valign="middle" alt="Google Chrome"> **Google Chrome** | v88+ | [![Download ZIP](https://img.shields.io/badge/Google%20Chrome-Download%20ZIP-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://github.com/KAWDHITHA-NIRMAL/Subflix/releases/tag/subFlix) |
| <img src="https://cdn.jsdelivr.net/npm/@browser-logos/brave/brave.png" width="20" height="20" alt="Brave">&nbsp;&nbsp;<img src="https://cdn.jsdelivr.net/npm/@browser-logos/opera/opera.png" width="20" height="20" alt="Opera">&nbsp;&nbsp;<img src="https://cdn.jsdelivr.net/npm/@browser-logos/vivaldi/vivaldi.png" width="20" height="20" alt="Vivaldi"> **Brave / Opera / Vivaldi** | Chromium-based | Manual installation using the Chrome offline ZIP package |

---

## 🛠️ Manual Installation Guide (Developer Mode)

To load the unpacked extension manually in your browser (for Google Chrome, Brave, Opera, Vivaldi, or manual testing on Edge):

1. **Download the Offline Package**: Click the **Download ZIP** button in the table above for Google Chrome (or clone/download this repository).
2. Extract the downloaded `SubFlix.zip` file into a local folder on your computer.
3. Open your browser and navigate to the Extensions management page:
   - **Chrome**: `chrome://extensions/`
   - **Edge**: `edge://extensions/`
   - **Brave**: `brave://extensions/`
   - **Opera**: `opera://extensions/`
4. Enable **Developer mode** using the toggle switch (typically in the top-right corner or left menu).
5. Click the **Load unpacked** button.
6. Select the folder where you extracted the ZIP package (make sure it's the folder containing `manifest.json`).
7. The SubFlix icon should now be loaded and visible in your browser's extension bar!

---

## 🎬 How to Use

1. Open any website containing an HTML5 video (e.g., YouTube, Vimeo, or a local file player).
2. Play the video.
3. Open the **SubFlix** popup from your extensions toolbar.
4. Drag and drop your `.srt` or `.vtt` file directly into the popup box, or drop it onto the video player region of the webpage.
5. The subtitle overlay will mount instantly.
6. Use the popup slider or quick-adjustment buttons to offset latency if the subtitle timing does not align with the audio.

---

## ⚙️ Advanced Controls & Shortcuts

SubFlix maps the following interactive hotkeys directly inside active video tabs (ensuring typing inputs in text fields are ignored):

| Action | Keyboard Shortcut | Description |
| :--- | :--- | :--- |
| **Toggle Visibility** | `Ctrl + Shift + S` | Show or hide the active subtitle overlay. |
| **Delay Timing** | `Ctrl + Shift + Left Arrow` | Decreases timing offset by -0.5s. |
| **Advance Timing** | `Ctrl + Shift + Right Arrow` | Increases timing offset by +0.5s. |
| **Shift Up** | `Ctrl + Shift + Up Arrow` | Lifts vertical margin up by 2% from bottom. |
| **Shift Down** | `Ctrl + Shift + Down Arrow` | Lowers vertical margin down by 2% to bottom. |
| **Increase Size** | `Ctrl + Shift + +` | Enlarges text scaling size by 5%. |
| **Decrease Size** | `Ctrl + Shift + -` | Shrinks text scaling size by 5%. |

---

## 📂 Project Structure

```
SubFlix/
├── manifest.json
├── package.json
├── README.md
├── src/
│   ├── image/
│   │   ├── icon.png
│   │   └── logo.png
│   ├── popup/
│   │   ├── index.html
│   │   ├── popup.css
│   │   └── popup.js
│   ├── content/
│   │   ├── content.js
│   │   ├── subtitle-engine.js
│   │   ├── subtitle-parser.js
│   │   ├── video-detector.js
│   │   └── overlay.css
│   ├── background/
│   │   └── service-worker.js
│   ├── options/
│   │   ├── options.html
│   │   ├── options.css
│   │   └── options.js
│   └── utils/
│       ├── storage.js
│       ├── messaging.js
│       └── helpers.js
└── test/
    ├── test-player.html
    ├── sample-english.vtt
    └── sample-sinhala.srt
```

---

## 🔐 Privacy Policy

- **100% Local Processing**: All subtitle files are read and processed directly in memory inside your browser. No files or text contents are ever uploaded to external servers.
- **No Analytics/Telemetry**: SubFlix does not track your viewing habits, visit histories, or IP addresses.
- **Minimal Permissions**: The extension only requests access to `"storage"` (to persist custom appearance rules), `"activeTab"` (to safely query pages for video players), and `"contextMenus"`.

---

## 👨‍💻 Developer

Developed with ❤️ by **Kawdhitha Nirmal**.

<p align="left">
  <a href="https://t.me/codex_developer" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram" />
  </a>
  &nbsp;&nbsp;
  <a href="https://facebook.com/kawdhitha" target="_blank">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook" />
  </a>
</p>

---

## 📄 License & Credits

Special thanks to Google DeepMind and the open-source Chromium project.

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

<br/>

<p align="center">
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-4CAF50?style=for-the-badge" alt="MIT License" />
  </a>
</p>
