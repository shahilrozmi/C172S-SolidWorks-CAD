# C172S SolidWorks CAD Reconstruction

Work-in-progress **SolidWorks CAD reconstruction of a Cessna 172S**, developed as an aerospace/mechanical design portfolio project. The model currently includes substantial fuselage exterior geometry, a modeled propeller and spinner, tailcone rework, and vertical-stabilizer integration, with the rudder and additional detail still in development.

> **Status:** Work in progress. This repository captures the current design state and selected development backups as of September 2026.

## Project Objectives

- Build a detailed external CAD reconstruction of the Cessna 172S using SolidWorks.
- Practice aircraft geometry reconstruction, lofting, surfacing/solid modeling, assembly management, and design repair workflows.
- Produce a clean aircraft assembly suitable for portfolio presentation and later extension into additional components and detail.
- Preserve meaningful intermediate versions so major geometry changes and repair decisions remain traceable.

## Current Progress

### Fuselage and exterior details

Current fuselage work includes:

- front and side windshield geometry
- mirrored center geometry and corrected fuselage width
- main cabin and baggage doors
- external door handles and main-door hinges
- cowling split/seam features
- power-panel access feature on the left side
- oil dipstick/filler access door on the right side
- upper cooling inlets and lower induction intake
- dorsal VHF antenna
- corrected propeller-axis location

### Tailcone

The aft fuselage was substantially reworked using replacement profiles and guide geometry. The repair included:

- replacement forward/mid/rear tail profiles
- loft reconstruction of the aft fuselage
- guide-curve and tangency tuning
- closure of the previous left-side gap
- removal of the superseded fuselage body
- cleanup of dangling sketch relations after geometry replacement

The current fuselage part is `Fuselage_PostTailconeReplacement.SLDPRT`.

### Propeller and spinner

The propeller work is based on the McCauley **1A170E/JHA7660** installation used on the C172S, with a nominal **76 in diameter** and **60 in pitch** reference.

The model includes:

- multiple radial blade stations
- root and tip geometry
- spanwise twist definition
- separate spinner geometry
- propeller/spinner subassembly
- assembly clearance adjustments to eliminate interference

### Vertical stabilizer

The vertical stabilizer has been reconstructed and integrated with the current fuselage geometry. Work included:

- corrected image/reference scaling
- master planform definition
- root, mid, and tip construction planes
- lofted stabilizer geometry
- VBA/API-assisted repair and loft-generation workflows
- rebuild cleanup after the fuselage/tail replacement

### Rudder

Rudder outline and hinge-line work has begun. The rudder remains a **work-in-progress component** and still requires final clearance cuts, separation/detailing, and hinge development.

## Repository Layout

```text
C172S-SolidWorks-CAD/
├── README.md
├── CURRENT_STATE.md
├── FILE_INVENTORY.csv
├── .gitignore
└── Cessna172/
    ├── Assembly.SLDASM
    ├── Fuselage_PostTailconeReplacement.SLDPRT
    ├── C172S_Vertical_Stabilizer.SLDPRT
    ├── Propeller_Spinner_Assembly.SLDASM
    ├── Propeller_Approx_External.SLDPRT
    ├── Spinner.SLDPRT
    ├── Assembly1.SLDASM / Assembly2.SLDASM / Assembly3.SLDASM
    ├── older fuselage and propeller versions
    ├── neutral-format / Pack-and-Go snapshots
    ├── reference spreadsheets
    └── SolidWorks VBA macros used during VS audit/repair
```

The original CAD-file layout has intentionally been preserved rather than aggressively reorganized. SolidWorks assemblies can contain opaque external references, so retaining the historical files in-place minimizes the risk of silently breaking a dependency while the design is still active.

## Current Working Files

The current project state is centered around the following files:

- `Cessna172/Assembly.SLDASM` — latest top-level assembly
- `Cessna172/Fuselage_PostTailconeReplacement.SLDPRT` — current repaired fuselage/tailcone
- `Cessna172/C172S_Vertical_Stabilizer.SLDPRT` — current vertical stabilizer
- `Cessna172/Propeller_Spinner_Assembly.SLDASM` — propeller/spinner subassembly
- `Cessna172/Propeller_Approx_External.SLDPRT` — current external propeller representation used by the subassembly snapshot
- `Cessna172/Spinner.SLDPRT` — spinner part

Older `Assembly1/2/3`, earlier fuselage parts, and the initial propeller part are retained as **development backups**, not as the preferred current design state.

See `FILE_INVENTORY.csv` and `CURRENT_STATE.md` for more detail.

## SolidWorks Automation

The repository retains several `.swp` VBA/API tools developed during the vertical-stabilizer repair process:

- `VS_Audit.swp`
- `VS_Repair.swp`
- `VS_REPAIR2.swp`

These are retained as part of the engineering-development history and as evidence of CAD automation/API work.

## Software and Skills Demonstrated

- SolidWorks part and assembly modeling
- lofts, guide curves, reference planes, cuts, and feature repair
- aircraft geometry reconstruction
- iterative fit/interference correction
- CAD assembly management
- VBA / SolidWorks API automation
- engineering documentation and configuration tracking

## Remaining Work

- finish rudder geometry and clearances
- develop rudder hinge details
- continue empennage cleanup and exterior detailing
- add remaining major aircraft geometry/components as required for the intended model scope
- perform final assembly interference and rebuild checks
- create clean portfolio renders and annotated CAD screenshots
- prepare a stable neutral-format export of the completed assembly

## Notes and Limitations

This is an **educational CAD reconstruction and portfolio project**, not manufacturer CAD data and not a certified production model. Geometry is reconstructed from available references and engineering measurements and should not be treated as authoritative Cessna design data.

The repository intentionally retains several older versions because the project is still under active development and those files provide rollback points for major geometry changes.
