# CourtVision.Ai
An AI-powered mobile application that turns a smartphone into a real-time tennis referee. Designed for recreational players who don’t have access to line judges or Hawk-Eye systems.
📌 Overview

AI Referee for Amateurs is a mobile app that uses a smartphone camera placed at mid-court to automatically detect:

✅ Out-of-bounds shots

✅ Foot faults

✅ Ball trajectory

✅ Real-time line calls

The app provides fair, instant, and unbiased decisions — making amateur matches more professional and dispute-free.

🚀 Problem Statement

Recreational tennis players often face:

Disputes over line calls

No access to professional review systems

Unfair advantages due to incorrect judgments

Interruptions during gameplay

Professional systems like Hawk-Eye are expensive and unavailable to amateurs.

💡 Solution

Place a smartphone at mid-court on a tripod.
The app uses computer vision and AI to:

Detect the tennis ball

Track its trajectory

Identify court boundary lines

Determine if the ball is IN or OUT

Detect foot faults during serves

Provide instant visual and audio feedback

🧠 Tech Stack

Python

OpenCV

YOLO / Custom Object Detection Model

TensorFlow / PyTorch

Mobile Integration (Flutter / React Native – Optional)

Real-time Video Processing

Homography & Perspective Transformation

🏗️ System Architecture
Camera Input
     ↓
Ball Detection Model
     ↓
Trajectory Tracking
     ↓
Court Line Detection
     ↓
Boundary Intersection Logic
     ↓
Decision Engine (IN / OUT / FOOT FAULT)
     ↓
Audio + Visual Feedback

📲 How It Works

Mount phone at mid-court.

Start match recording.

App detects court lines automatically.

AI tracks ball frame-by-frame.

When ball lands:

Calculates landing coordinate.

Compares with court boundaries.

Announces result instantly.

🎯 Features

🎥 Real-time ball tracking

📍 Precise boundary detection

🔊 Audio call (“Out!”, “In!”, “Foot Fault!”)

📊 Match analytics (optional future feature)

📱 Works with just a smartphone

💰 Affordable alternative to professional systems

📈 Impact

Reduces arguments between players

Makes amateur matches more professional

Encourages fair play

Affordable officiating system

Useful for schools, clubs, and local tournaments

🛠️ Future Improvements

Multi-camera support

Score tracking integration

Slow-motion replay

Cloud-based analytics

AI training mode for coaching

Doubles court support

🧪 Installation (Prototype Version)
git clone https://github.com/madHAVgupta2008/COURTVISION.AI
cd ai-referee-tennis
pip install -r
python main.py

📂 Project Structure
ai-referee-tennis/
│
├── models/
├── data/
├── main.py
├── detection.py
├── tracking.py
├── utils.py
├── requirements.txt
└── README.md

🤝 Contribution

Contributions are welcome!

Fork the repository

Create a new branch

Commit your changes

Submit a pull request

👤 Author

Developed for hackathons and amateur sports innovation.
Created by Madhav Gupta and Jatin Jain
