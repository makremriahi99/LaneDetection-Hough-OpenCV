# Lane Detection — Hough Transform + OpenCV

Real-time **road lane detection** using OpenCV's Probabilistic Hough Transform (`HoughLinesP`), applied to a highway photo taken with a mobile phone.

## What it does

- Loads and auto-rotates a road image (90° counterclockwise correction)
- Applies **Gaussian blur** to reduce noise before edge detection
- Detects edges with **Canny** algorithm (thresholds: 50/150)
- Applies an **ROI mask** (lower half of image — sky/vegetation ignored)
- Runs **HoughLinesP** to find lane segments
- Classifies lines as left/right lane by slope sign
- Averages multiple segments → single representative line per side
- Draws a **semi-transparent red overlay** on the lane area
- Draws **yellow lane lines** extended beyond image borders
- Computes and annotates **asphalt width in pixels**

## Results

```
Lines detected left:  7
Lines detected right: 3
Left slope:   -1.359  |  intercept: 540.7
Right slope:   0.873  |  intercept: -118.6
Asphalt width at y=284: 272.2 px
```

## Tech stack

- Python 3
- `opencv-python` (`cv2`) — image processing
- `numpy` — matrix operations

## Usage

Place a road photo named `strada2.jpg` in the working directory, then open `notebook.ipynb` and run all cells. Output saved as `LaneDetection.jpg`.

## Topics

`python` `opencv` `computer-vision` `hough-transform` `lane-detection` `autonomous-driving`
