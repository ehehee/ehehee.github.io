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
### __Nutsedge Detection__
The dataset can be found in this [webpage](http://telerobot.cs.tamu.edu/weed-detection/)

---
## __Stage 2: Planning and Full System__

### __Weed Sprayer__



### __Weed Flamer__



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
<div class="caption">
    This image can also have a caption. It's like magic.
</div>


