# GestureSnap
Hand Gesture-Triggered Screenshot Capture Using OpenCV and CVZone for Beginners.

---
## Table of Contents
* [Overview](#overview)
* [Key Features](#key-features)
* [Prerequisites](#prerequisites)
* [Installation](#installation)
* [Usage](#usage)
* [How It Works](#how-it-works)
* [License](#license)

---
## Overview
GestureSnap is a beginner-friendly Python script that enables interactive screenshot capture through hand gestures detected via webcam. Using OpenCV and the CVZone library, it recognizes a specific two-finger gesture (index and middle fingers up) to trigger a full-screen screenshot, making it an engaging introduction to computer vision and gesture recognition. Ideal for novices exploring practical applications in a fun, hands-on way.

---
## Key Features
- **Effortless Gesture-Based Capture**: Raise your index and middle fingers in front of the camera to instantly take and save a screenshot.
- **Powered by OpenCV and CVZone**: Leverages robust libraries for hand tracking and image processing, providing an accessible entry point to advanced computer vision techniques.

---
## Prerequisites
- Python installed on your system (version 3.7 or higher recommended).
- A webcam connected to your device.

---
## Installation
Install the required dependencies using pip:
```bash
pip install opencv-python cvzone pyscreenshot
```

Save the script as `gesture_snap.py` (or your preferred name) and ensure it's in your working directory.

---
## Usage
1. Run the script:
   ```bash
   python gesture_snap.py
   ```
2. Face the webcam and raise your index and middle fingers (with others down) to trigger a screenshot.
3. The captured image will be saved as `shot.png` in the script's directory. An on-screen message ("SHOTTED!!!!") will confirm the action.
4. Press 'q' or 'Q' to exit the program.

---
## How It Works
- Initializes webcam capture and hand detection with CVZone's HandDetector.
- Flips the video feed for a natural mirror view.
- Continuously checks for hands; if detected, verifies the finger configuration ([0,1,1,0,0] for thumb down, index up, middle up, ring down, pinky down).
- Upon matching gesture, grabs the full screen using pyscreenshot and saves it.
- Displays the video feed with hand overlays and exits on key press.

This project is perfect for beginners to grasp core computer vision concepts while building a useful, interactive tool. Feel free to customize it—e.g., change gestures, add timestamps to filenames, or integrate with other apps—and share your creations!

---
## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute.
