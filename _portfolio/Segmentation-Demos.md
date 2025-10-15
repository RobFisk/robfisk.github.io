---
title: "Demonstrating Computer Vision Tools for Elevation Models"
excerpt: "Part of a summer project on using machine learning to identify plant species from drone images. Learned about and implemented cutting edge computer vision models and demonstrated their strengths and weakness for a dataset of field images in East Ayrshire from the project.<br/><img src='/images/unsam.jpg' width='400'>"
collection: portfolio
---

For the second half of my summer project on Monitoring Vegetation using Machine Learning, I quickly realised that to feed a DEM into a classifier, I'd first need to segment it. Initially, we'd hoped to demonstrate a classifier working on these segmented images but due to time constraints had to settle for simply demonstrating the classifiers worked. These time constraints mostly came because after Glasgow didn't get the funding for my summer research I had decided to take on the project part time to allow me to still do paid work while gaining experience. 

The segmentation models one of my supervisors was interested in were SAM (Segment Anything Model) and UnSAM (Unsegmented SAM) as well as a precursor, the CutLer (Cut and Learn) algorithm. Using the research papers and github pages for these, I wanted to demonstrate how current model checkpoints would handle the DEMs I created in the first part of the project. 

Due to a combination of poor documentation, issues with the CoLab environment I was working in and a variety of version dependency clashes between the most up to date versions of UnSAM's pre-requisites it took a long time to get code working. Solving the challenges I came across with version dependencies required going through each package and checking what numpy and pytorch versions I could match them with and often installing these before running the setup files for packages like detectron2 (the install for which I have particular beef with). After this I ran into the UnSAM model running out of memory on the GPU, but not reporting this and showing an error in a much different part of the code afterward. It took tracing the code as if I was debugging it to find this memory issue, which in the end I fixed by keeping the GPU clear and reducing the quality of images I provided to the models. This may have slightly impacted the results, but the code I wrote could run with higher-quality images if one had access to a better GPU than I did in my CoLab notebook. 

In the end, I was able to produce masks which can be visualised like this:

<p float="left">
  <img src="/images/projects/vegetation/field_out_sam.jpg" width="400" />
  <img src="/images/projects/vegetation/trees_out_unsam.jpg" width="400" />
</p>

As well as a good tutorial for anyone who might be interested in doing something similar in [this presentation](https://docs.google.com/presentation/d/e/2PACX-1vThJUS9vCFha2E8BJjK5JllxjjLLoIoG34YQ0fSfWR3SXIf3pZzb0vvRDceYtkCTiXWrW5Ds-laCpmZ/pub?start=false&loop=false&delayms=3000).

Overall, the project showed that the process for turning drone images to segmented DEMs could be done in a streamlined way, but there were definitely areas the models could be improved upon. Without going into too much detail these include better training on images of field/forest terrain, where the differences in greens are less sharp than the colour differences the models will be used in most photographs and a modification to the UnSAM algorithm which would allow elevation values to be passed in addition to RGB images. 

My supervisors (Doctors Tiffany Vlaar and Paul Eizenhoefer) said they were really impressed with what I'd been able to deliver while only working part time on the project and with so little support, and they loved how I'd remained focused on setting up future PhD research into the area throughout my project and while presenting my findings. We developed a great working relationship and I'm extremely grateful for their support in providing data, recommending research papers and being another set of eyes on the project. At the end they also offered me a chance to work on a Data Science PhD with them - I might take this up one day but for now would like to get some industry experience first. 

Skills:
 * Research Skills
 * Python
 * Google Colab
 * Computer Vision
 * Perservearance
 * Presenting Findings
