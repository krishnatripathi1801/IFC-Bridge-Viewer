# OsdagBridge IFC Viewer

Browser-based IFC visualization for bridge models using WebIFC and Three.js.

## Overview
This project loads and visualizes IFC bridge models directly in the browser without desktop BIM software.

The IFC model is parsed using WebIFC and converted into Three.js BufferGeometry for rendering and interaction.

## Features
- Load IFC files in browser
- Parse IFC geometry using WebIFC
- Render bridge model using Three.js
- OrbitControls (Rotate / Pan / Zoom)
- Interactive UI information panel
- Hover highlighting using Raycasting
- Element tooltip display
- Custom bridge colouring:
  - Main steel girders → Steel blue-grey
  - Cross bracing → Light silver
  - Upper deck region → Concrete tint
- Bounding box and dimension extraction
- Basic IFC metadata extraction

## Tech Stack
- HTML
- CSS
- JavaScript
- Three.js
- WebIFC

## Project Structure

project/
│
├── index.html
├── D_40_3L_NF_S_SUPER.ifc
├── README.md

## Installation

Clone repository:

git clone <repo-url>

Open folder:

cd project

Run:

http-server . --cors -p 8080 -c-1

Open:

http://localhost:8080

## Implementation

1. Load IFC file using fetch()
2. Initialise WebIFC WASM engine
3. Parse geometry from IFC
4. Convert geometry into Three.js BufferGeometry
5. Apply transformations
6. Render meshes in Three.js scene
7. Add OrbitControls
8. Apply bridge colouring rules
9. Add raycasting interaction
10. Extract metadata and display in UI panel

## Colour Rules

- IFCBEAM → Main bridge girders
- IFCBUILDINGELEMENTPROXY / Brace → Cross bracing
- Upper region → Concrete colour
- Hover → Green highlight

## Current Work

Working on extracting richer metadata directly from IFC properties instead of using static values.

## Demo

Bridge model rendered in browser with interactive navigation and hover detection.