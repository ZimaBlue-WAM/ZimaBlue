<div align="center">

<h1>ZimaBlue: Evolving Generalizable World Action Models through Scalable Video Pre-training</h1>

<p><a href="https://zimablue-wam.github.io/">Project Page</a> · Paper (Coming Soon)</p>

<p><strong>Code and model releases are in preparation.</strong></p>

</div>

<p align="center">
  <img src="assets/teaser.png" alt="ZimaBlue data scaling and acceleration results" width="100%">
</p>

## Abstract

Robotic manipulation faces a fundamental scaling challenge: robust generalization demands broad physical experience, yet action-labeled robot trajectories are expensive to collect and inherently limited in diversity. Egocentric videos offer a far more scalable source of embodied experience, capturing object interactions, contact dynamics, tool use, and long-horizon behaviors across diverse environments. The central challenge is how to convert this abundant but action-free experience into effective robot control. We introduce **ZimaBlue**, a scalable framework for learning generalizable World Action Models (WAMs) from large-scale video. ZimaBlue follows a three-stage training curriculum: it first performs causal embodied video pre-training on large-scale human and robot egocentric videos, then grounds the learned visual dynamics in heterogeneous robot trajectories through video-action mid-training with a unified action representation, and finally specializes the model to a target robot for deployment. To make generative WAMs practical for real-time control, ZimaBlue further adopts an asynchronous Slow-Fast dual-system architecture, where a high-capacity Slow world model provides generalizable spatiotemporal representations and a lightweight Fast branch enables ***30 Hz action prediction*** on an NVIDIA RTX 4090 GPU. On real-robot zero-shot evaluations, scaling from target-robot data alone to over ***120,000 hours of embodied video improves success from 36.1% to 77.8%***. ZimaBlue further delivers strong performance across multiple benchmarks, with particularly pronounced gains on unseen tasks.

## Contributions

This work makes three contributions:

- We present **ZimaBlue**, framing video scaling as a practical route toward generalizable World Action Models, and provide empirical evidence that scaling video pre-training significantly improves zero-shot generalization and strengthens performance on challenging manipulation benchmarks.
- We introduce a three-stage training framework comprising egocentric video pre-training, multi-embodiment video-action mid-training, and target-robot post-training, coupled with a unified state-action representation.
- We propose a Slow-Fast WAM architecture that enables 30 Hz closed-loop physical robot control.

## Release Plan

- [ ] Add the technical report and BibTeX entry.
- [ ] Release simulation-post-trained Slow model checkpoints.
- [ ] Release training scripts for simulation post-training.
- [ ] Release evaluation scripts for RoboTwin 2.0, RoboCasa365, and LIBERO-Plus.
