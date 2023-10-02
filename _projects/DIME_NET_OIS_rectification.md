---
layout: page
title: DIME NET (Camera OIS rectification)
description: A neural network-based approach that estimates camera intrisic matrix in real time so that pose estimation or scene reconstruction can be run at camera native resolution for the highest accuracy on the mobile devices.
img: assets/img/OIS.png
importance: 2
category: work
years: [2023]
---

### DIME-Net: Neural Network-Based Dynamic Intrinsic Parameter Rectification for Cameras with Optical Image Stabilization System
Optical Image Stabilization (OIS) system in mobile devices reduces image blurring by steering lens to compensate for hand jitters. However, OIS changes intrinsic camera parameters (i.e. K matrix) dynamically which hinders accurate camera pose estimation or 3D reconstruction. Here we propose a novel neural network-based approach that estimates K matrix in real time so that pose estimation or scene reconstruction can be run at camera native resolution for the highest accuracy on the mobile devices.
Our network design takes gridified projection model discrepancy feature and 3D point positions as inputs and employs a Multi-Layer Perceptron (MLP) to approximate f(K) manifold. We also design a unique training scheme for this network by introducing a Back propagated PnP (BPnP) layer so that reprojection error can be adopted as the loss function. The training process utilizes precise calibration patterns for capturing accurate f(K) manifold but the trained network can be used anywhere. We name the proposed Dynamic Intrinsic Manifold Estimation network as DIME-Net and have it implemented and tested in three different mobile devices. In all cases, DIME-Net can reduce reprojection error by at least 64% indicating that our design is successful.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/OIS.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


DIME-Net architecture and training scheme. This pipeline reflects the process of training the DIME-Net. In the inference stage, a user only needs the grey box to estimate K and the pose can be calculated using standard PnP algorithm
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DIME_NET.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

{: #publications}
## __Publications__
<div class="publications">
{% for y in page.years %}
  {% bibliography -f ois_paper -q @*[year={{y}}]* %}
{% endfor %}
</div>