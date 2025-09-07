# TB6612FNG — Altium Library

>Altium Designer library for the TB6612FNG dual H‑bridge motor driver (Toshiba). This repo includes the schematic symbol, PCB footprint, an Altium Library Package, and 3D models (STEP and SolidWorks). Use it directly in Altium or compile an Integrated Library for distribution.

---

## What’s in this repo
```
TB6612FNG-Altium-Library
├── 3D body/
│   ├── TB6612FNG Module.STEP — generic STEP model for the IC
│   ├── Motor_driver.sldprt — SolidWorks part (source CAD)
│   ├── 8_pin_header.SLDPRT — additional example part (not required for the IC)
│   └── Assem1.SLDASM — SolidWorks assembly (example/demo)
├── TB6612FNG/
│   ├── History/ — Altium auto-generated library history (safe to keep/ignore)
│   ├── TB6612FNG.LibPkg — Altium Library Package (recommended entry point)
│   ├── TB6612FNG.SchLib — schematic symbol library
│   └── TB6612FNG.PcbLib — PCB footprint library
└── LICENSE
```
Notes:
- You can work directly with the `.SchLib/.PcbLib` or use the `.LibPkg` to compile an Integrated Library (`.IntLib`).
- The SolidWorks files are provided as editable 3D sources; Altium consumes the STEP (`.STEP`).

---

## Quick start (Altium Designer)

Option A — Use the Library Package (recommended)
1. Open `TB6612FNG.LibPkg` in Altium.
2. Review the component, symbol-to-footprint links, and parameters.
3. Compile to an Integrated Library:
   - Project/Library panel: Right‑click the library project and select “Compile Integrated Library” (wording may vary by version).
   - The `.IntLib` will be generated in the project outputs folder.
4. Install the `.IntLib`:
   - View > Panels > Components (or Libraries) > Installed > Install From File, choose the `.IntLib`.

Option B — Use raw libraries
1. Add `TB6612FNG.SchLib` and `TB6612FNG.PcbLib` to your project or install them via the Libraries/Components panel.
2. Place > Component, search for TB6612FNG, and place into your schematic/PCB.

---

## 3D model usage

- The footprint can reference “`3D body`/`TB6612FNG Module.STEP`”.
- In the PCB Library editor:
  1. Open `TB6612FNG.PcbLib`, select the footprint.
  2. Place > 3D Body > Generic 3D Model and browse to `TB6612FNG Module.STEP`.
  3. Set orientation/offsets so the STEP aligns with pads and the component origin.
  4. Save the library. In PCB, press 3 to verify the 3D view.

SolidWorks models (`.SLDPRT`/`.SLDASM`) are included as sources; they are not required by Altium. If you modify them, export a new STEP and re‑link it in the footprint.

---

## Pinout and mapping checklist

Typical net names to use/verify (match the datasheet exactly):
- VM, VCC, GND, STBY
- PWMA, PWMB
- AIN1, AIN2, BIN1, BIN2
- AO1, AO2, BO1, BO2

Before manufacturing:
- Confirm symbol pin numbers match footprint pad numbers.
- Confirm package style and pitch (TB6612FNG commonly uses a 24‑pin SSOP/TSSOP‑like package, 0.65 mm pitch — verify against your specific datasheet revision).
- Verify courtyard, solder mask expansion, and paste mask apertures against your fab’s capabilities.
- If you attach a thermal pad or copper pour recommendations, follow the datasheet’s thermal guidelines.

---

## Contributing

- Open an issue for symbol/footprint corrections or enhancements.
- For footprint fixes, reference the exact datasheet figure/page and package variant.
- Pull requests welcome. Please update this `README` if you change file names, footprint models, or the directory structure.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---
