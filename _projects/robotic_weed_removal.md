---
layout: page
title: Robotics Weed Removal
description: We introduce our progress of complicated weed detection, sparying based weeding robots and active perception guided field navigation using boston dynamics quadrupedal robot SPOT mini with arm system. 
img: assets/img/Robotics_weed_removal.png
importance: 1
category: work
years: [2023, 2022, 2021]
---
## __Stage 1: Perception__
#### __Toward Robotic Weed Control: Detection of Nutsedge Weed in Bermudagrass Turf Using Inaccurate and Insufficient Training Data__


To enable robotic weed control, we develop algorithms to detect nutsedge weed from bermudagrass turf. Due to the similarity between the weed and the background turf, manual data labeling is expensive and error-prone. Consequently, directly applying deep learning methods for object detection cannot generate satisfactory results. Building on an instance detection approach (i.e. Mask R-CNN), we combine synthetic data with raw data to train the network. We propose an algorithm to generate high fidelity synthetic data, adopting different levels of annotations to reduce labeling cost. Moreover, we construct a nutsedge skeleton-based probabilistic map (NSPM) as the neural network input to reduce the reliance on pixel-wise precise labeling. We also modify loss function from cross entropy to Kullback-Leibler divergence which accommodates uncertainty in the labeling process. We implement the proposed algorithm and compare it with both Faster R-CNN and Mask R-CNN. The results show that our design can effectively overcome the impact of imprecise and insufficient training sample issues and significantly outperform the Faster R-CNN counterpart with a false negative rate of only 0.4%. In particular, our approach also reduces labeling time by 95% while achieving better performance if comparing with the original Mask R-CNN approach.

##### __Algorithm__
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/weed_detection_alg.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


##### __Dataset__
<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/data_col.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/data_syn.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


The dataset can be found in this [webpage](http://telerobot.cs.tamu.edu/weed-detection/)

---
## __Stage 2: Planning and Full System__

### __Weed Sprayer__
Weed competition is one of the most limiting factors affecting crop yield and profitability. Robotic weeding systems have demonstrated their potential to save herbicide usage and thereby minimize costs and adverse impacts on the environment. We introduce the software and hardware design of an automatic system for micro-volume herbicide spray using a mobile robot for early-stage weed control. The system is equipped with a stereo camera, one inertial measurement unit, and multiple linearly actuating spray nozzles. To enable the system, we propose a new scene representation from the perspective of spray operation. We represent the space occupied by weeds as candidate line segments for spray and then construct a directed acyclic graph (DAG) that embraces the feasible nozzle paths among weeds. Based on the new scene representation, we formulate an optimal K-nozzle assignment/motion planning problem and develop a binary linear programming-based algorithm to assign nozzles to the candidate line segments for optimal coverage. We built the system and conducted both simulation and field experiments. Evaluation on rough soil surfaces with artificial targets has shown that the lateral errors of herbicide spray are at sub-centimeter levels. Simulation results demonstrate that the proposed assignment algorithm can provide good coverage within the intra-row regions. 

<p align="center">
    <img src="{{ 'assets/img/sparyer_real.gif' | relative_url}}" />
</p>

<div class="caption">
    Hardware demostration of weed sprayer
</div>

<p align="center">
<img src="{{ 'assets/img/spary_experiment.gif' | relative_url}}" />
</p>
<div class="caption">
    Tri-layer weed Representation construction from the weed detection and spray planning
</div>

### __Weed Flamer__




<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/spot_system_pipeline_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    System Design Diagram for Spot Weed Flamer
</div>

<p align="center">
<img src="{{ 'assets/img/Weed_experiment_4x.gif' | relative_url}}" />
</p>
---

{: #publications}
## __Publications__

<div class="publications">
{% for y in page.years %}
  {% bibliography -f weed_paper_list -q @*[year={{y}}]* %}
{% endfor %}
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Poster-robotic-weed-removal.bmp" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


