# Interactive Hand Gesture Drawing Application

## Introduction

This project implements an interactive hand gesture drawing application using computer vision techniques. The application allows users to draw on a canvas using hand gestures captured by a webcam. It leverages libraries such as OpenCV, NumPy, and Mediapipe for image processing, numerical computations, and hand tracking, respectively.

## Technologies Used
Computer Vision , Python , MediaPipe, OpenCV


## Features

1. **Library Imports**:
   - **cv2**: OpenCV library for image processing and computer vision tasks.
   - **np**: NumPy library for numerical computations, especially array manipulation.
   - **mediapipe**: A library providing ready-to-use machine learning solutions for various tasks, including hand tracking.
   - **deque** from **collections**: A double-ended queue data structure used for efficient handling of drawing points.

2. **Canvas Setup**:
   - The `paintWindow` variable initializes a blank canvas for drawing, represented as a NumPy array.
   - Rectangles are drawn on the canvas to represent different colors (blue, green, red, yellow) and a clear button.
   - Text labels are added to indicate the functionality of each rectangle (clear button and color options).

3. **Hand Tracking and Gesture Recognition**:
   - The code initializes the `Hands` class from the `mediapipe` module to detect hand landmarks in each frame captured by the webcam.
   - Hand gestures are recognized based on the positions of these landmarks. For example, a gesture near the color rectangles indicates color selection, while a gesture near the clear button indicates clearing the canvas.

4. **Drawing Implementation**:
   - Arrays (`bpoints`, `gpoints`, `rpoints`, `ypoints`) are initialized to store points for drawing in different colors.
   - Lines are drawn on the canvas and the frame based on the movement of the hand and the selected color. The `deque` data structure ensures that the number of points remains limited, preventing memory overflow.

5. **User Interaction**:
   - Users interact with the application through hand gestures captured by the webcam.
   - Hand movements are translated into drawing actions on the canvas, such as drawing lines or selecting colors.
   - The application responds to gestures by updating the canvas and displaying the changes in real-time.

6. **Main Loop**:
   - The main loop continuously captures frames from the webcam, processes them, and updates the canvas and frame accordingly.
   - It terminates when the user presses the 'q' key, indicating a desire to exit the application.

## Conclusion

This project provides a foundation for an interactive drawing application where users can draw using hand gestures. By leveraging hand tracking and gesture recognition techniques, the application offers a unique and intuitive way to interact with the drawing interface.
