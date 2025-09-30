---
title: "Processing LIDAR images to create elevation models"
excerpt: "Part of a summer project on using machine learning to identify plant species from drone images. Learned to use pix4dmapper and QGIS to process LIDAR images into an elevation model (DEM), as well as creating an educational resource to help taught Master's students at the University of Glasgow to do the same.<br/><img src='/images/stew_point_cloud.png' width='400'>"
collection: portfolio
---

As part of a research project on Monitoring Vegetation usign Machine Learning, I had to learn how to proccess UAV drone images into a single model which could be fed to a classifier. This model is called a DEM (Digital Elevation Model) and is basically a terrain map with elevation included. As someone with an entirely maths/computing background this was a very new skill for me but by the end I was able to produce the high-quality DEM required for the second half of the project. I also produced an educational resource for future Master's degree students looking to recreate the process I followed, [this presentation](https://docs.google.com/presentation/d/e/2PACX-1vSRN8-KrVAjVregGT4YcsfJy95HziA0Ptze673Tc1jmIZrzZC7Ete-s77bCYYi-7iL69NWtwKKw4ZmY/pub?start=false&loop=false&delayms=3000), which my supervisors were grateful for.

I had to work in the software Pix4d, QGIS and R to:
    - Load UAV images
    - Triangulate using control points on the ground
    - Produce a point cloud of pixels from the drone images
    - Thin the point cloud to only include so many pixels per metre
    - Classify the points that make up the ground level
    - Filter the cloud to only include these points
    - Generate Red, Green, Blue and elevation rasters
    - 

Having taught myself these skills mostly independently I was proud of my ability to do this and hope that creating an educational resource on the topic will make it easier for others to learn.

The some of the DEMs produce can be seen here from a top-down view (RGB, no z):

<p float="left">
  <img src="/images/projects/vegetation/field.jpg" width="400" />
  <img src="/images/projects/vegetation/trees.jpg" width="400" />
</p>


Skills Developed:
 * QGIS
 * Research Skills
 * Presenting
 * Adapting to new software