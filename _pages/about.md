---
layout: about
title: about
permalink: /
subtitle: PostDoc @ UCB, Ph.D. @ TAMU 

profile:
  align: right
  image: photo.jpg
  image_circular: true # crops the image to make it circular

news: true  # includes a list of news items 
latest_posts: false  # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}" 
# social: true  # includes social icons at the bottom of the page
---
<div class="chip-row">
  <a class="chip" href="mailto:syxie@berkeley.edu">email</a>
  <a class="chip" href="https://scholar.google.com/citations?user=nrnJBX0AAAAJ&hl=en">google scholar</a>
  <a class="chip" href="https://www.linkedin.com/in/syxie-/">linkedin</a>
  <a class="chip" href="https://x.com/shuangyu0_0xie">x / twitter</a>
</div>

I am a Postdoctoral researcher in the [AUTOLab](https://autolab.berkeley.edu/) at UC Berkeley, working with [Prof. Ken Goldberg](https://goldberg.berkeley.edu/). Prior to joining UC Berkeley, I obtained my Ph.D. and M.S. degree from Texas A&M University, advised by [Prof. Dezhen Song](https://mbzuai.ac.ae/study/faculty/dezhen-song/).  My research aims to make robots more capable and resilient in unstructured environments, spanning applications in manipulation, mobile manipulation and agricultural robotics. 


<div class="section-block corl-section">
<h2 class="section-title"><span class="lbr">CoRL</span> 2026 Presentations</h2>
<p class="corl-lead">Come see me in Austin, November 9&ndash;12.</p>
  <article class="corl-talk">
    <a class="corl-media" href="https://berkeleyautomation.github.io/flipanything/" aria-label="Flip Anything with Agentic Robotics Self-Learning project page"><video src="/assets/video/corl2026/flip.mp4" poster="/assets/video/corl2026/flip.jpg" autoplay muted loop playsinline preload="metadata"></video></a>
    <div class="corl-body">
      <h3><a href="https://berkeleyautomation.github.io/flipanything/">Flip Anything with Agentic Robotics Self-Learning</a></h3>
      <ul class="corl-sessions"><li class=""><span class="when">Monday, Nov 9, 12:00&ndash;1:30 PM</span><span class="what"><b class="lbr">Late-Breaking Result</b>, board 131, Griffin, JW Marriott (Level 2)</span></li></ul>
      <div class="chip-row"><a class="chip" href="https://berkeleyautomation.github.io/flipanything/">project page</a><a class="chip" href="https://openreview.net/forum?id=Oq2jahhF6r">openreview</a></div>
    </div>
  </article>
  <article class="corl-talk">
    <a class="corl-media" href="https://robosimstudio.github.io" aria-label="RoboSimStudio: An Interactive Toolkit for Rapid Real2Sim of Robot Manipulation Tasks project page"><video src="/assets/video/corl2026/rss.mp4" poster="/assets/video/corl2026/rss.jpg" autoplay muted loop playsinline preload="metadata"></video></a>
    <div class="corl-body">
      <h3><a href="https://robosimstudio.github.io">RoboSimStudio: An Interactive Toolkit for Rapid Real2Sim of Robot Manipulation Tasks</a></h3>
      <ul class="corl-sessions"><li class=""><span class="when">Tuesday, Nov 10, 12:00&ndash;1:30 PM</span><span class="what"><b class="lbr">Late-Breaking Result</b>, board 122, Griffin, JW Marriott (Level 2)</span></li><li><span class="when">Thursday, Nov 12, afternoon</span><span class="what"><b class="oral">Oral, PhysWM Workshop</b></span></li></ul>
      <div class="chip-row"><a class="chip" href="https://robosimstudio.github.io">project page</a><a class="chip" href="https://openreview.net/forum?id=mxGqlrfUvR">openreview</a><a class="chip" href="https://arxiv.org/abs/2610.18835">arxiv</a><a class="chip" href="https://github.com/robosimstudio/robosimstudio">code</a></div>
    </div>
  </article>
  <article class="corl-talk">
    <a class="corl-media" href="https://graph-robots.github.io/gap/" aria-label="GaP: A Graph-as-Policy Multi-Agent Self-Learning Harness for Variational Automation Tasks project page"><video src="/assets/video/corl2026/gap.mp4" poster="/assets/video/corl2026/gap.jpg" autoplay muted loop playsinline preload="metadata"></video></a>
    <div class="corl-body">
      <h3><a href="https://graph-robots.github.io/gap/">GaP: A Graph-as-Policy Multi-Agent Self-Learning Harness for Variational Automation Tasks</a></h3>
      <ul class="corl-sessions"><li><span class="when">Wednesday, Nov 11, 8:30&ndash;9:00 AM</span><span class="what"><b class="spot">Spotlight S6</b>, Hilton Austin</span></li><li class=""><span class="when">Wednesday, Nov 11, 10:30 AM&ndash;12:00 PM</span><span class="what"><b>Poster 100</b>, Poster Session 3, JW Marriott, Lone Star (3rd floor)</span></li></ul>
      <div class="chip-row"><a class="chip" href="https://graph-robots.github.io/gap/">project page</a><a class="chip" href="https://openreview.net/forum?id=C96z0RnFh8">openreview</a><a class="chip" href="https://arxiv.org/abs/2607.05369">arxiv</a><a class="chip" href="https://github.com/graph-robots/graph-as-policy">code</a></div>
    </div>
  </article>
</div>

<div class="section-block" markdown="1">
<h2 class="section-title">Research Highlights</h2>

My recent work explores how **Vision-Language Models and robotics can advance each other**: real robot experience provides the grounded, embodied data that VLMs need, while VLMs bring the open-world semantic understanding that robots need to perceive, reason, and act. I pursue this along three threads:

- **Learning VLMs from robot experience.** [Robo2VLM](https://berkeleyautomation.github.io/robo2vlm/) (NeurIPS 2025, <em>Spotlight</em>) turns large-scale, in-the-wild robot manipulation datasets into grounded visual question-answering data, using the robot’s own sensing and kinematics to supervise VLM training and evaluation.
- **Evaluating VLMs for robotics.** [RoboVista](https://berkeleyautomation.github.io/robovista) (RSS 2026) is the first robot-at-work benchmark that evaluates VLMs across diverse real-world robot deployments—manipulation, driving, and surgical scenes—with a public [leaderboard](https://berkeleyautomation.github.io/robovista/leaderboard.html).
- **Understanding and curating robot data with VLMs.** [RoboSQ](https://berkeleyautomation.github.io/robosq/) (ICRA 2026) is a semantic query engine that uses natural language to curate high-quality, task-aligned training data from large robot datasets, and [RoboSegNet](https://berkeleyautomation.github.io/RoboSegNet/) (CVPR 2026) fuses vision and kinematics to segment robot trajectories into meaningful sub-tasks, zero-shot.

I also build **agentic harnesses that turn foundation models into deployable robot policies**. [GaP: Graph-as-Policy](https://graph-robots.github.io/gap/) (CoRL 2026, <em>Spotlight</em>; with NVIDIA) represents a robot policy as an executable behavior graph: a team of LLM agents writes the graph from a plain-language task description, grounds it in an open robot-skills library, verifies it, and improves it in NVIDIA Isaac simulation before running it on real UR5e and Franka robots. Across grocery fulfillment, packing, popcorn making, cable insertion, and bimanual crate washing, GaP reaches 0.93–0.99 success under pose variation. [Paper](https://arxiv.org/abs/2607.05369) · [Code](https://github.com/graph-robots/graph-as-policy) I also released the [Open Gemini 4 Argon Robot Harness](https://ehehee.github.io/blog/open-gemini-harness/), an open, bimanual implementation of the harness in Google's Gemini 4 Argon robotics report: grid-overlay observations, skill programs, and human or automatic motion checking. On two YAM arms, Gemini handed over and placed a tape roll and a spring clamp zero-shot, with no task-specific training or demonstrations. [Report](https://ehehee.github.io/blog/open-gemini-harness/) · [Code](https://github.com/ehehee/open-gemini-robot-harness) · [Video](https://x.com/Shuangyu0_0Xie/status/2112947017236258997)
</div>


