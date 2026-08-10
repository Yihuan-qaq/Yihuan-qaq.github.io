---
layout: post
title: "Why deepfake detection is really a data problem"
date: 2026-07-18
excerpt: "Every detector I have worked on eventually bumps into the same wall: the dataset. Notes from the lab on why we should care about what we test on."
categories: [research]
---

# Why deepfake detection is really a data problem

*Filed under: lab notes · 2026-07-18*

For the past few years I have spent most of my time on speech deepfake
detection. The models keep getting better at fooling us — and the detectors
keep getting better at catching them. But there is a pattern I keep running
into, across every method I have worked on: **the bottleneck is almost never
the model architecture. It is the data.**

## The distribution gap

A detector trained on a clean, studio-recorded spoofing dataset can hit
near-perfect accuracy on its own test split. Put it on a real phone call —
compression, background noise, a different microphone — and performance
collapses. This is the gap we studied in
[When AVSR Meets Video Conferencing](https://arxiv.org/abs/2603.22915):
real-world channels introduce degradation patterns that simply do not exist
in the lab.

## What this means for how we work

1. **Benchmarks matter.** A paper's number is only meaningful relative to the
   test set it is measured on.
2. **Datasets are contributions.** Building *EchoFake* taught me that a
   well-constructed dataset can be as valuable as a clever loss function.
3. **Skepticism is a research skill.** If your detector only works in one
   setting, you have found a feature of the test set, not a property of the
   world.

This is part of why the research lines on this site are organized the way
they are — each direction is really asking the same question from a different
angle: *what can we trust, and under what conditions?*

More notes to come as I keep working through it.
