<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:F8BBD0,50:CE93D8,100:B39DDB&height=180&section=header&text=Retail%20Surveillance%20Pipeline&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Detect%20%C2%B7%20Track%20%C2%B7%20Pose%20%C2%B7%20Behavior%20%C2%B7%20Risk&descAlignY=58&descSize=15)

</div>

## Overview

A multi stage computer vision pipeline built for automated retail surveillance. Rather than a single detection model, it chains detection, tracking, pose estimation, behavior analysis and risk scoring into one flow, so anomalies are flagged with real context instead of a raw bounding box alone.

## Key Features

### Object detection
Identifies people and relevant objects in each frame as the entry point into the pipeline.

### Multi object tracking
Assigns and maintains consistent identities across frames, so behavior can be analyzed per individual over time rather than per frame in isolation.

### Pose estimation
Extracts body pose per tracked individual, feeding structured movement data into the behavior analysis stage.

### Behavior analysis
Interprets pose and movement sequences to recognize behaviors relevant to retail anomaly detection.

### Risk scoring
Combines signals from the earlier stages into a single risk score per individual, which downstream systems can use to trigger alerts.


## Tech Stack

<div align="center">
<img src="https://skillicons.dev/icons?i=opencv,pytorch,python" />
</div>

OpenCV for video and frame handling, PyTorch based detection and pose models, and a custom tracking and scoring layer connecting each stage.

## How It Works

Video frames flow through detection, then tracking assigns persistent IDs, then pose estimation runs per tracked individual. Behavior analysis consumes pose sequences over a rolling window, and risk scoring aggregates behavior signals into a final score per person, exposed through the pipeline's output stream.

## Setup and Run

1. Install dependencies with `pip install -r requirements.txt`.
2. Point `config.yaml` at your video source, either a file path or an RTSP stream.
3. Run `python pipeline.py` to process the stream through all five stages.
4. Review output risk scores and flagged events in the generated log or dashboard.

## Roadmap

- Add configurable behavior rule sets per retail environment
- Optimize the pipeline for real time performance on edge devices
- Add a lightweight dashboard for live monitoring

## Status

> **Status:** This repository was scaffolded from the project description on the author's resume. Source code is being migrated and added here in stages. Reach out using the contact links below if you would like early access to the implementation.

## Let's Connect

<div align="center">

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rawish0922@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/rawishsarfraz)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Rawishs-2882)
[![Phone](https://img.shields.io/badge/Call-+92--332--8747138-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](tel:+923328747138)

</div>

<div align="center">

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:B39DDB,50:CE93D8,100:F8BBD0&height=80&section=footer)

</div>
