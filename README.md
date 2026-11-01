# 🏓 Multiball Mayhem: Infinite Pong

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Web Audio API](https://img.shields.io/badge/Web_Audio_API-Synthesized-005571?style=for-the-badge)](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

A fast-paced, cyberpunk-themed arcade Pong game built as a zero-dependency, single-file browser application. Featuring continuous ball spawns, an adaptive autonomous CPU AI, touch and mouse support, procedurally synthesized retro audio, and **16 stackable chaos modifiers** that unlock every 30 points.

---

## 📑 Table of Contents

- [Features](#-features)
- [Game Modes](#-game-modes)
- [How to Play](#-how-to-play)
- [Chaos Modifiers](#-chaos-modifiers)
- [Chaos Combo Lab (Sandbox)](#-chaos-combo-lab-sandbox)
- [Developer & Cheat Console](#-developer--cheat-console)
- [Controls](#-controls)
- [Technical Architecture](#-technical-architecture)
- [Getting Started](#-getting-started)
- [Deploying to GitHub Pages](#-deploying-to-github-pages)
- [Author & License](#-author--license)

---

## ⚡ Features

- **Continuous Multi-Ball Spawns**: Every 1.0 second (0.5s in Turbo mode), a new ball launches from the center spawner into play.
- **Predictive Trajectory Reticles**: Dynamic dotted laser guides and directional arrowheads indicate incoming ball trajectories before launch.
- **Milestone Chaos Trigger**: Every time either player reaches a multiple of 30 points (30, 60, 90, ...), a new randomized game modifier is triggered with screen shake and alert banners.
- **16 Stackable Modifiers**: Modifiers combine dynamically, multiplying the mayhem (e.g., *Penta Shot* + *Spiral* + *Double Spawner*).
- **Procedural Audio Engine**: 100% self-contained sound effects generated on-the-fly using the browser's Web Audio API oscillators—no external sound files required.
- **Retro-Cyberpunk Aesthetic**: CRT scanline overlay, neon bloom glow, dynamic particle spark bursts, and high-contrast HUD styling powered by Google Orbitron and Tailwind CSS.
- **Full Cross-Platform Input**: Complete support for keyboard, mouse tracking, and mobile touch controls.

---

## 🕹️ Game Modes

| Mode | Description |
| :--- | :--- |
| **🤖 1P vs CPU** | Battle an autonomous AI that tracks and calculates ball trajectories in real-time across dozens of active balls. |
| **👥 2P Local** | Head-to-head couch multiplayer on a shared keyboard or split touchscreen. |
| **🧪 Chaos Combo Lab** | A sandbox test environment with unlimited play (no 50-point cap), manual ball volley triggers, modifier matrix controls, and pre-built chaos combinations. |

---

## 🎯 How to Play

1. **Objective**: First player to score **50 points** wins the match (customizable via the Developer Console).
2. **Scoring**: Deflect balls past your opponent’s baseline to score. Each ball that slips through awards 1 point.
3. **Escalation**: As the match progresses, the screen fills with active balls. Every 30 points scored unlocks an additional stacking modifier.
4. **Trajectory Aiming**: Watch the center aiming reticle—it projects where the next ball volley will emerge, giving you a split-second to reposition your paddle.

---

## 💥 Chaos Modifiers

Multiball Mayhem features 16 distinct modifiers that stack on top of each other:

| # | Modifier | Duration / Limit | Mechanics & Effects |
| :-: | :--- | :--- | :--- |
| **1** | **🔥 Penta Shot (Frenzy)** | Permanent / Stackable | Spawns a fan of 5 simultaneous balls instead of a single volley. |
| **2** | **⚡ Double Speed (Turbo)** | Permanent / Stackable | Cuts the spawner countdown timer in half (from 1.0s down to 0.5s). |
| **3** | **〰️ Sine Wave** | Permanent / Stackable | Balls oscillate vertically in high-frequency sinusoidal sine-wave trajectories. |
| **4** | **📏 Micro Paddles** | 30 Seconds | Shrinks paddle heights by 50%, requiring pin-point precision. |
| **5** | **💥 Rapid Spray 20** | 20 Balls | Discharges a machine-gun burst of 20 randomized high-velocity balls. |
| **6** | **🧪 Glue Slime** | 30 Seconds | Drips sticky slime onto the court, reducing paddle movement speeds by 55%. |
| **7** | **👿 Evil Spray** | 20 Balls | Rapid-fires 20 direct-targeted projectiles specifically toward one player's goal. |
| **8** | **🌀 Charge Blast** | Accumulator | Charges energy each spawn. At 10 charges, releases a 10-ball 360° supernova burst. |
| **9** | **✂️ Ball Splitter** | 10 Deflections | The next 10 paddle collisions cause the deflecting ball to split into a duplicate child ball. |
| **10** | **🎯 Homing Lock-On** | 30 Seconds | Incoming balls smoothly curve and steer toward the target player's paddle. |
| **11** | **👥 Me, Myself & I** | 30 Seconds | Spawns two mirror mini-paddles above and below the player's primary paddle. |
| **12** | **🗼 Sentry Turret** | 30 Seconds | Places an automated laser sentry on court that actively fires at the opponent. Turret bullets vanish upon paddle impact. |
| **13** | **✨ Dupe Spawner** | Permanent / Stackable | Activates an auxiliary second court spawner and duplicates existing sentries. |
| **14** | **🌀 Spiral Shot** | 30 Balls | Emits 30 projectiles in a continuous 360-degree rotating pinwheel pattern. |
| **15** | **🌊 Wiggle** | 60 Seconds | Modulates the velocity of all active balls continuously between 50% and 150% speed. |
| **16** | **💻 Binary (0101)** | Permanent / Stackable | Quantum digital mode: paddles expand to 50% screen height and snap exclusively to top (`0`) or bottom (`1`). |

---

## 🧪 Chaos Combo Lab (Sandbox)

Click **🧪 Lab Mode** or enter via the start overlay to launch the Sandbox:

- **Infinite Play**: Winning score conditions are suspended, allowing for prolonged sessions with 50+ active balls.
- **Interactive Stack Matrix**: Individually toggle any of the 16 modifiers ON or OFF in real time.
- **Quick Preset Combos**:
  - 🔥 **Bullet Hell**: *Penta Shot* + *Turbo* (10 balls/second volley rate).
  - 〰️ **Snakers**: *Sine Wave* + *Micro Paddles* + *Splitter*.
  - 🎯 **Sticky Hunter**: *Homing* + *Glue* + *Evil Spray*.
  - ☠️ **Total Chaos**: Activates all 16 modifiers simultaneously.
- **Utility Actions**: Trigger `+10 Ball Volley`, wipe active balls, or reset the modifier matrix.

---

## 🛠️ Developer & Cheat Console

Multiball Mayhem includes an in-game developer tweak tool.

1. Click the **⚡ [CHEAT CODE]** button located at the bottom-right of the control bar.
2. Enter the passcode:
   ```text
   code123456
   ```
3. Once authenticated, the tweak console allows you to adjust live physics values:
   - **Paddle Speed**: `200` to `1800 px/s` (default: 550 px/s)
   - **Paddle Height**: `20` to `180 px` (default: 78 px)
   - **Ball Base Speed**: `150` to `1000 px/s` (default: 320 px/s)
   - **Spawn Interval**: `0.1` to `3.0 seconds` (default: 1.0s)
   - **Target Winning Score**: `5` to `200 points` (default: 50 pts)
   - **Direct Modifier Overrides**: Instant activation and clearance of any modifier.

---

## 🎮 Controls

### Player Controls

| Player | Keyboard | Mouse / Pointer | Touchscreen |
| :--- | :--- | :--- | :--- |
| **Player 1 (Cyan)** | `W` (Up) / `S` (Down) | Move mouse vertically inside canvas | Drag on left half of screen |
| **Player 2 (Pink)** | `↑` (Up) / `↓` (Down) | N/A (Keyboard / Touch only) | Drag on right half of screen |
| **Binary Mode** | `W` / `↑` (Top: `0`)<br>`S` / `↓` (Bottom: `1`) | Top Half (`0`) / Bottom Half (`1`) | Upper Half (`0`) / Lower Half (`1`) |

### Game Controls

- **Start / Pause / Resume**: `Spacebar` or click the **Pause** button.
- **Restart Match**: Click **Restart**.
- **Exit Round**: Click **✕ Exit Round** or the **✕** icon on the top-right of the arena.
- **Toggle Audio**: Click **🔊 Sound On** / **🔇 Muted**.

---

## 🏗️ Technical Architecture

- **Single-File Architecture**: The complete game—markup, responsive Tailwind CSS styling, game loop logic, and Web Audio synthesizer—is contained within `index.html`.
- **Game Loop**: Driven by `window.requestAnimationFrame` with delta-time (`dt`) calculation, ensuring consistent ball physics and animation speeds across high-refresh displays (60Hz, 120Hz, 144Hz+).
- **Procedural Audio Engine**: Uses native `AudioContext` with parameterized `OscillatorNode` types (`sine`, `square`, `triangle`, `sawtooth`) and `GainNode` volume envelopes for zero-latency, asset-free sound effects.
- **Render Pipeline**: HTML5 2D Canvas rendering utilizing rounded geometry (`roundRect`), ball motion trails with exponential alpha falloff, particle sparks, and CSS CRT scanline styling.

---

## 🚀 Getting Started

### Option 1: Direct File Launch (No Server Required)
Simply double-click `index.html` or drag it into any modern web browser (Google Chrome, Mozilla Firefox, Apple Safari, Microsoft Edge).

### Option 2: Local Static Server

Using Python:
```bash
python3 -m http.server 8000
```
Then navigate to `http://localhost:8000` in your browser.

Using Node.js (`npx serve`):
```bash
npx serve .
```

---

## 🌐 Deploying to GitHub Pages

1. Push your repository to GitHub.
2. In your repository on GitHub, navigate to **Settings** > **Pages**.
3. Under **Build and deployment** > **Source**, select **Deploy from a branch**.
4. Set the branch to `main` (or `master`) and folder to `/ (root)`.
5. Click **Save**. Your game will be live at `https://<username>.github.io/<repo-name>/`.

---

## 👤 Author & License

- **Author**: [Xreston Leung](https://github.com/xreston)
- **License**: Released under the [MIT License](LICENSE).
