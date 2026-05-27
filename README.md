# TB6612FNG — Altium Library

> Altium Designer library for the Toshiba **TB6612FNG** dual H-bridge motor driver. Schematic symbol, PCB footprint, Library Package, and 3D models (STEP + SolidWorks).

[![Altium](https://img.shields.io/badge/Altium-Designer-A5915F?style=flat-square&logo=altiumdesigner&logoColor=white)](https://www.altium.com/)
[![Hardware Library](https://img.shields.io/badge/type-hardware%20library-1F2937?style=flat-square)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

---

## What's in this repo

```
TB6612FNG-Altium-Library/
├── 3D body/
│   ├── TB6612FNG Module.STEP           # Generic STEP model for the IC
│   ├── Motor_driver.sldprt             # SolidWorks part (source CAD)
│   ├── 8_pin_header.SLDPRT             # Example header part (not required for the IC)
│   └── Assem1.SLDASM                   # SolidWorks assembly demo
├── TB6612FNG/
│   ├── History/                        # Altium auto-generated library history
│   ├── TB6612FNG.LibPkg                # Library Package (recommended entry point)
│   ├── TB6612FNG.SchLib                # Schematic symbol library
│   └── TB6612FNG.PcbLib                # PCB footprint library
└── LICENSE
```

Altium consumes the `.STEP` for 3D rendering; the SolidWorks files are editable sources.

## Quick start (Altium Designer)

**A — Use the Library Package (recommended)**

1. Open `TB6612FNG.LibPkg` in Altium
2. Review component, symbol-to-footprint links, parameters
3. Right-click the library project → **Compile Integrated Library** to generate `.IntLib`
4. View → Panels → Components → Installed → Install From File → select the `.IntLib`

**B — Raw libraries**

Add `TB6612FNG.SchLib` and `TB6612FNG.PcbLib` directly to your project, or install via the Components panel.

## License

[MIT](LICENSE) — see [anjanamb.github.io](https://anjanamb.github.io/) for more projects.
