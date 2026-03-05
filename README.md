# ✨ Particle Morph v2

### Real-Time Hand Gesture Controlled 3D Particle System

---

## 🎬 What Is This?

**Particle Morph v2** is a real-time interactive 3D particle engine that responds to your hand gestures using your webcam.

It combines:

* 🖐 Computer Vision (Hand Tracking)
* 🌌 WebGL 3D Rendering
* ⚡ Real-Time Physics Simulation
* 🎨 Dynamic Visual Effects

Move your hand.
Change the shape.
Trigger explosions.
Control color.

All in the browser.

---

# 🚀 Live Interaction Guide

| Gesture                   | What Happens                    |
| ------------------------- | ------------------------------- |
| ✋ Move Hand Up            | Particles morph into a Heart ❤️ |
| ✋ Move Hand Down          | Particles morph into Saturn 🪐  |
| 🤏 Quick Pinch            | Triggers Burst Explosion 💥     |
| 👉 Move Finger Left/Right | Changes Particle Colors 🎨      |
| ✋ Move Hand Around        | Moves Entire Particle System 🌀 |

---

# 🧠 How It Works (Behind the Scenes)

## 1️⃣ Hand Tracking Engine

* Uses MediaPipe Hands
* Detects 21 hand landmarks
* Tracks:

  * Index fingertip (Landmark 8)
  * Thumb tip (Landmark 4)
* Pinch gesture detected by measuring fingertip distance

If distance < threshold → Burst Mode Activated

---

## 2️⃣ Particle System Architecture

* 12,000 particles
* Built using `THREE.BufferGeometry`
* Custom target position morphing
* Velocity-based explosion physics
* Additive blending for glowing effect
* Smooth interpolation using LERP

Each frame:

* If normal mode → particles move toward target positions
* If burst mode → particles move via velocity vectors with damping

---

## 3️⃣ Shape Generation Logic

### ❤️ Heart Shape

Generated using parametric heart equation:

x = 16sin³(t)
y = 13cos(t) − 5cos(2t) − 2cos(3t) − cos(4t)

---

### 🪐 Saturn System

* 40% particles form a sphere (planet core)
* 60% particles form rotating ring structure

---

### 💥 Burst Mode

* Random spherical velocity vectors assigned
* Gradual velocity decay (friction effect)
* Creates dynamic explosion animation

---

# 🛠 Technology Stack

* Three.js (WebGL Rendering)
* MediaPipe Hands (Computer Vision)
* JavaScript (ES Modules)
* HTML5
* CSS3
* WebRTC Camera API

No frameworks.
No build tools.
Pure browser-based interaction.

---

# 📦 Installation & Setup

### 1️⃣ Clone the Repository

```
git clone https://github.com/yourusername/particle-morph-v2.git
```

---

### 2️⃣ Start a Local Server

(Webcam will NOT work with file://)

Using Python:

```
python -m http.server 8000
```

---

### 3️⃣ Open in Browser

```
http://localhost:8000
```

Allow camera permission when prompted.

---

# ⚡ Performance Notes

* Works best in Chrome or Edge
* GPU acceleration recommended
* Requires webcam access
* Designed for desktop experience
* Particle count: 12,000 (GPU dependent)

---

# 🎯 What This Project Demonstrates

✔ Real-time computer vision integration
✔ WebGL particle optimization
✔ Physics-based animation
✔ Gesture recognition logic
✔ Procedural geometry generation
✔ Creative coding + visual design

---

# 🔮 Future Improvements

* More morph targets (Galaxy, DNA, Face Mesh)
* Audio-reactive particle mode
* UI toggle controls
* Adjustable particle density
* Mobile optimization
* Post-processing bloom effects

---

# 👨‍💻 Author

Built as an exploration of real-time graphics, gesture interaction, and creative web engineering.

---

# 📜 License

Open-source for educational and experimental use.

---

⭐ If you found this interesting, consider starring the repository.
