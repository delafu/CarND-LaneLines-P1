# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"
[image2]: ./test_images/solidWhiteCurve.jpg "Sample 1"
[image3]: ./test_images_ouput/solidWhiteCurve.jpg "Sample 1 with Lines"


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consists of 6 steps:

* Convert the image to the gray scale
* Apply a Gaussian Blur filter
* Find edges using Canny edge detector
* Define the region that is interesting to find lanes
* Run the Hough Transform to find the lanes
* And last draw the lines

I´m happy with the results I´ve obtained in the static images and in the first two videos, but I have to work to fix the challenge video. 

[image1]
[image2]



I´m going to explain some of the steps of the pipeline.

### Find edges using Canny edge detector

I´ve used similar parameters that I used in the lesson and I think that I got a good result.

### Define the region that is interesting to find lanes

I´ve used a practical method and I´ve selected a polygon based in the height and width of the image and from testing some different values. 

### Run the Hough Transform to find the lanes

I´ve run the Hough Transform with values like used in the lessons and they work very well with exception of very shiny images.

### Draw the lines

This was the most tricky part. I calculated the lines using the average slope, x and y of the lines obtained from the Hough transform. I discarded the horizontal (or near horizontal)lines and then using the equation y=mx+b I was able to calculate the lines from the bottom of the image to the top of the region of interest. All of this work is done in the avg_lines function.

I used a moving average to stabilize the video. When I did not use the lines move too much. 

I´ve drawn the lines for the videos using weighted_img function to get a transparent effect. I had to create a black image and draw the lines on it and then call to the weighted function.

### Identify potential shortcomings with your current pipeline

My current pipeline does not work very well in the challenge video. I think that one of the problems is that has problems with shinny images.

I think that the pipeline will have problems in curves


### 3. Suggest possible improvements to your pipeline

A potential improvement could be to detect white and yellow lines instead of all the lines in the image.

Another improvement would be to give more value to the lines near the observer.


