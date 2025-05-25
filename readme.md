Virtual Steering Controller
Description
Virtual Steering Controller is a computer vision project that enables steering control through hand gestures detected via a webcam. Using MediaPipe's hand detection and OpenCV, the script tracks the positions of both hands (wrist landmarks) to determine gestures, triggering keyboard inputs to simulate turning left, right, moving straight, or moving back. This project addresses the need for hands-free navigation, offering an interactive solution for applications like gaming, virtual driving simulations, or robotic control, with real-time visual feedback on the webcam feed.
Installation/Usage
Installation

Clone the Repository:
git clone https://github.com/your-username/virtual-steering-controller.git
cd virtual-steering-controller


Install Dependencies:Ensure Python 3.7 or higher is installed, then install the required libraries:
pip install opencv-python mediapipe numpy

Note: The script also uses a custom keyinput module (included below) for Windows-specific keyboard input simulation. Ensure your system supports this (Windows only).

Set Up Your Environment:

Ensure you have a webcam connected to your computer.
Position yourself so that both hands are visible to the webcam.



Usage

Run the Script:
python virtual_steering_controller.py


Perform Hand Gestures:

Turn Left: Position your hands with the left hand higher and to the right of the right hand (or vice versa) with a vertical difference > 65 pixels.
Turn Right: Position your hands with the right hand higher and to the left of the left hand (or vice versa) with a vertical difference > 65 pixels.
Move Straight: Keep both hands aligned horizontally with a vertical difference < 65 pixels.
Move Back: Use only one hand in the frame.
The script will simulate keyboard inputs (a for left, d for right, w for straight, s for back) and display the action on the screen.
Press q to exit the application.


On-Screen Feedback:

The webcam feed shows:
Hand landmarks and connections.
A green circle and lines indicating gesture detection.
Text labels ("Turn left", "Turn right", "keep straight", "keeping back") at the top-left corner.





Technologies Used

Python: Core programming language for the project.
OpenCV: Handles webcam video capture and image rendering.
MediaPipe: Provides real-time hand detection and landmark tracking.
NumPy: Used for mathematical computations, such as coordinate calculations.
Custom keyinput Module: Implements Windows-specific keyboard input simulation (included in the script).

Challenges & Learning

Challenge: Accurately detecting hand positions and distinguishing gestures under varying lighting and hand orientations.
Solution: Adjusted min_detection_confidence and min_tracking_confidence to 0.5 and used a vertical difference threshold (> 65 pixels) to improve gesture recognition.


Challenge: Ensuring smooth keyboard input simulation without conflicts.
Solution: Implemented release_key and press_key functions using Windows API to manage key states effectively.


Learning: Gained experience in hand landmark detection, geometric calculations for gesture recognition, and integrating computer vision with system input control.

Visuals
Add screenshots or GIFs here to demonstrate the project in action. Examples include:

Screenshot of the webcam feed showing hand landmarks, the green circle, and "Turn left" text.
GIF showing the gesture detection triggering "Turn right" or "keep straight" with corresponding keyboard inputs.

To include visuals, capture images or recordings, upload them to your GitHub repository, and link them here using Markdown image syntax, e.g., ![Demo](path/to/image.png).
