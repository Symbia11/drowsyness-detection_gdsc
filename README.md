# drowsyness-detection_gdsc
A project by students of Vidyalankar School Of Information Technology
This code can detect your eyes and alert when the user is drowsy.

Applications 🎯

This can be used by riders who tend to drive for a longer period of time that may lead to accidents

Code Requirements 🦄

The example code is in Python (version 3.9 or higher will work).

Dependencies

import cv2
import pygame

Description 📌

A computer vision system that can automatically detect driver drowsiness in a real-time video stream and then play an alarm if the driver appears to be drowsy.

Algorithm 👨‍🔬

* Alert Sound Function:*

play_alert_sound():
Initializes Pygame's mixer for playing audio.
Loads the audio file "a.wav" for playback.
Plays the loaded audio.

* Eye Detection:*

Loads a pre-trained haarcascade_eye.xml file containing eye detection features.
Creates a video capture object (cap) to access the webcam.

* Main Loop:*

Reads each frame from the webcam (ret, frame).
Converts the frame to grayscale for better object detection.
Uses the eye_cascade object to detect eyes in the grayscale frame.
scaleFactor: Adjusts the image search size.
minNeighbors: Minimum number of neighbors required for a detection.
minSize: Minimum size of an eye region to be considered.
Checks if eyes are detected (len(eyes) == 0).
If no eyes found:
Plays the alert sound using play_alert_sound().
Prints "no" and waits until the sound finishes playing.
Draws green rectangles around detected eyes.
Displays the frame with detected eyes.
Exits the loop if the 'q' key is pressed.

*Cleanup:*

Releases the video capture object.
Closes all OpenCV windows.

Execution 🐉

To run the code, type python hel.py

References 🔱

.Google Gemini AI
