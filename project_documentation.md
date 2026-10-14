<!-- STREAMING_CHUNK:Creating project header and status badges... -->
# 🏰 Wizard's Chess 3D — Minimalist Gothic Cathedral

![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=for-the-badge&logo=three.js)
![Chess.js](https://img.shields.io/badge/Chess.js-v0.10.3-amber?style=for-the-badge)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.x-38B2AC?style=for-the-badge&logo=tailwind-css)
![Tone.js](https://img.shields.io/badge/Tone.js-Web_Audio-ff9d3b?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-emerald?style=for-the-badge)

A playable 3D **Wizard's Chess** web application set inside an atmospheric, minimalist **Gothic Cathedral**. Built with **Three.js**, **Chess.js**, **Tone.js**, and a **Material Design 3** single-level frosted-glass HUD, the game pits sculpted **White Carrara Marble** against **Black Volcanic Obsidian** with procedural animations and real-time 3D shattering physics.

---

<!-- STREAMING_CHUNK:Documenting core gameplay and visual features... -->
## ✨ Key Features

- **Minimalist 3D Gothic Cathedral Environment**
  - Clustered nave columns, pointed Gothic transverse arches with golden boss keystones, and a stepped altar plinth.
  - Illuminated North Apse featuring a 12-petal stained-glass **Rose Window**, tall lancet windows, and volumetric god-ray light shafts.
  - Dynamic flickering corner torch braziers and floating cathedral dust embers.
- **Sculpted 3D Marble vs. Obsidian Pieces**
  - All 32 pieces are procedurally modeled in 3D with custom canvas-generated marble and obsidian veined textures and gold accents.
- **Custom Procedural Animations & 3D Shatter Physics**
  - **Idle**: Subtle breathing scale, mystical crown rotation, and levitation when selected.
  - **Move**: Smooth stone-gliding interpolation with momentum tilt and high parabolic leaps for Knights.
  - **Attack & Shatter**: Capturing pieces perform a wind-up and dramatic lunge strike onto the target, shattering the victim into 24 3D polyhedral fragments that bounce, tumble, and skitter across the 64-square board under gravity and friction.
- **Complete Chess Rules & Modes**
  - Full legal move validation via `chess.js`, including **Castling**, **En Passant**, **Pawn Promotion** (interactive modal), **Check**, **Checkmate**, and **Stalemate/Draw** detection.
  - Play against the built-in **Wizard AI** (Minimax with center-control heuristics) or **2-Player Pass & Play**.
- **Cathedral Acoustics (Web Audio Synthesizer)**
  - Zero external audio assets required—uses **Tone.js** cathedral reverb, membrane synths, pink-noise bursts, and polyphonic chimes for stone slides, impacts, shatters, and fanfare.
- **Single-Level Material Design 3 UI**
  - Frosted-glass (`backdrop-filter: blur`) top status bar and bottom navigation dock providing one-click access to all controls without nested menus.

---

<!-- STREAMING_CHUNK:Adding interactive controls and navigation reference... -->
## 🎮 Controls & Navigation

| Control / Gesture | Action |
| :--- | :--- |
| **Left Click / Tap Piece** | Select a piece and display legal moves (blue discs) and captures (crimson reticles) |
| **Left Click / Tap Target Square** | Execute move or trigger an attack lunge & 3D shatter |
| **Click + Drag / Touch Drag** | Orbit the camera 360° around the cathedral altar |
| **Mouse Wheel / Pinch** | Zoom camera in and out |
| **vs Wizard AI / 2P Toggle** | Switch between AI opponent and local 2-player Pass & Play |
| **View Preset Button** | Cycle between *Marble*, *Obsidian*, *Top-Down*, and *Cathedral* camera angles |
| **Hint Button** | Highlight a recommended tactical move in emerald green |
| **Undo Button** | Revert the previous move (or full turn pair against the AI) |
| **Sound Toggle** | Mute or unmute procedural Tone.js cathedral audio |
| **New Game** | Reset all 32 pieces with a ceremonial rising animation |

---

<!-- STREAMING_CHUNK:Writing quick start and deployment instructions... -->
## 🚀 Quick Start (Local Development)

Because the entire application is self-contained inside `index.html`, no build step or bundler is required.

### Option 1: Open Directly
Simply double-click `index.html` to open it in any modern desktop or mobile web browser (Chrome, Firefox, Edge, Safari).

### Option 2: Run with a Local Server
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/wizards-chess-3d.git
cd wizards-chess-3d

# Serve using Python 3
python3 -m http.server 8080

# Or using Node.js serve
npx serve .
```
Then visit `http://localhost:8080` in your browser.

---

<!-- STREAMING_CHUNK:Outlining GitHub Pages hosting and repository structure... -->
## 🌐 Deploying to GitHub Pages

This repository includes an automated GitHub Actions workflow (`.github/workflows/deploy.yml`).

1. Push your code to the `main` branch on GitHub.
2. Go to your repository **Settings** → **Pages**.
3. Under **Build and deployment** → **Source**, select **GitHub Actions**.
4. Your playable 3D Wizard's Chess game will automatically deploy to `https://YOUR_USERNAME.github.io/REPO_NAME/`.

---

## 📁 Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── deploy.yml   # Automated GitHub Pages deployment workflow
├── index.html           # Complete single-file 3D WebGL application (HTML/CSS/JS)
├── LICENSE              # MIT License
├── .gitignore           # Ignored OS and editor files
└── README.md            # Project documentation
```

---

## 🛠️ Tech Stack

- **[Three.js (r128)](https://threejs.org/)** — 3D WebGL rendering, procedural geometry, PBR materials, shadow mapping, and particle physics.
- **[Chess.js (v0.10.3)](https://github.com/jhlywa/chess.js)** — Complete chess rules engine, FEN/SAN parsing, and legal move generation.
- **[Tone.js (v14.8.49)](https://tonejs.github.io/)** — Real-time procedural Web Audio synthesis and cathedral convolution reverb.
- **[Tailwind CSS](https://tailwindcss.com/)** & **Google Material Symbols** — Responsive Material Design 3 glassmorphism HUD.

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](./LICENSE) for full details.