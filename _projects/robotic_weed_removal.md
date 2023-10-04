---
layout: page
title: Robotic Weed Removal
description:  Weed detection, sparying based weeding robots and active perception guided manipulation. 
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

### __Weed Flamer and Coupled Active Perception and Manipulation(CAPM) Algorithm__

#### Weed Flamer Hardware & Software System

<div class="row">
<div class="row align-items-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flamer_robot_platform.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/flamer_software_system.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
</div>
Robotic weed flaming provides an environmentally friendly approach to removing weeds in the agricultural field. Here we present a robotic weed-flaming solution using a 6 degrees of freedom (DoF) manipulator mounted on a quadrupedal robot. The mobile manipulator system includes overall design, hardware integration, and software pipeline. We propose a flame model with an estimation method that uses a center-arc curve with a Gaussian cross-section model to describe the flame coverage in real time.  
The experiments have demonstrated the working system and shown that our model and algorithm can achieve a mean average precision (mAP) of more than 76% in the reprojected images during online prediction.
<!-- <div class="caption">
    System Design Diagram for Spot Weed Flamer
</div> -->


#### CAPM Algorithm
<div class="row">
    <div class="col-sm mt-6 mt-md-0">
            {% include figure.html path="assets/img/capm.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
A mobile manipulator often finds itself in an application where it needs to take a close-up view before performing a manipulation task. Named this as a coupled active perception and manipulation (CAPM) problem, we model the uncertainty in the perception process and devise a key state/task planning approach that considers reachability conditions as task constraints of both perception and manipulation tasks for the mobile platform. By minimizing the expected energy usage in the body key state planning while satisfying task constraints, our algorithm achieves the best balance between the task success rate and energy usage. We have implemented the algorithm and tested it in both simulation and physical experiments. The results have confirmed that our algorithm has a lower energy consumption compared to a two-stage decoupled approach, while still maintaining a success rate of 100% for the task.     


#### Experiment
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




