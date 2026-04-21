# 🤖 FACE.ID — Real-Time Neural Face Recognition

> A cyberpunk-styled, browser-based face detection and analysis tool powered by **face-api.js** — no backend, no server, 100% client-side.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![face-api.js](https://img.shields.io/badge/face--api.js-0.22.2-00f0ff?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

---

## ✨ Features

- 🎯 **Real-time face detection** using SSD MobileNet v1
- 🗺️ **68-point facial landmark** mapping rendered live on the video feed
- 🧬 **Age & gender estimation** per detected face
- 😄 **Expression analysis** with 7 emotion categories and animated progress bars
- 📦 **Zero backend** — all AI models run locally in the browser via WebGL
- 🔒 **Privacy-first** — no data is sent to any server
- 📊 **Live system log**, FPS counter, and biometric data panel
- 🖥️ Responsive layout for desktop and mobile

---

## 📸 Preview

```
┌─────────────────────────────────────────────────────────┐
│  FACE.ID                          ● MODELS READY  FPS:5 │
├──────────────────────────────┬──────────────────────────┤
│                              │  BIOMETRIC DATA          │
│   [ WEBCAM FEED ]            │  FACES       1           │
│                              │  AGE (EST.)  27 yrs      │
│   ╔══════════════╗           │  GENDER      MALE        │
│   ║  #1 27y MALE ║           │  CONFIDENCE  94%         │
│   ║    94%       ║           │  EXPRESSION  HAPPY       │
│   ╚══════════════╝           ├──────────────────────────┤
│   · · · · · · · ·            │  EXPRESSION ANALYSIS     │
│                              │  HAPPY    ████████ 82%   │
│  [ START ]  [ STOP ]         │  NEUTRAL  ██ 10%         │
│                              │  SURPRISED █ 5%          │
└──────────────────────────────┴──────────────────────────┘
```

---

## 🚀 Getting Started

### Option 1 — Open directly (no install)

Just download `face-recognition.html` and open it in any modern browser:

```bash
# Clone the repo
git clone https://github.com/your-username/face-id.git

# Open in browser
open face-id/face-recognition.html
```

> ⚠️ Some browsers block webcam access for `file://` URLs. If the camera doesn't start, use Option 2.

### Option 2 — Serve locally

```bash
# Using Python
python3 -m http.server 8080

# Using Node.js
npx serve .

# Then open
http://localhost:8080/face-recognition.html
```

---

## 🧠 How It Works

FACE.ID loads four neural network models from a CDN at startup:

| Model | Purpose |
|---|---|
| `ssdMobilenetv1` | Detects face bounding boxes |
| `faceLandmark68Net` | Maps 68 facial keypoints |
| `ageGenderNet` | Estimates age and gender |
| `faceExpressionNet` | Classifies 7 emotional expressions |

Once models are ready, the webcam feed is captured and processed at ~5 FPS. Detections are drawn onto a `<canvas>` overlay mirrored to match the natural selfie orientation.

---

## 😮 Detected Expressions

| Expression | Description |
|---|---|
| 😊 Happy | Smiling, joy |
| 😐 Neutral | Resting face |
| 😢 Sad | Downward expression |
| 😠 Angry | Furrowed brows, tension |
| 😱 Surprised | Wide eyes, open mouth |
| 😨 Fearful | Raised brows, tension |
| 🤢 Disgusted | Wrinkled nose |

---

## 🛠️ Tech Stack

| Technology | Role |
|---|---|
| **Vanilla JS** | Core application logic |
| **face-api.js v0.22.2** | Face detection & analysis models |
| **HTML5 Canvas** | Overlay rendering |
| **MediaDevices API** | Webcam access |
| **Google Fonts** | `Share Tech Mono` + `Rajdhani` |
| **CSS Custom Properties** | Theming & design tokens |

---

## 🌐 Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 15+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile Chrome | ✅ Full |
| Mobile Safari | ⚠️ Requires HTTPS |

> **Note:** Camera access requires either `localhost` or an `https://` origin on most browsers.

---

## 🔒 Privacy

- All AI inference runs **entirely in your browser**
- **No video, images, or biometric data** is transmitted anywhere
- No analytics, no tracking, no cookies
- Models are loaded from a public CDN (jsDelivr) on first use

---

## 📁 Project Structure

```
face-id/
│
├── face-recognition.html   # Single-file application (HTML + CSS + JS)
└── README.md               # This file
```

---

## 🤝 Contributing

Contributions are welcome! Some ideas for improvements:

- [ ] Face recognition across multiple people (labeling)
- [ ] Screenshot / snapshot capture button
- [ ] Record video with overlay
- [ ] Dark/light theme toggle
- [ ] Adjustable detection confidence threshold
- [ ] Mobile camera switching (front/back)

1. Fork the repo
2. Create your branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add my feature'`
4. Push: `git push origin feature/my-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute.

---

## 🙏 Acknowledgements

- [face-api.js](https://github.com/justadudewhohacks/face-api.js) by Vincent Mühler
- [@vladmandic/face-api](https://github.com/vladmandic/face-api) — maintained fork used for model hosting
- Models based on [dlib](http://dlib.net/) and TensorFlow.js

---

<div align="center">
  Made with ☕ and vanilla JS &nbsp;·&nbsp; No frameworks were harmed
</div>
