# CourtVision.Ai 🎾🏸

> **Dual-Sport AI Analysis System (Tennis & Badminton)**  
> *Professional Line Calling & Analytics using YOLOv26 & Computer Vision*

![Version](https://img.shields.io/badge/version-0.1.0-blue.svg) ![Status](https://img.shields.io/badge/status-active_development-orange.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg) ![Python](https://img.shields.io/badge/python-3.9%2B-blue.svg)

## 📖 Overview

**CourtVision.Ai** is a cutting-edge mobile application and AI system that turns a standard smartphone into a professional-grade real-time referee and analytics platform. Following the architectural principles of industry leaders like SwingVision, this system adapts advanced computer vision for a dual-sport setup: **Tennis** and **Badminton**.

Designed for recreational players who lack access to expensive Hawk-Eye systems, CourtVision.Ai provides fair, instant, and unbiased line calls, eliminating disputes and bringing a professional vibe to every match.

---

## 🚀 Problem & Solution

### The Problem
Recreational players often face:
- ❌ **Disputes**: Arguments over line calls interrupt the flow of the game.
- ❌ **Unfairness**: Lack of neutral officiating leads to frustration.
- ❌ **Cost**: Professional systems (Hawk-Eye) are prohibitively expensive and unavailable for local courts.

### The Solution
A "Visual Brain" in your pocket. By placing a smartphone at mid-court, CourtVision.Ai uses:
- ✅ **Computer Vision**: To track the ball/shuttlecock in real-time.
- ✅ **Spatial Mapping**: To understand court boundaries with centimeter-level precision.
- ✅ **Instant Feedback**: Audio and visual cues for "IN", "OUT", and "FOOT FAULT".

---

## 🏗️ The 5-Phase "Vibe Coding" Blueprint

Our development follows a structured, modular approach to ensure robustness and scalability.

### Phase 1: The "Visual Brain" (Detection) 👁️
- **Dual-Model Approach**: Separate YOLOv26 models for Tennis (ball) and Badminton (shuttlecock) to handle distinct physics.
- **Source**: Fine-tuned models from Roboflow Universe.
- **Integration**: TensorFlow Lite (TFLite) for efficient edge processing on mobile devices.
- **Core Function**: High-speed tracking and trajectory visualization (5-frame tail).

### Phase 2: The "Spatial Brain" (Court Mapping) 📐
- **Keypoint Detection**: OpenCV-based identification of court corners and line intersections.
- **Perspective Correction**: Homography matrix transformation converting 2D video feeds into a "flat" 3D world coordinate system.
- **Boundary Logic**: Precise "IN" vs "OUT" regions mapped to standard court dimensions.

### Phase 3: The "Referee" (Real-Time Call) ⚖️
- **Physics-Based Decision Engine**:
  - **Tennis**: Detects "Bounce" events (V-shape trajectory inflection).
  - **Badminton**: Detects "Floor Hits" (Altitude $Z$ reaches 0).
- **Feedback**: Instant "OUT" audio trigger and on-screen score updates.
- **Foot Faults**: Monitors the baseline during service.

### Phase 4: The "Analyst" (Post-Match Intelligence) 🧠
- **Data Logging**: Exports detailed match CSVs: `[Timestamp, Shot_Type, Speed, Landing_Zone, Outcome]`.
- **Pattern Recognition**: Custom AI agents (via Edge Impulse/Vertex AI) analyze play styles.
- **Pro Insights**: "You lose 70% of points on deep cross-court shots."

### Phase 5: The "Multi-Sport" Tech Stack 💻

| Component | Technology |
| :--- | :--- |
| **Object Detection** | Ultralytics YOLOv26 / Custom Models |
| **Computer Vision** | OpenCV, Homography, Perspective Transform |
| **ML Framework** | TensorFlow / PyTorch / TFLite (Mobile) |
| **App Interface** | Lovable.dev / Flutter / React Native |
| **Language** | Python (Core Logic) |
| **Data Platform** | Supabase (Logs & Stats) |
| **AI Training** | Edge Impulse (Custom Logic) |

---

## 🎯 Key Features

- **🎥 Real-Time Tracking**: Frame-by-frame analysis of ball/shuttlecock trajectory.
- **📍 Precise Line Calling**: Automated decision-making for boundary hits.
- **🔊 Audio Referee**: Instant voice announcements ("Out!", "Fault!").
- **📊 Smart Analytics**: (Upcoming) Match stats, heatmaps, and speed analysis.
- **📱 Accessible**: Works with just a smartphone and a tripod.

---

## 🛠️ Installation (Prototype)

To run the Python-based prototype:

```bash
# Clone the repository
git clone https://github.com/TeamOpaque/CourtVision.Ai
cd CourtVision.Ai

# Install dependencies
pip install -r requirements.txt

# Run the main application
python main.py
```

### Project Structure
```
CourtVision.Ai/
│
├── models/          # YOLO & TFLite models
├── data/            # Test videos and datasets
├── main.py          # Entry point
├── detection.py     # Object detection logic
├── tracking.py      # Trajectory tracking
├── referee.py       # In/Out logic
├── utils.py         # Helper functions
├── requirements.txt
└── README.md
```


## 🤝 Contribution

Contributions are welcome! We are building this for the love of the game.
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## 👤 Authors

**Team Opaque**  
Developed for hackathons and amateur sports innovation.

- **Madhav Gupta**
- **Jatin Jain**

---
*Built with ❤️ and AI Assistance*
