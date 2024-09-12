# Real-Time Object Detection using YOLOv8 and Python

## Introduction
In this project, I implemented **real-time object detection** using the **YOLOv8 architecture**. My goal was to detect objects in both images and video streams efficiently, leveraging the power of deep learning. YOLOv8 was chosen for its balance between accuracy and speed.

## Video Demonstration

You can watch a demonstration of the results [here](Object_Detection_Output.mp4).

Or download the video directly:

[Download the video](Object_Detection_Output.mp4)

## Key Components
- **YOLOv8**: Utilized the YOLOv8 model for object detection due to its optimized performance.
- **Python & Jupyter Notebooks**: Employed Python for scripting and Jupyter notebooks for experimentation.
- **OpenCV for Video Processing**: Integrated for real-time video analysis.
- **Model Inference**: Performed object detection using pre-trained YOLOv8 weights on both images and video streams.

## Steps
### 1. Dataset Preparation
Collected and processed data for testing the object detection model. The images were resized and normalized to match the input requirements of YOLOv8.

### 2. Model Selection
I selected the **YOLOv8n** variant for its lightweight architecture, suitable for real-time applications with limited computational resources.

### 3. Inference on Images and Video
The model was tested on a series of images and video streams, applying real-time detection and labeling. Detection results included bounding boxes, class labels, and confidence scores.

### 4. Results
The system successfully identified and labeled objects in real time, proving its efficiency in both static and video-based inputs.

## Challenges
- **Balancing Accuracy and Speed**: Ensuring high accuracy without sacrificing real-time performance.
- **Handling Various Object Sizes**: Managing detection for both large and small objects in different contexts.
- **Image Quality**: Detecting objects in varying conditions such as low light and motion blur.

## Conclusion
This project showcases the ability of **YOLOv8** to perform real-time object detection with high accuracy, even in dynamic video streams. It can be applied to a variety of fields, including surveillance and real-time analytics.

## Future Improvements
- Fine-tuning the model for specific use cases such as pedestrian or vehicle detection.
- Enhancing performance under challenging conditions like low light and occlusions.
- Implementing tracking across multiple frames to improve detection consistency.

---

## Example Usage

### Inference on an Image:
```python
from ultralytics import YOLO

# Load model and image
model = YOLO('yolov8n.pt')
results = model('path/to/image.jpg')

# Display results
results.show()
