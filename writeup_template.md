# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

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

I´m happy with the results I´ve obtained in the static images and in the first two videos, but I have to work to fix the challenge video that is horrible. I´m going to explain some of the steps of the pipeline.

### Find edges using Canny edge detector

I´ve used a very similar parameters that I used in the lesson and I think that I have a good result.

### Find edges using Canny edge detector

I´ve used a practical method and I´ve selected a polygon 




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
