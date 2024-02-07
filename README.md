# Face Tracking Application

This project is a face tracking application developed using Python and OpenCV. It showcases the application of computer vision techniques to dynamically track a face in real-time through a webcam feed.

## How It Works

The application initially employs the Haar Cascade Classifier to detect faces in the first frame captured from the webcam. Upon detecting the face, it designates a Region of Interest (ROI), which is crucial for the subsequent tracking process. Real-time tracking is then accomplished using the Continuously Adaptive Mean Shift (CamShift) algorithm. 

### CamShift Algorithm

CamShift (Continuously Adaptive Mean Shift) extends the Mean Shift algorithm by continuously updating the size and orientation of the window used for tracking. This adaptability makes it particularly suited for tracking faces that move and rotate in the video.

- **Initialization**: Starts with a user-defined or detected ROI that identifies the target (in this case, a face).
- **Color Histograms**: Utilizes color histograms within the ROI for the tracking basis, making it robust against variations in lighting and the target's orientation.
- **Adaptive Window**: Dynamically adjusts the tracking window's size and rotation to match the target's shape and movement, ensuring consistent tracking even as the face moves or changes expression.
- **Back Projection**: Applies back projection of the color histogram to locate the target in each frame, guiding the CamShift algorithm to adjust the tracking window accordingly.

### Key Technologies

- **Python**: The primary programming language used for developing the application.
- **OpenCV (cv2)**: Offers comprehensive computer vision functionalities, including the Haar Cascade Classifier for face detection and the CamShift algorithm for adaptive face tracking.
