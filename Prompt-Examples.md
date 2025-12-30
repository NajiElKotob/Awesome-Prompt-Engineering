# Prompt Examples

---
## Interactive Hand-Controlled 3D Particle System

## Objective
Create a **high-performance, single-file HTML5/JavaScript application** that demonstrates a **real-time, gesture-controlled 3D particle system** using **Three.js** and **MediaPipe Hands**.  
The solution must be technically stable, visually polished, and robust enough for a **live presentation**.



## 1. Visual Architecture

### Engine
- Use **Three.js** with a **BufferGeometry** approach to efficiently handle **20,000 particles** on the CPU/GPU.

### Aesthetics
- Implement a **dark-mode environment** with **AdditiveBlending** to create a neon / energy-glow effect.
- Instead of square points, generate a **procedural radial-gradient texture** using an HTML canvas to give particles a soft, organic **“orb”** appearance.
- Particles must transition between the following target geometries:
  - **Sphere**
  - **Heart**
  - **Cube**
  - **Archimedean Spiral**

### Morphing
- Use **interpolated transitions** (linear interpolation or spring-based physics).
- Shapes should **flow smoothly** into each other every **5–7 seconds**.



## 2. Hand Tracking & Coordinate Mapping

### Vision Engine
- Use **MediaPipe Hands** via CDN.
- Enable `maxNumHands: 1` to maintain performance.

### Interaction Mirroring
- Mirror the webcam input so the user’s **right hand controls the right side** of the particle scene for intuitive interaction.

### Spatial Scaling
- Map MediaPipe’s normalized **[0, 1]** coordinates to the Three.js world space.
- Example: map hand movement to a **-500 to +500** coordinate range so gestures cover the full viewport.



## 3. Advanced Gesture & Physics Logic

### Responsive Physics
- Each particle must maintain:
  - Position
  - Velocity
  - Acceleration
- Apply a **damping (friction) factor** to avoid erratic motion and jitter.

### Open Hand — Repulsion
- Identify the **INDEX_FINGER_TIP** landmark.
- Compute a **distance-squared repulsion force**.
- Particles within a defined radius are pushed away from the hand position.

### Closed Fist — Singularity
- Detect a fist by evaluating the **proximity of finger tips** to the wrist or knuckles.
- **Action:** Switch the global force to **Attraction**.
- Particles accelerate toward the scene origin **(0, 0, 0)** while the fist remains closed, creating a **“black hole”** effect.


## 4. UX & Technical Constraints

### Zero Configuration
- No build tools (Vite, Webpack, etc.).
- Use **ES Modules or global scripts via CDN only**.

### Robustness
- Display a minimal **UI overlay** showing:
  - Tracking Status
  - Current Shape Mode
- Handle webcam permissions gracefully:
  - If denied, display a **“Camera Required”** message.
- Optimize the animation loop to maintain **~60 FPS** on modern hardware.

### Documentation
- Include **inline code comments** focusing on:
  - Force calculation logic
  - Hand-to-3D coordinate transformation

---
