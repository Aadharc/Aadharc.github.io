---
layout: page
title: Image Fusion for Misaligned Thermal and Visual Images
description: 
img: assets/img/fusion.gif
importance: 1
category: Thesis
---

Autonomous systems rely on various sensors, such
as visual cameras (including stereo pairs), thermal
cameras, Radio Detection and Ranging (RADAR) and
Light Detection and Ranging (LiDAR), to understand
and navigate their surroundings, make decisions, and
complete desired tasks. However, each of these these
sensor modalities have limitations which, if not compensated
for, can negatively impact the performance
of autonomous systems. Combining multiple
types of sensors together allows autonomous systems
to experience the benefits of sensors collectively
while offsetting their individual weaknesses. This is
called sensor fusion, which is, fusing the complementary
data from different sensors to generate richer
and more meaningful data. One such task is image
fusion, where images from different cameras are fused
together and can be used in practical applications such
as autonomous driving and video surveillance (e.g.
Wilderness Search and Rescue). The present project
focuses on image fusion using thermal and visual
cameras in particular.


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


