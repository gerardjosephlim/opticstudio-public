# OpticStudio Column CAD — Interactive Optical Column Design & Ray Tracing Simulator

OpticStudio Column CAD is a high-precision, web-based optical engineering computer-aided design (CAD) tool and sequential ray tracing simulator for designing, analyzing, and budgeting multi-element commercial optical columns (e.g. Epi-Fluorescence microscopes, collimators, objective-tube lens imaging relays).

---

## Live Web Application

Access the interactive web simulator directly at:
**[https://gerardjosephlim.github.io/opticstudio-public/](https://gerardjosephlim.github.io/opticstudio-public/)**

---

## Key Features

- **Interactive 3D Component CAD & Optomechanical Inspector**: Inspect physical dimensions ($Ø\text{ Outer}$, $Ø\text{ Clear Aperture}$, edge/center thicknesses, focal lengths) and surface coating callouts (dichroic interference sheen, broadband AR, optical cement) with full 3D orbital navigation and 90° cutaway cross-section inspection.
- **Dual-Arm & Multi-Branch Ray Tracing**: Complete round-trip epi-fluorescence simulation tracing both the excitation arm ($530\text{ nm}$ green LED reflected $90^\circ$ into specimen) and emission arm (Stokes-shifted $585\text{ nm}$ amber fluorescence transmitted through dichroic substrate to tube lens and camera), with interactive beam path filtering.
- **Sequential 3D Vector Ray Tracing**: Exact Snell's law refraction ($n' \vec{S}' = n \vec{S} + \Gamma \vec{n}$) with high-order Newton-Raphson polynomial even-asphere solving.
- **Paraxial ABCD Matrix Engine**: Instantaneous calculation of system and component cardinal points: Effective Focal Length ($EFL$), Back Focal Length ($BFL$), System Numerical Aperture ($NA$), Airy disk radius, and RMS spot radius.
- **Commercial Component Grounding**: Authentic optical prescriptions and physical dimensions for standard commercial components:
  - Achromatic Doublets (`AC254-060-A`, `AC254-080-A`, `AC254-100-A`)
  - Precision Aspheric Condenser (`ACL25416U-A`)
  - High-Power LED Source (`M530D3`)
  - Dichroic Beamsplitter (`DMLP490`)
  - 20X Microscope Objective (`DL20X-PA`)
  - Pellicle Beamsplitter (`BP145B1`)
- **Discrete 90° Step Component Rotation**: Full 4-quadrant rotation ($0^\circ, 90^\circ, 180^\circ, 270^\circ$) across all components via Inspector segmented pill buttons, on-canvas HUD, selection gizmo, and keyboard shortcuts (`R`, `Shift+R`, `F`).
- **Finite Beamsplitter Plate Refraction**: Exact $3.0\text{ mm}$ UV Fused Silica plate modeling with internal refraction ($28.93^\circ$), $-0.94\text{ mm}$ lateral beam displacement, and directional $90^\circ$ split branches.
- **Live Optical Diagnostics**: Real-time image plane Spot Diagram with Airy disk diffraction limit and Transverse Ray Fan aberration curves ($EY$ vs $PY$).
- **Decoupled Evaluation Plane**: CMOS camera measurement plane isolated from the optical train with live defocus analysis.
- **Configuration Persistence**: Save custom presets to browser storage, and export/import complete column layouts via JSON.

---

## Running Locally

To run this application locally on your computer:

```bash
# 1. Start a local HTTP server in this directory
python3 -m http.server 8088

# 2. Open in your web browser
open http://localhost:8088/
```
