# B.E.A.C.O.N. - Blueprint Engineering And Component Organizational Nexus (CAD Files)

<img src="https://www.oasisproject.net/assets/BEACON_Logo_bg.png" alt="BEACON Logo" width="350" align="right">

## Overview

B.E.A.C.O.N. (Blueprint Engineering And Component Organizational Nexus) is the CAD and mechanical design repository for the O.A.S.I.S. ecosystem. It provides 3D-printable enclosures, mounts, and structural components that house the electronics from other O.A.S.I.S. components.

BEACON contains STL files ready for slicing and printing, along with reference images showing print orientation and assembly. The designs are organized by functional category: HUD mounting, wearable systems, speakers, remote control, and miscellaneous mechanical parts.

## Hardware

BEACON provides designs for housing the following O.A.S.I.S. hardware:

| Assembly | Version | Parts | Houses |
|----------|---------|-------|--------|
| HorizonHUD Mounting | MK3.17 v7 | 3 main parts + 2 camera buck variants | MIRAGE display and cameras |
| Jetson Sling | v2 | Base, Lid, Lens | Jetson compute platform (DAWN) |
| Wearable Stereo Speakers | v6 | Base + 2 top variants (blank, SI) | Audio output hardware |
| Controller Housing (Pad5) | v13 | Bottom, Side | Remote control interface |
| Audio Tie-Downs | v3 | Headphone clamps, mic clamps, screwdown mount | Helmet audio hardware (AURA) |

## Software Dependencies

### For 3D Printing

- Any slicer: [Cura](https://ultimaker.com/software/ultimaker-cura/), [PrusaSlicer](https://www.prusa3d.com/prusaslicer/), or equivalent
- STL file viewer (most slicers include this)

### For Design Modifications

- [FreeCAD](https://www.freecadweb.org/) (free, open-source)
- [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/) (proprietary)
- Any CAD software supporting STEP import/export

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/The-OASIS-Project/beacon.git
   ```
2. Open STL files in your slicer software
3. Apply print settings (see Usage section)
4. Slice and print

No software installation beyond a slicer is required for printing. For design modifications, install one of the CAD tools listed above.

## Usage

### Print Settings

| Setting | Standard Parts | Structural Parts |
|---------|---------------|-----------------|
| Layer Height | 0.2mm | 0.2mm |
| Infill | 15-20% | 40%+ |
| Material | PLA or PETG | PLA or PETG |
| Supports | Minimal by design | Check orientation |

- **PLA**: Suitable for most parts
- **PETG**: Recommended for heat-exposed components (near electronics)
- Reference images (PNG files alongside STLs) show recommended print orientation

### Repository Structure

```
beacon/
├── hud/                           # HUD display mounting (5 STLs)
├── wearable_systems/              # Body-worn housings (3 STLs)
├── speakers/                      # Audio mounts (3 STLs)
├── remote_control/                # Controller housing (2 STLs)
├── misc_mechanical_components/    # General parts (5 STLs)
└── docs/
    ├── guide.md                   # This file
    └── parts-catalog.md           # Visual catalog with reference images
```

### File Naming Convention

```
[Component]-[Version]_[Variant].[ext]

Examples:
  HorizonHUD-MK3.17_v7_p1.stl          (multi-part assembly, part 1)
  Jetson_Sling_Base_v2.stl              (single component)
  wearable_stereo_speakers_top_si_v6.stl (variant: Stark Industries)
```

### Design Standards

When contributing new designs:
- STL meshes must be manifold (watertight)
- Use reasonable polygon count (not excessively dense)
- Scale in millimeters
- Z-up orientation
- Include a reference PNG image showing the printed part

## Troubleshooting

| Issue | Possible Cause | Solution |
|-------|---------------|----------|
| STL won't slice | Non-manifold geometry | Run mesh repair in slicer or Meshmixer |
| Parts don't fit together | Scale mismatch | Verify slicer is set to millimeters, not inches |
| Warping during print | Bed adhesion or material | Use brim/raft; ensure bed is level and heated |
| Camera buck too tight/loose | Manufacturing tolerance | Try the alternate fitment variant (large vs tight) |
| Part breaks under load | Insufficient infill | Reprint with 40%+ infill for structural parts |
| Overhangs sagging | Missing supports | Check reference image for correct print orientation |

## Related Components

- [M.I.R.A.G.E.](https://www.oasisproject.net/components/mirage/) - HorizonHUD mounting system houses the MIRAGE display and cameras
- [D.A.W.N.](https://www.oasisproject.net/components/dawn/) - Jetson Sling enclosure houses the compute platform running DAWN
- [A.U.R.A.](https://www.oasisproject.net/components/aura/) - Audio tie-downs and clamps mount helmet electronics managed by AURA
- [S.P.A.R.K.](https://www.oasisproject.net/components/spark/) - Mechanical components for gauntlet housings

See [parts-catalog.md](parts-catalog.md) for a visual catalog of all components.
