# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

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


### 2. Identify potential shortcomings with your current pipeline
> The current solution can's solve the challenge video.

### 3. Suggest possible improvements to your pipeline
> Mask the bottom region of the image which not belong to lane.
