# Model verification status

Numerical geometry can be generated to high computational precision, but **physical accuracy is unverified**. In particular, the 0.015 mm mesh discretization setting used for v1.3 mechanical parts is not a claim of 0.015 mm accuracy to the hardware.

### Classes

- **Design-file grounded (EAGLE)**: official Uno R3 Rev3e numerical PCB outline/hole/footprint coordinates. Physical component heights estimated; slots reconstructed; no fabrication certification.
- **Mating footprint grounded (KiCad)**: outline, shield/socket hole centers, footprint conductor/connector mating positions. NOT manufacturer assembly drilling or 3D component placement. Arduino Micro NPTH markers particularly not guaranteed to exist on physical PCB.
- **Estimated general layout**: other assembled envelopes, pins, headers and board outlines based on nominal dimensions and procedural estimates. Use for visual clearance study only.

### Mechanical checks

`QA_REPORT.json` contains inherited v1.3 topology/mesh QA for every selected STL, and STEP import checks when available. All published STL entries in this candidate are expected watertight from the recorded checks. These checks do not compare geometry to a manufactured board.

### Usage warning

Verify physical board revision and measure USB protrusion, connector stand-off, hole diameter/center, PCB thickness, solder underside clearances, and maximum component height. Do not infer mains insulation, creep/clearance, thermal safety, or fabrication tolerances from these data.
