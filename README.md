# Hand-Gesture-Recognition-

================================================================
           HAND TRACKER - README
           Built with OpenCV + MediaPipe
================================================================
WHAT THIS PROJECT DOES
-----------------------
This project uses your webcam to detect and track your hands
in real time. It can:
  - Detect up to 2 hands at the same time
  - Draw a skeleton (21 landmarks) on your hand
  - Count how many fingers are raised
  - Identify hand gestures (Fist, Peace, Thumbs Up, Open Hand,Index Up, Call Me, Rock On, Thumbs Up, Pinky Up, Four Fingers, Four + Thumb)
  - Label each hand as Left or Right correctly
  - Show live FPS (frames per second)

----------------------------------------------------------------
REQUIREMENTS
----------------------------------------------------------------
  - Windows 10 or 11
  - Python 3.13 (already installed)
  - A working webcam
  - VS Code (already installed)
  - Internet connection (only needed for first run to
    download the hand landmark model)
 
----------------------------------------------------------------
FOLDER STRUCTURE
----------------------------------------------------------------
  Human Posture/
  |
  |-- handposture.py         (main Python script)
  |-- hand_landmarker.task   (auto-downloaded on first run)
  |-- README.txt             (this file)

----------------------------------------------------------------
HOW TO INSTALL (One Time Only)
----------------------------------------------------------------
  Step 1: Open VS Code
  Step 2: Open the Terminal
          Menu -> Terminal -> New Terminal
          OR press:  Ctrl + `
 
  Step 3: Run this command to install required libraries:
 
          pip install mediapipe opencv-python
 
  Step 4: Wait for installation to finish.
          You should see "Successfully installed" at the end.
 

----------------------------------------------------------------
HOW TO RUN THE PROJECT
----------------------------------------------------------------
  Step 1: Open VS Code
 
  Step 2: Open the project folder
          File -> Open Folder -> Select "Human Posture" folder
 
  Step 3: Open the Terminal (Ctrl + `)
 
  Step 4: Run this command:
 
          & "C:\Users\Robot\AppData\Local\Programs\Python\Python313\python.exe" "c:/Users/Robot/Desktop/Human Posture/handposture.py"
 
          OR simply click the Run button (▶) at the top right
          of VS Code after opening handposture.py
 
  Step 5: First run will show:
          "Downloading hand landmark model... please wait"
          Wait a few seconds for it to download.
 
  Step 6: Your webcam window will open automatically!
 
  Step 7: Press Q to quit the webcam window.

----------------------------------------------------------------
GESTURES DETECTED
----------------------------------------------------------------
  Fingers Up             Gesture Name
  ─────────────────────────────────────
  None (all closed)   →  Fist
  All 5 fingers       →  Open Hand
  Index only          →  Index Up
  Index + Middle      →  Peace
  Thumb + Pinky       →  Call Me
  Thumb+Index+Pinky   →  Rock On
  Thumb only          →  Thumbs Up
  Pinky only          →  Pinky Up
  Index+Middle+Ring
  +Pinky              →  Four Fingers
  All except Pinky    →  Four + Thumb
 
 
----------------------------------------------------------------
COLOUR CODES ON SCREEN
----------------------------------------------------------------
  Cyan / Green box    →  Right Hand
  Orange box          →  Left Hand
 
----------------------------------------------------------------
TROUBLESHOOTING
----------------------------------------------------------------
  Problem: "No module named mediapipe"
  Fix: Run this in terminal:
       pip install mediapipe opencv-python
 
  Problem: Webcam window does not open / black screen
  Fix: Change VideoCapture(0) to VideoCapture(1)
       in handposture.py line:
       cap = cv2.VideoCapture(0)
 
  Problem: Low FPS / slow detection
  Fix: Change resolution in handposture.py:
       cap.set(cv2.CAP_PROP_FRAME_WIDTH, 640)
       cap.set(cv2.CAP_PROP_FRAME_HEIGHT, 480)
 
  Problem: Hand not detected properly
  Fix: Make sure lighting is good.
       Keep hand clearly visible to the webcam.
 
 
----------------------------------------------------------------
LIBRARIES USED
----------------------------------------------------------------
  opencv-python  →  Webcam capture and drawing on screen
  mediapipe      →  Hand landmark detection (by Google)

================================================================
                    PROJECT BY: Human Posture
                    Language  : Python 3.13
                    Libraries : OpenCV + MediaPipe
================================================================


