---
title: "CS-499 Capstone Final Project"
layout: splash
permalink: /
date: 2021-04-12T15:08:00-05:00
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /images/splash-header.jpg
  actions:
    - label: "Get Started"
      url: "https://crakindev.github.io/project_summary/"
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "This project encompasses an ambitious full-stack application development utilizing a third-party game API supplied by Bungie Studios to aggregate player data, store in a MongoDB database and display in a front-end web dashboard. Additional connectivity is also available via a Discord bot developed with DiscordJS."
intro: 
  - excerpt: 'Project Aspects'
feature_row:
  - image_path: /images/code-review-th.jpg
    alt: "Application Code Review"
    title: "Application Code Review"
    excerpt: 'Code review of all aspects of existing application boilerplate plus best practices. Code review video included.'
    url: "https://crakindev.github.io/code_review/"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row2:
  - image_path: /images/unsplash-gallery-image-1-th.jpg
    alt: "Project Enhancement One"
    title: "Project Enhancement One"
    excerpt: "Discord bot development via DiscordJS Node module"
    url: "https://crakindev.github.io/portfolio/enhancement-1/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
    title: "Project Enhancement Two"
    excerpt: "Application API server development with Express"
    url: "https://crakindev.github.io/portfolio/enhancement-2/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /images/unsplash-gallery-image-3-th.jpg
    title: "Project Enhancement Three"
    excerpt: "Application API server completion and React-based web dashboard."
    url: "https://crakindev.github.io/portfolio/enhancement-3/"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row3:
  - image_path: /images/unsplash-gallery-image-2-th.jpg
    alt: "Professional Self-Assessment"
    title: "Professional Self-Assessment"
    excerpt: 'My educational journey, CS program reflection, and professional experiences.'
    url: "https://crakindev.github.io/professional_assessment/"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="feature_row" type = "left" %}

{% include feature_row id="feature_row2" %}

{% include feature_row id="feature_row3" type="right" %}
