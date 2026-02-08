# BEACON

**Blueprint Engineering And Component Organizational Nexus** - CAD files and 3D printable components for the O.A.S.I.S. wearable computing platform.

## Overview

BEACON contains 3D models, mechanical designs, and printable components for building O.A.S.I.S. hardware. Files are provided in standard formats compatible with common 3D printing and CAD software.

## Repository Structure

```
beacon/
├── hud/                          # HUD display mounting components
├── wearable_systems/             # Body-worn component housings
├── speakers/                     # Audio component mounts
├── remote_control/               # Remote/controller housings
└── misc_mechanical_components/   # General purpose parts
```

## File Formats

| Format | Purpose | Software |
|--------|---------|----------|
| `.stl` | 3D printing | Any slicer (Cura, PrusaSlicer, etc.) |
| `.step` | CAD interchange | FreeCAD, Fusion 360, SolidWorks |
| `.png` | Reference images | Any image viewer |

## Quick Start

### 3D Printing

1. Download the `.stl` files for your component
2. Import into your slicer software
3. Check reference images (`.png`) for orientation
4. Slice with appropriate settings:
   - Layer height: 0.2mm typical
   - Infill: 15-20% (40%+ for structural parts)
   - Material: PLA or PETG
5. Print and assemble

### Design Modifications

1. Import `.step` files into your CAD software
2. Make modifications
3. Export new `.stl` for printing
4. Maintain version numbering in filenames

## Components

### HUD (hud/)

HorizonHUD mounting system - multi-part assembly for display positioning.

### Wearable Systems (wearable_systems/)

Body-worn housings including Jetson Sling enclosure.

### Audio (speakers/, misc_mechanical_components/)

Mounting solutions for headphones, microphones, and speakers.

## Related Projects

BEACON is part of the [O.A.S.I.S. Project](https://github.com/The-OASIS-Project):

| Component | Purpose |
|-----------|---------|
| [MIRAGE](https://github.com/The-OASIS-Project/mirage) | HUD display system |
| [DAWN](https://github.com/The-OASIS-Project/dawn) | AI voice assistant |
| [SPARK](https://github.com/The-OASIS-Project/spark) | Hand/gauntlet firmware |
| [AURA](https://github.com/The-OASIS-Project/aura) | Helmet sensor firmware |
| [GENESIS](https://github.com/The-OASIS-Project/genesis) | Python utilities |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or any later version.

See [LICENSE](LICENSE) for full details.
