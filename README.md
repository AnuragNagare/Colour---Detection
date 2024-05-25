# Colour---Detection

# RGB Color Picker with OpenCV

This project captures a real-time video feed from your webcam and allows you to click on any point in the captured frame to get the RGB color value of that point. The RGB value is displayed both in the console and on the image itself.

## Features

- Real-time video capture from webcam.
- Capture a frame by pressing 'c'.
- Get RGB values of clicked points in the captured frame.
- Display RGB values on the image.
- Exit the program by pressing 'q'.

## Requirements

- Python 3.x
- OpenCV
- NumPy

## Installation

1. Clone this repository to your local machine.
    ```sh
    git clone https://github.com/your-username/rgb-color-picker.git
    ```
2. Navigate to the project directory.
    ```sh
    cd rgb-color-picker
    ```
3. Install the required Python packages.
    ```sh
    pip install opencv-python numpy
    ```

## Usage

1. Run the Python script.
    ```sh
    python color_picker.py
    ```
2. The webcam feed will be displayed in a window titled "Real-Time Frame".
3. Press 'c' to capture the current frame. A new window titled "Captured Frame" will open displaying the captured frame.
4. Click on any point in the "Captured Frame" window to get the RGB color value of that point. The RGB value will be printed in the console and displayed on the image.
5. Press 'q' to exit the program.

Detailed Explanation
Importing Libraries
Two libraries are used:

OpenCV: For computer vision tasks and real-time image processing.
NumPy: For handling image data as arrays and performing numerical operations.
Defining the Callback Function
A callback function is defined to handle mouse events. Specifically, it triggers when the left mouse button is clicked. The function retrieves the BGR (Blue, Green, Red) color value at the clicked point, converts it to the RGB (Red, Green, Blue) format, and prints it to the console. It also displays this RGB value on the captured frame at the clicked location.

Initializing the Camera
The webcam is initialized to start capturing video. A VideoCapture object is created, which by default uses the primary camera.

Main Loop
A loop runs continuously to read frames from the webcam and display them in a window. The program waits for user input during this loop:

If the user presses the 'c' key, the current frame is captured and displayed in a new window. The mouse callback function is set for this window, allowing the user to click on points in the frame to get their RGB values.
If the user presses the 'q' key, the loop breaks, and the program terminates.
Cleanup
After exiting the loop, the program releases the webcam resource and closes all OpenCV windows to ensure that all resources are properly freed and the application terminates cleanly.
