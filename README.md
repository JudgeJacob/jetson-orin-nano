# Jetson Orin Nano Gesture Recognition

A real-time hand gesture recognition project running on the NVIDIA Jetson Orin Nano Super using MediaPipe and OpenCV.

## Features

- Hello gesture detection
- Thumbs Up gesture detection
- Thumbs Down gesture detection
- One Finger gesture detection
- Real-time FPS display
- Live camera feed processing

## Hardware

- NVIDIA Jetson Orin Nano Super
- USB Webcam

## Software

- Ubuntu (JetPack 6.2.1)
- Python 3
- OpenCV
- MediaPipe

## Credits

This project was originally based on the Cytron Technologies tutorial:

[Gesture Recognition with NVIDIA Jetson Orin Nano Super]

(https://my.cytron.io/tutorial/nvidia-jetson-orin-nano-super-gesture-recognition&tracking=yt-products&utm_campaign=yt-products)

I extended the project by:

- Fixing missing gesture detection functions
- Troubleshooting MediaPipe runtime errors
- Adjusting gesture thresholds for reliable detection
- Adding documentation and testing

## Issues Encountered

### Missing Function Error

While running the original code:

```python
elif is_only_one_gesture(hand_landmarks):
```

the following error occurred:

```text
NameError: name 'is_only_one_gesture' is not defined
```

Cause:

The function was referenced but not defined in the script.

Solution:

Implemented the missing function:

```python
def is_only_one_gesture(hand_landmarks):
    ...
```

### Thumbs Up / Thumbs Down Detection Failure

Problem:

The Good and Bad gestures were not being detected.

Cause:

The original threshold:

```python
curled_threshold = 0.1
```

was too restrictive for my camera setup.

Solution:

Increasing the threshold improved recognition:

```python
curled_threshold = 0.15
```

## Demo

### Hello Gesture



### Thumbs Up



### Thumbs Down



## Demo Video



## Future Improvements

- Additional hand gestures
- Multi-hand support
- Gesture-based robot control
- TensorRT acceleration
- Custom-trained gesture models

## Author

Jacob Hernandez

Computer Engineering Technology

Focused on AI, Robotics, Embedded Systems, and NVIDIA Jetson Development.
