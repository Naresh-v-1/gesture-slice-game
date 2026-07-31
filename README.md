<div align="center">

# 🍉 SLICE
### Gesture Vision Game

**Slice fruit with nothing but your hand — tracked live through your webcam.**

![vanilla js](https://img.shields.io/badge/stack-vanilla%20JS-f7df1e?style=flat-square)
![mediapipe](https://img.shields.io/badge/tracking-MediaPipe-4285f4?style=flat-square)
![privacy](https://img.shields.io/badge/video-never%20leaves%20your%20device-c6ff3d?style=flat-square)
![status](https://img.shields.io/badge/status-hackathon%20ready-00e5ff?style=flat-square)

**[▶ Play it live](https://naresh-v-1.github.io/gesture-slice-game/)**

</div>

---

## 🎯 What it does

Swipe your index finger through the air to slice fruit as it launches up the screen — dodge the bombs, chain combos for score multipliers, and grab the rare golden fruit for a big payout.

A live hand-tracking HUD overlays your skeleton and tracking status directly on the video feed, so anyone watching can see the computer vision working in real time — no black box, no controller, no keyboard.

> Everything runs **on-device**, in the browser. No frame of video is ever uploaded anywhere.

---

## ✨ Features

| | |
|---|---|
| 🖐️ **Real-time hand tracking** | 21-point hand landmark detection via MediaPipe, fully client-side (WASM + GPU delegate) |
| 👋 **Gesture-only controls** | Swipe to slice, hold an open palm still to pause/resume — no keyboard needed |
| 🔥 **Combo system** | Chain slices within a short window for up to a 5x score multiplier |
| ⭐ **Golden fruit** | Rare high-value fruit with its own glow and sound |
| 📈 **Adaptive difficulty** | Spawn rate ramps up as your score climbs, with a live level indicator |
| 💥 **Juice** | Screen shake + red flash on bombs, particle bursts on every slice, jitter-free cursor smoothing |
| ⏱️ **3-2-1 countdown** | Runs before the round starts, and every time you resume from pause |
| 📊 **Session stats** | Live FPS, per-hand tracking badges, and a game-over screen with accuracy + best combo |
| ✋✋ **Two-hand support** | Track and slice independently with both hands |

---

## 🎮 Controls

| Action | How |
|---|---|
| Slice fruit | Swipe your index finger across it |
| Pause / Resume | Hold an open palm still for ~0.6s, or press `P` |
| Restart | Press `Space`, click the frame, or hit **Play Again** |
| Mute / unmute | Speaker icon in the HUD |

---

## 🛠️ Tech stack

- **Vanilla HTML / CSS / JS** — zero build step, zero framework
- **MediaPipe Tasks Vision** (via CDN) — hand landmark detection
- **Web Audio API** — synthesized sound effects, no audio files
- **Canvas 2D** — all rendering

---

## 🚀 Running it locally

```bash
git clone https://github.com/Naresh-v-1/gesture-slice-game.git
cd gesture-slice-game
python3 -m http.server 8000
```
Then open `http://localhost:8000` — a local server (not `file://`) is needed for camera permission to work in most browsers.

---

## 🌐 Live deployment

Hosted on GitHub Pages, straight from the `main` branch:
👉 **https://naresh-v-1.github.io/gesture-slice-game/**

---

## 🔒 Privacy

All video processing happens locally in the browser. No frame, image, or hand-tracking data is ever sent to a server.

---

## 🗺️ Roadmap

- [ ] Two-player split-screen mode
- [ ] Persistent leaderboard (needs a backend/database — high score is currently session-only)
- [ ] Difficulty presets / custom game length
