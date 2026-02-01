# CLAUDE.md - LLM Integration Guide

## Project Overview

**BEACON** (Blueprint Engineering And Component Organizational Nexus) is the CAD and 3D model repository for the O.A.S.I.S. wearable computing platform. It contains printable components, mechanical designs, and assembly references for building O.A.S.I.S. hardware.

---

## Repository Structure

```
beacon/
├── hud/                          # HUD display mounting components
│   ├── HorizonHUD-MK3.17_*.stl   # 3D printable HUD parts
│   └── *.png                     # Reference images
├── wearable_systems/             # Body-worn component housings
│   ├── Jetson_Sling_*.stl        # Jetson carrier/sling parts
│   └── *.png                     # Reference images
├── speakers/                     # Audio component mounts
├── remote_control/               # Remote/controller housings
├── misc_mechanical_components/   # General purpose parts
│   ├── headphone clamp *.stl     # Audio mounting
│   └── mic clamp *.stl           # Microphone mounting
├── CLAUDE.md                     # This file
├── CONTRIBUTING.md               # Contribution guidelines
├── LICENSE                       # GPLv3
└── README.md                     # Project overview
```

---

## File Formats

| Format | Purpose | Software |
|--------|---------|----------|
| `.stl` | 3D printing | Any slicer (Cura, PrusaSlicer, etc.) |
| `.step` | CAD interchange | FreeCAD, Fusion 360, SolidWorks |
| `.f3d` | Fusion 360 native | Autodesk Fusion 360 |
| `.FCStd` | FreeCAD native | FreeCAD |
| `.png` | Reference images | Any image viewer |

---

## Design Guidelines

### Printing Considerations

- **Layer height**: Most parts designed for 0.2mm layer height
- **Infill**: 15-20% typical, 40%+ for structural parts
- **Material**: PLA suitable for most parts, PETG for heat exposure
- **Supports**: Check part orientation; many designed to print without supports

### Naming Convention

```
[Component]-[Version]_[Variant].[ext]

Examples:
- HorizonHUD-MK3.17_v7_p1.stl      # HUD part 1, version 7
- Jetson_Sling_Base_v2.stl         # Sling base, version 2
- headphone clamp bottom v3.stl    # Headphone clamp, version 3
```

---

## Component Categories

### HUD (hud/)

Mounting system for the heads-up display:
- Multi-part assembly for display positioning
- Camera buck variants (large/tight fit)
- Designed for specific display modules

### Wearable Systems (wearable_systems/)

Body-worn component housings:
- Jetson Sling: Multi-part enclosure (Base, Lid, Lens)
- See reference images for assembly

### Audio Components (speakers/, misc_mechanical_components/)

Mounting solutions for audio hardware:
- Headphone clamps
- Microphone mounts
- Speaker housings

---

## Working with This Repository

### For 3D Printing

1. Download the `.stl` files for your component
2. Import into your slicer software
3. Orient for optimal printing (check reference images)
4. Slice with appropriate settings for your printer
5. Print and assemble

### For Design Modifications

1. Use `.step` files for CAD interchange
2. Or native format files (`.f3d`, `.FCStd`) if available
3. Maintain version numbering in filenames
4. Export both native format and `.stl` for printing

### Common Tasks

| Task | Approach |
|------|----------|
| Print a component | Download STL, slice, print |
| Modify a design | Import STEP into CAD, modify, export new version |
| Add new component | Create in CAD, export STL + STEP, add reference image |
| Fix print issues | Adjust orientation, supports, or modify design |

---

## Integration Points

### O.A.S.I.S. Ecosystem

| Component | Relationship |
|-----------|--------------|
| **MIRAGE** | HUD mounts house the display hardware |
| **AURA** | Sensor housings for helmet electronics |
| **SPARK** | Gauntlet/hand component housings |

### S.C.O.P.E. Coordination

- **Meta-repo**: [malcolmhoward/the-oasis-project-meta-repo](https://github.com/malcolmhoward/the-oasis-project-meta-repo)
- **Documentation**: Aggregated in S.C.O.P.E. coordination docs

---

## License

BEACON is licensed under **GPLv3**. See LICENSE for details.

This means you can:
- Use, modify, and distribute the designs
- Must share modifications under the same license
- Must provide attribution
