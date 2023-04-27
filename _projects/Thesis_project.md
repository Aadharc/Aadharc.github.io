---
layout: page
title: Image Fusion for Misaligned Thermal and Visual Images
description: 
img: assets/img/fusion.gif
importance: 1
category: Thesis
---

The main challenge of a Wilderness Search and Rescue (WiSAR) mission is to cover a large area within a reasonable and short amount of time effectively. The recent development in the area of sensor-equipped Unmanned Aerial Vehicles (UAV) and object detection algorithms have pushed the idea of using UAVs equipped with appropriate sensors for the surveillance of the area and finding humans in an efficient and time-saving way. The present work discusses a novel deep learning approach using Generative Adversarial Network (GAN) with two Discriminators and a Masked-Feature Extractor, to fuse the images (inputs) obtained from the Visual and the Thermal cameras to address the diverse terrain and weather conditions which can be experienced during the search and rescue operation. The proposed solution utilizes a GAN network based on Pix2Pix but with two discriminators as opposed to one. The results obtained further motivate the idea of developing an end-to-end pipeline for human detection in a wilderness environment using both, visual and thermal images as inputs.

<div class="row">
    <div class="col-sm mt-3 mt-md-0" style="text-align:center">
        {% include figure.html path="assets/img/Visual.jpeg" title="Visual Image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig 1: An example of visual image from the <a href="https://sites.google.com/uw.edu/wisard/">Wilderness Search and Rescue Dataset (WiSARD)</a>.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0" style="text-align:center">
        {% include figure.html path="assets/img/Thermal.jpeg" title="Thermal Image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig 2: An example of thermal image of the same scene from the <a href="https://sites.google.com/uw.edu/wisard/">Wilderness Search and Rescue Dataset (WiSARD)</a>.
</div>

Both images shown above, though taken at the same exact moment, are different in terms of resolutions, field of view, and scale. These differences come from the different camera properties and lense parameters. To leverage the available information from both images and fuse them together, these differences should be addressed and reduced to a minimum. Thats where a Generative Adversarial Network (GAN) can help. I am working on a customized GAN network to address the misalignment of two images and fuse them together. Below are some preliminary results of my method.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/results.jpg" title="Thermal Image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/results2.jpg" title="Thermal Image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fig 3: The results after training the network on a diversed dataset. The images on the far right are generated/fused images of the respective thermal image (left) and visual image (right). 
</div>


