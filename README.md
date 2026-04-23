<div align="center">

# 🚇 Subway Surfers - OpenCV Controller
**Play Subway Surfers using Hand Gestures and Body Pose!**

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)](https://opencv.org/)
[![MediaPipe](https://img.shields.io/badge/MediaPipe-Latest-orange.svg)](https://google.github.io/mediapipe/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


</div>

## 📖 Introduction
This project allows you to play the popular endless runner game, **Subway Surfers**, entirely hands-free! By utilizing **Computer Vision (OpenCV)** and **MediaPipe**, the script tracks your body/hand movements through your webcam and translates them into keyboard inputs in real-time.

## ✨ Features
- **Real-Time Tracking:** High-performance hand and pose detection using Google's MediaPipe.
- **Virtual Keyboard Simulation:** Uses `PyAutoGUI` to seamlessly trigger arrow keys.
- **Customizable Thresholds:** Easily adjust movement sensitivity based on your webcam distance.
- **Low Latency:** Optimized for smooth gameplay without noticeable input lag.

## 🛠️ Tech Stack
- **Python** - Core programming language
- **OpenCV** - Video capturing and image processing
- **MediaPipe** - Machine learning pipeline for pose/hand landmark detection
- **PyAutoGUI** - Cross-platform GUI automation (simulating key presses)

## 💻 Installation

**1. Clone the repository:**
```bash
git clone https://github.com/Lalitchauhan52/Subway-Surfer-OpenCV.git
cd Subway-Surfer-OpenCV
```

**2. Create a virtual environment (optional but recommended):**
```bash
python -m venv venv
# Activate on Windows:
venv\Scripts\activate
# Activate on Mac/Linux:
source venv/bin/activate
```

**3. Install dependencies:**
```bash
pip install -r requirements.txt
```
*(If you don't have a requirements.txt, run: `pip install opencv-python mediapipe pyautogui`)*

## 🎮 How to Play

1. Open **Subway Surfers** (either the web version on Poki or a desktop emulator).
2. Run the main python script:
   ```bash
   python main.py
   ```
3. **Make sure the game window is in focus!**
4. Stand in front of your webcam and use the following gestures:
   - **Move Left:** Lean or swipe your hand to the Left ⬅️
   - **Move Right:** Lean or swipe your hand to the Right ➡️
   - **Jump:** Move upward ⬆️
   - **Roll:** Move downward ⬇️

## 🧠 How it Works
1. **Capture:** OpenCV captures the live video feed from your webcam.
2. **Process:** The frames are converted to RGB and passed to MediaPipe.
3. **Detect:** MediaPipe extracts 3D coordinates (x, y, z) of specific body landmarks (like shoulders, wrists, or nose).
4. **Action:** The script calculates the relative distance of these landmarks from a neutral center position. If a movement crosses a predefined threshold, `PyAutoGUI` triggers the corresponding arrow key!

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

## 👨‍💻 Author
**Lalit Chauhan**
- GitHub: [@Lalitchauhan52](https://github.com/Lalitchauhan52)

---
⭐️ If you like this project, please give it a star on GitHub!
