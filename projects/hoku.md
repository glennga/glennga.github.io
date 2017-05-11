---
layout: project
type: project
image: images/locate-stars-test.jpg
title: Hoku
permalink: projects/hoku
date: 2017
labels:
  - Optimization
  - Reference Frames
  - Star Identification
summary: Research toward matching stars in an image without sky reference to a star catalog.
---

<img class="ui medium right floated rounded image" src="../images/eid-5err.png">

## Project Description 

This project aims to develop a faster, lighter, and more robust lost-in-space star identification algorithm for star trackers. 

Ancient mariners could look up at the night sky, point out what stars they were looking at, and navigate across the globe with precision. ‘Star identification algorithm’ refers to a computational approach to pointing out which stars are in the sky. If we take an image of the sky, star identification is matching the stars in the picture to stars in a astronomical catalog. The device that performs these computations is the star tracker, much like the navigators on the ship. ‘Lost-in-space’ refers to an additional constraint on the problem: the absence of knowing where we took the picture and how we pointed the camera.

This project is funded by Undergraduate Research Opportunities Program, and I am under the direction of Dr. Lipyeow Lim. The funding period for Hoku begins this August, but I have laid the foundation for this project over the past year. 

My work will be based on previous approaches to this problem: Tappe Angle Method, Cole & Crassidus Planar Triangles Method, Cole & Crassidus Spherical Triangles Method, Mortari Pyramid Method, and the Astrometry.net Method. By empirically analyzing the robustness, speed, and storage of these existing implementations, I will create a more optimal identification algorithm.

## Significance 

Star identification has its applications in general navigation, astronomical logging, and orientation determination (star trackers). 

Like ancient mariners, the idea of using the stars to navigate has grown beyond naval applications. Star navigation is currently being used as a backup to GPS on planes and on land rovers. Certain spacecraft (such as NASA’s Cassini) rely on the stars to adjust their propulsion devices and stay on course to their destination. Outside of navigation, star identification has significance with astronomical logging. If an astronomer loses the location or the camera hardware associated with his photos of the sky, star identification alone can determine both.

The absence of knowing where the given image is the portion of this project is most concerned with, as this represents our ‘lost-in-space’ constraint. The device that deals with this specific sub problem is the star tracker, a device spacecraft use to determine the craft’s orientation (attitude) using known stars. Attitude determination is essential to most space missions, as this enables the craft to direct its solar panels and payloads accordingly. A few seconds might just be enough to freeze the wrong part of the craft or power down forever. Speed and reliability are critical here, which is why a robust, fast, and lightweight star identification algorithm is important here. 

There currently exists many approaches to star identification, but many them only improve one aspect of the lost-in-space sub problem. For instance, Cole & Crassidis’s spherical and planar triangles algorithm only focus on identifying star groups- and the astrometry.net algorithm is more geared toward astronomical logging (imposing additional constraints not related to problem). The second problem is that there exists minimal experimental data regarding comparisons between different implementations of the algorithms. This work will not only present star trackers with a specific, fast, robust, and lightweight approach to the lost-in-space sub problem, but will also generate extensive empirical data between six different approaches. 

## In-Progress Comments

In the summer of 2016, I had the opportunity to volunteer at the Hawaii Space Flight Laboratory (HSFL). I was under the supervision of HSFL engineers Eric Pilger and Miguel Nunes to develop software for a first-generation star tracker. This project has also been the subject of my ICS499 project.

Switching perspectives from engineering to research really opened my eyes and has helped me lay down a foundation. One road bump I'll share was trying to map a sphere onto a plane for the generated image- it took a good month and a half between talks with Dr. Lim and hours of cartography research to just say, "Let's skip this step." But wait, how can you pick stars from an image if you don't even have an image? The answer was that our goals were different than my time at HSFL. My goal isn't to create a working star tracker, it's to analyze the underlying processes!  The lesson I took from this was to '`ctrl -`' (zoom out) every now and then and perform my sanity checks.

You can track my current progress at my GitHub repository [here](https://github.com/glennga/hoku).