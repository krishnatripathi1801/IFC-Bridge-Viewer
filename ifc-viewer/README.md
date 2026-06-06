# OsdagBridge IFC Viewer

Browser-based IFC visualization for bridge models using WebIFC and Three.js.

---

## Overview

This project loads and visualizes IFC bridge models directly inside the browser without requiring desktop BIM software.

The IFC model is parsed using WebIFC, converted into Three.js BufferGeometry, and rendered interactively using WebGL.

The viewer supports navigation, element highlighting, bridge colouring, geometry measurements, and IFC metadata extraction.

---

## Features

- Load IFC bridge models directly in browser
- Parse IFC geometry using WebIFC
- Render bridge model using Three.js
- OrbitControls (Rotate / Pan / Zoom)
- Interactive bridge information panel
- Hover highlighting using Raycasting
- Tooltip display for IFC elements
- Bridge colouring based on IFC element classification
- Bounding box and dimension extraction
- Basic IFC metadata extraction
- Responsive browser rendering

---

## Bridge Colouring

- Main Steel Girders (IFCBEAM) → Steel Blue-Grey  
- Cross Bracing (IFCBUILDINGELEMENTPROXY / Brace) → Light Silver  
- Upper Deck Region → Concrete Tint  
- Hovered Element → Green Highlight  

---

## Tech Stack

- HTML
- CSS
- JavaScript
- Three.js
- WebIFC

---

## Project Structure

plaintext IFC-Bridge-Viewer/ │ └── ifc-viewer/     ├── index.html     ├── D_40_3L_NF_S_SUPER.ifc     └── README.md 

---

## Installation

Clone repository:

bash git clone https://github.com/krishnatripathi1801/IFC-Bridge-Viewer.git 

Open project:

bash cd IFC-Bridge-Viewer/ifc-viewer 

Run local server:

bash http-server . --cors -p 8080 -c-1 

Open:

plaintext http://localhost:8080 

---

## Implementation Flow

1. Load IFC file using fetch()
2. Initialise WebIFC WASM engine
3. Parse IFC geometry
4. Convert geometry into Three.js BufferGeometry
5. Apply IFC placement transformations
6. Render meshes inside Three.js scene
7. Add OrbitControls
8. Apply bridge colouring rules
9. Implement raycasting for interaction
10. Extract metadata and display in UI panel

---

## Current Progress

Completed:
- IFC geometry loading
- Browser-based rendering
- OrbitControls integration
- Raycasting interaction
- Bridge colouring
- UI information panel

Current work:
- Extracting richer metadata directly from IFC properties instead of static values
- Improving element identification and property mapping

---

## Demo

Interactive bridge visualization with:

- Rotation
- Pan
- Zoom
- Hover detection
- Element highlighting
- Metadata panel

---

## Author

Krishna Tripathi  
CSE Core | VIT Bhopal