# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

---

|solid white right|solid yellow left|
|:--------:|:--------:|
|[solidWhiteRight](./test_videos_output/solidWhiteRight.gif)|[solidYellowLeft](./test_videos_output/solidYellowLeft.gif)|


**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg "solidWhiteCurve"
[image2]: ./test_images_output/solidWhiteRight.jpg "solidWhiteRight"
[image3]: ./test_images_output/solidYellowCurve.jpg "solidYellowCurve"
[image4]: ./test_images_output/solidYellowCurve2.jpg "solidYellowCurve2"
[image5]: ./test_images_output/solidYellowLeft.jpg "solidYellowLeft"
[image6]: ./test_images_output/whiteCarLaneSwitch.jpg "whiteCarLaneSwitch"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

* My pipeline consisted of 6 steps.
1. RGB convert to gray
2. Define kernel size and apply Gaussian smoothing
3. Define the threshold of candy and apply candy 
4. Define region of interest
5. Define the parameters of hough and apply hough transform
6. Blend lane and image

* how you modified the draw_lines() function.
1. Distinguish left and right lane with the slope
2. Calcute the avergae of the slope respectively
3. Calcute the max value and min value of y axis, then get the corresponding values of x axis.

> In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]
![alt text][image2]
![alt text][image3]
![alt text][image4]
![alt text][image5]
![alt text][image6]
