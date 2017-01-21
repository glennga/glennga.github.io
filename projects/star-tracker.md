---
layout: project
type: project
image: images/locate-stars-test.jpg
title: Star Tracker
permalink: projects/star-tracker
date: 2015
labels:
  - Spacecraft
  - Astronomy
  - C++
summary: Development of star-based attitude estimation algorithms. 
---

<img class="ui image" src="{{ site.baseurl }}/images/location-and-brightness-test.png">

Spacecraft star tracking refers to matching stars given in a detector to their position in a database to derive an attitude relative to Earth. Once specific stars are known, an attitude relative to the Earth can be obtained. From here the craft can direct their propulsion systems, orient their solar panels, and/or move their payload accordingly. 

One current method for LEO (Low Earth Orbit) attitude extraction involves two sensors (a Sun sensor and an accelerometer for Earth's gravity). A minimum of two vectors are necessary to represent rotation across an frames. A star-tracker is able to act without relying on additional sensors and is under significantly less constraints than the combo described above. 

I developed a star-tracker agent under the COSMOS framework that takes an image as input, and updates a "state of health" stream with relavent attitude information. The general steps I used to extract a quaternion attitude from an image are below:

1. Identify the mass centers and grayscale values of the blobs in the image. These are the stars. 
2. Calculate the area/perimeter for a trio of stars. Match these stars with a area/perimeter in an inertial frame (lookup table). Repeat this until a match is found.
3. Draw vectors to two of known stars in image, and inertial vectors to the same two stars in catalog.
4. Generate quaternion attitude with TRIAD.

I learned a lot about what I wanted to do after college from this project. Prior to this, I found enjoyment is just typing code into a text editor and watching it run. During this project, I had to learn so much of the math and formal algorithms behind a seemingly magic piece of machinery. As much as I banged my head against the wall trying to understand these concepts, I later realized that I love this type of work. It was here I decided that I want to go into math/computer science research.A

I have a LinkedIn SlideShare presentation [here](http://www.slideshare.net/GlennGalvizo/hsfl-star-tracker-presentation).

Some of this project is proprietary, you can contact me directly for more information regarding the process described above.
