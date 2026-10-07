# Web AR Model Viewer

A browser-based augmented reality experience built with Unity WebGL that places interactive 3D content on tracked image targets using a mobile device's camera.

**[Launch the live demo](https://tunc0x.github.io/web-ar-model-viewer/)** · **[View the full demo excerpt](https://tuncay-portfolio.pages.dev/)**

## Demo

[![Web AR Model Viewer demo](docs/web-ar-demo.gif)](https://tuncay-portfolio.pages.dev/)

> This repository contains the deployable WebGL build.  
> The underlying Unity project and source code are kept private.

## Overview

Web AR Model Viewer explores marker-based augmented reality directly in the browser, without requiring a native mobile application.

The application requests access to the device camera, tracks predefined image targets and uses the tracking result to align Unity-rendered content with the physical scene.

## Features

- Browser-based AR through Unity WebGL
- Image-target tracking
- Mobile camera access
- Support for front and rear camera handling
- Multiple image targets
- Unity content rendered over the live camera feed
- Runs directly from a hosted web page without a native app installation

## How it works

```text
Device camera
      │
      ▼
Browser camera stream
      │
      ▼
Image tracking / computer vision
      │
      ▼
Target pose
      │
      ▼
Unity WebGL runtime
      │
      ▼
AR content aligned with the tracked image
```

The browser layer handles camera access and tracking integration while the Unity WebGL application renders and manages the interactive 3D experience.

## Technology

- Unity
- C#
- WebGL
- JavaScript
- OpenCV.js
- Web APIs for camera access
- GitHub Pages

## Repository structure

This repository contains the exported application rather than the Unity authoring project.

```text
web-ar-model-viewer/
├── Build/              # Compiled Unity WebGL application
├── StreamingAssets/    # Runtime assets
├── TemplateData/       # Unity WebGL page assets
├── targets/            # Image-tracking targets
├── arcamera.js         # Browser camera integration
├── itracker.js         # Image-tracking runtime
├── opencv.js           # OpenCV.js runtime
└── index.html          # WebGL entry point
```

## Source availability

The original Unity project is kept private. This public repository contains the exported WebGL build used for the hosted demonstration.

A recorded excerpt of the application is available on my portfolio:

**[View project demo](https://tuncay-portfolio.pages.dev/)**

## Running the build

Because browser camera access requires a secure context, run the application through HTTPS or a local web server rather than opening `index.html` directly.

The hosted version is available here:

**https://tunc0x.github.io/web-ar-model-viewer/**
