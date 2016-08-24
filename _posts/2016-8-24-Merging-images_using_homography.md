---
layout: post
title: Generating basic Panoramas using Homographies
published: true
comments: true
---

I got interested in Homography a few days back since it was needed for my research. So I though why not do a simple tutorial showing how to use OpenCV to generate a basic panorama.

But! for that you need to understand what a Homography is. Go through section 2.1 and 2.2 of this paper (Malis): <https://hal.archives-ouvertes.fr/file/index/docid/174739/filename/RR-6303.pdf>

To summarize it: Suppose we have two images of the same _planar_ object with some overlap between them. Let p1 be the pixel coordinates [p1x, p1y, 1] of a point in 1st image and p2 be the pixel coordinates [p2x, p2y, 1] of a point in the 2nd image. Let us call the 1st image as the destination image and the 2nd image as the source image. The Homography <sup>1</sup>H<sub>2</sub> relates every pixel coordinate in the 2nd image to a pixel coordinate in the 1st image.

```math
p1 = 1H2 * p2
```

If you think of the 1st image in a bigger canvas where everything surrounding it is black (since we don't have data around it), the related pixel coordinates from the second image will bring in more data and will stick around those black part! Think about this :)

Anyways, I wanted to get started with coding this Homography retrieval using OpenCV in C++. To find the homography between any two source and destination images, we need to have at-lest 4 point to point correspondences. Getting these correspondences are easy if you use some kind of feature detector and match them via their descriptors. Examples of some feature detectors are SIFT, SURF, ORB etc etc. We will stick to SIFT here. They are a bit slow compared to other options but are most accurate.

1. So we start with 2 images. Image 1 is the destination and Image 2 is the source. Both have some overlap between them.
![Image 1](/images/1.jpg "Destination Image")
![Image 2](/images/2.jpg "Source Image")
