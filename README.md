# <img width="256" height="256" alt="delta" src="https://github.com/user-attachments/assets/b5e8004a-9ac3-44ef-88a6-7f04d16f6370" />

# HydroDrain – Automated Hydrological Workflow for QGIS

HydroDrain is a QGIS plugin that automatically generates drainage networks from Digital Elevation Models (DEMs). It integrates the official WhiteboxTools Python API and automates the complete hydrological preprocessing workflow within a single interface.

---

## Features

- Select a DEM from an existing QGIS layer or from disk.
- User-defined channelization threshold.
- Automatic depression filling (`FillDepressions`).
- D8 flow accumulation calculation.
- D8 flow direction (pointer) generation.
- Stream extraction.
- Raster stream vectorization.
- Automatic loading of output layers into the QGIS project.
- Built-in help explaining the channelization threshold.

---

## Workflow

HydroDrain currently performs the following workflow:

DEM
↓
Fill Depressions
↓
D8 Flow Accumulation
↓
D8 Pointer
↓
Extract Streams
↓
Raster Streams to Vector

Future versions will extend this workflow with:

- Snap geometries to layer
- Watershed delineation
- Isochrone generation

---

## Requirements

- QGIS 3.44 LTR or later
- Windows (currently tested)

---

## Installation

1. Download or clone this repository.
2. Copy the plugin folder into:

Windows

%APPDATA%/QGIS/QGIS3/profiles/default/python/plugins/

3. Restart QGIS.
4. Enable **HydroDrain** from the Plugin Manager.

---

## Usage

1. Open the HydroDrain panel.
2. Select a DEM.
3. Define the channelization threshold.
4. (Optional) Select output locations.
5. Click **Ejecutar**.
6. Output layers are automatically added to the current QGIS project.

---

## Roadmap

Future versions of HydroDrain will extend the automated workflow with:

- Drainage network generation ✔
- Snap geometries to layer
- Watershed delineation
- Time of concentration analysis
- Isochrone generation

The objective is to provide a complete guided hydrological workflow within a single QGIS plugin.

---

## License

HydroDrain is licensed under the GNU General Public License v2.0 or later (GPL-2.0-or-later).

This project includes WhiteboxTools by Dr. John Lindsay, distributed under the MIT License.

---

## Author

**Roberto Zygmunt Saldaña**

GIS Technician | Environmental Engineer

---

## Acknowledgements

HydroDrain integrates third-party open-source software.

### WhiteboxTools

Hydrological processing is performed using **WhiteboxTools**, developed by **Dr. John Lindsay** (Geomorphometry and Hydrogeomatics Research Group, University of Guelph).

The plugin uses the official WhiteboxTools Python API to execute:

- FillDepressions
- D8FlowAccumulation
- D8Pointer
- ExtractStreams
- RasterStreamsToVector

WhiteboxTools:
https://www.whiteboxgeo.com
https://github.com/jblindsay/whitebox-tools

### Icons

River/Delta icon created by **Freepik** and distributed via **Flaticon**.

---

© 2026 Roberto Zygmunt Saldaña
