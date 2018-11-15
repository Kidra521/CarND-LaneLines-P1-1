# **Finding Lane Lines on the Road** 


## Self Driving Car

## Udacity Self Driving Car Nanodegree 

### This document describe the methods to find the lane lands. 

---

**Finding Lane Lines on the Road**

The tools you have are color selection, region of interest selection, grayscaling, Gaussian smoothing, Canny Edge Detection and Hough Tranform line detection. The goals / steps of this project are the following:
* Color selection. The channel threshold should be properly tuned.
* Region masking to find the Region Of Interest(ROI). Remove other stuff.
* Turn the RGB to GrayScale.
* Image noise elimination.
* Edge detection. Use Canny, and just cv2.canny().
* Hough transform. Tune the parameters to get proper lane line.
* Some linear regression to eliminate noise segment,connect/average/extrapolate the line segments.
* Generate new image files and highlight the laneline on it.
* Manage the lanelines object data for further utility.


[//]: # (Image References)
[image0]: ./examples/course/image0.png "Origin"
[image1]: ./examples/grayscale.jpg "Grayscale"
[image2]: ./examples/course/image2.png "Edge"
[image3]: ./examples/course/image3.png "Hough_bad"
[image4]: ./examples/course/image4.png "Hough_good"
[grayscale]: /examples/grayscaleimage.jpg "pureGrayScale"
[grayscale_blur]: /examples/grayscaleblur.jpg "GrayScale_Removenoise"
[grayscale_noise]: /examples/grayscalenoise.jpg "GrayScale_noise"
[edgedetection_noblur]: /examples/edgedetection_noblur.jpg "edgedetection_noblur"
[edgedetection_blur]: /examples/edgedetection_blur.jpg "edgedetection_blur"

![alt text][image0]
![alt text][image1]![alt text][image2]![alt text][image3]![alt text][image4]

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...

### 4. What happen to the grayscale GaussianBlur is implemented?
![grayscale][grayscale]
![alt text][grayscale_blur]
![alt text][grayscale_noise]
![alt text][edgedetection_noblur]
![alt text][edgedetection_blur]     
After the cv2.GaussianBlur(), we could see the picture seems less clear, but from the different between these two pics we can see GaussianBlur can remove much noise, and it is helpful for next step.
