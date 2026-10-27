# 🎓 Smart ID Card Exam Paper Dispenser

## Automated Color-Coded Question Paper Dispensing System

An automated computer-vision and mechatronic dispenser simulation designed for college examination halls. The system identifies a student's branch through their color-coded ID card strap and automatically feeds the corresponding color-header exam paper from dedicated motorized compartments.

---

### 🎨 Branch Color Coding Specification

| Branch | ID Strap Color | Paper Header | Course Code | Subject |
|---|---|---|---|---|
| **Computer Engineering** | 🟢 Green | Emerald Green | `CS-501` | Distributed Systems & Cloud Computing |
| **Computer Science Engineering** | 🟡 Yellow | Golden Yellow | `CSE-402` | Design & Analysis of Algorithms |
| **Mechanical Engineering** | 🟣 Purple | Royal Purple | `ME-603` | Robotics & Mechatronics Automation |
| **Electronics & CS Engineering** | 🔴 Red | Crimson Red | `ECS-504` | Embedded Systems & Sensor Interfacing |

---

### 🚀 Key Improvements & Innovations

1. **Physical Strap Tracking Engine (No More Hallucination)**
   - **Fabric-Calibrated HSL Classifier**: Tuned specifically for reflective fabric lanyards under ambient indoor room lighting (rather than bright phone screens).
   - **Skin & Neutral Rejection**: Automatically detects and ignores human skin tones (`Hue 10°–34°`) and desaturated backgrounds (walls, paper, tables).
   - **Live Augmented Reality (AR) HUD**: Directly overlays colored highlights onto the webcam feed showing **exactly** which strap pixels are being tracked in real time.
   - **Click-to-Sample Pipette**: Click anywhere on the live video stream to sample your strap's exact color under current lighting conditions.
   - **Direct Demo Buttons**: Click any of the 4 branch cards for an instant demonstration.

2. **Authentic 3D Paper Dispensing Simulation (Three.js + OrbitControls)**
   - **Procedural High-Resolution Exam Paper**: Dynamically generated 1024×1448 canvas texture featuring:
     - Prominent **color-coded header band** matching the branch
     - College university banner & branch name
     - Real exam question layout (Section A/B, marks distribution, student roll number lines, security borders)
   - **Realistic Roller Ejection Animation**:
     - Paper is fed outward from the matching slot mouth — **the colored header emerges first**!
     - Curvature under gravity as it rolls out onto the front stainless steel collection tray.
   - **Interactive 3D Controls**: Click and drag to orbit 360°, scroll to zoom in, and inspect the dispensed paper up close.

3. **Taste-Skill Compliant UI (Vercel / Linear Aesthetic)**
   - **Dark Neutral Palette**: Built with `#09090b` canvas and `#121215` elevated panels.
   - **Zero Purple/Indigo Chrome**: Free of gimmicky gradients, glows, or emojis.
   - **Technical Typography**: Tabular monospace metrics (`font-variant-numeric: tabular-nums`) displaying real-time tracking statistics (RGB, HSL, pixel count, and FPS).

---

### 🛠️ Technology Stack

- **Frontend**: HTML5, CSS3 (Modern Flex/Grid, Custom Properties)
- **Computer Vision**: HTML5 Canvas API, WebRTC MediaStreams, Real-Time HSL Chrominance Filtering
- **3D Graphics**: Three.js (WebGL), Three.js OrbitControls, Dynamic Canvas Texturing
- **Design Standard**: Taste-Skill (`anti-slop`, Linear/Vercel Dark System)

---

### 🖥️ How to Run & Present to Your Teacher

1. **Open the Project**:
   ```bash
   # If not already running:
   cd id-card-dispenser
   python3 -m http.server 8080
   ```
   Open `http://localhost:8080` in your web browser.

2. **Teacher Demonstration Steps**:
   - **Step 1 (Webcam)**: Click **Start Webcam**. Point your camera at your green ID card strap inside the reticle box.
   - **Step 2 (Visual Feedback)**: Show the teacher the **green pixel highlight overlay** on the camera feed — this proves it is tracking the actual strap fabric and not the background!
   - **Step 3 (3D Dispenser Ejection)**: Watch the 3D dispenser machine:
     - The Green (COMP) slot LED illuminates.
     - The exam paper rolls forward out of the slot, **displaying the green header first**.
     - It settles in the collection tray.
   - **Step 4 (3D Inspection)**: Use your mouse to rotate and zoom into the dispensed exam paper to show the teacher the printed college header, branch code, and questions.
   - **Step 5 (Multi-Branch Testing)**: Click any of the other branch cards (Yellow / Purple / Red) to demonstrate multi-compartment automated dispensing.
