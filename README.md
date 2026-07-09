# Bee Yogi – Yoga Pose Detection

A desktop application that uses computer vision to detect and score yoga poses in real time. Built with **Tkinter** for the GUI, **MediaPipe** + **OpenCV** for pose estimation, and **Firebase (via Pyrebase)** for user accounts and progress tracking.

## Features

- User registration, login, OTP-based password reset, and profile management
- A library of 24 yoga poses with reference images and instructional videos
- Real-time webcam pose detection and accuracy scoring using MediaPipe
- Visual accuracy meter and per-user daily progress tracking stored in Firebase

## Project Structure

```
YogaPoseDetection-main/
├── main1.py          # Application entry point
├── main.py           # Alternate/legacy GUI entry point
├── getDB.py          # Firebase (Pyrebase) database helper functions
├── meter1.py         # Accuracy meter UI logic
├── pr.py             # Scratch/test script
├── requirements.txt  # Python dependencies
├── GUIImage/          # UI screenshots and icons
├── perform/           # Pose reference images
├── sliderimage/       # Homepage slider images
├── meter/             # Accuracy meter images
└── video/              # Instructional pose videos
```

## Prerequisites

- Python 3.7 – 3.10 recommended (MediaPipe has limited support for newer versions)
- A webcam
- The packages listed in `requirements.txt`, plus `mediapipe` and `opencv-python`, which aren't pinned there but are required (see below)

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Varad1230/Yoga-Pose-Detection.git
   cd Yoga-Pose-Detection/YogaPoseDetection-main
   ```

2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   venv\Scripts\activate        # Windows
   source venv/bin/activate     # macOS/Linux

   pip install -r requirements.txt
   pip install mediapipe opencv-python numpy
   ```

3. Run the application:
   ```bash
   python main1.py
   ```

## Firebase Configuration

This project uses a Firebase Realtime Database (via `getDB.py`) for user accounts, authentication, and progress data. The repository includes a demo Firebase project configuration for convenience. To use your own Firebase backend, replace the `firebaseConfig` values in `getDB.py` with your own project's credentials from the [Firebase console](https://console.firebase.google.com/).

## Tech Stack

- **GUI:** Tkinter, Pillow
- **Computer Vision:** OpenCV, MediaPipe
- **Backend/Database:** Firebase Realtime Database via Pyrebase

## License

No license has been specified for this project.
