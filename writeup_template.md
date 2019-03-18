# **Finding Lane Lines on the Road** 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)
[image0]: ./test_images/solidWhiteCurve.jpg
[image1]: ./test_images_output/solidWhiteCurve_step1_grayscale.jpg "Grayscale"
[image2]: ./test_images_output/solidWhiteCurve_step2_gauss_smooth.jpg "Gauss"
[image3]: ./test_images_output/solidWhiteCurve_step3_canny.jpg "Canny"
[image4]: ./test_images_output/solidWhiteCurve_step4_region.jpg "Grayscale"
[image5]: ./test_images_output/solidWhiteCurve_step5_hough.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

The original Image looked like this,
![alt text][image0]

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

Step1 : Convert to grayscale
![alt text][image1]

Step2 : Apply Gaussian Blur
![alt text][image2]

Step3 : Apply Canny Edge Detection
![alt text][image3]

Step4 : Select the region of interest
![alt text][image4]

Step5 : Apply probabilistic Hough transform to detect line segments
![alt text][image5]

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by making a condition for detecting the slope for two different lines i.e. left and right.

For each line, identified the first and the last points for the lane and make a line.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the car is travelling in a curved road, then it wouldn't be able to detect.

Another shortcoming could be for different weather conditions and night time, this algorithm might not work well.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to improve algorithm for taking care of the curved lines.

Another potential improvement could be to improve algorithm to also take care of the different weather conditions.
