# **Finding Lane Lines on the Road** 

---
**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report
---

My video link:
https://www.youtube.com/watch?v=xLowGZHIgow

### Reflection

## 1. Pipeline description:
My pipeline consisted of following 5 steps:
1. I converted the images to grayscale.
2. then I applied Gaussian Smoothing the image.
3. I use OpenCV to perform Canny Edge Detection on the smoothed grayscale image.
4. I define a region of interest and use OpenCV to perform Hough Transform on it to get line segments of lanes.
5. In order to draw a single line on the left and right lanes, I use draw_lines_extrapolate() to calculate an average slope / intercept of line segments to extrapolate to left lane and right lane.
6. Finally I draw the line_image to the original image.

## 2. Potential shortcomings 
I found an exception caused by a frame with 0 left lane segments when processing solidYellowLeft.mp4.
This exception was handled but I'm afraid there are more exceptions if used different parameters for Smoothing / Canny / Hough / Mask .

## 3. Possible improvements
It seems my extrapolated lane is not as stable as P1_example.mp4, maybe I should try more parameter fine tuning. 

