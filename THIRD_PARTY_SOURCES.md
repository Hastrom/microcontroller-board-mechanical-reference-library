# Source attribution and changes — CC BY-SA compliance

This is an independent **transformed numerical-geometry** library. The URLs below identify third-party engineering sources used to reconstruct meshes; **original source CAD/PCB files are not redistributed**. Licensors retain their rights in those sources. Generating output using AI does NOT erase upstream licensing obligations.

## 1. Official Arduino UNO R3 DIP Rev3e (specific version)

- Original project/creator: Arduino / Arduino S.r.l. (and contributors identified in the design files).
- Source delivered to model creator: `A000066-cad-files.zip`, containing `UNO-TH_Rev3e.brd` and `License.txt`.
- Official CAD source: https://docs.arduino.cc/hardware/uno-rev3 (downloads / CAD section).
- The original archive's `License.txt` states: **hardware Creative Commons Attribution-ShareAlike 4.0 International**.
- Modifications/transformation: numerical board outline, mounting/drill coordinates and component footprint locations were interpreted and converted to procedural **STL/STEP mechanical volumes** by ChatGPT; component body heights are approximated; overlapping barrel-jack drilling features were modeled as rounded slots. No original `.brd`/`.sch`/logo is included.
- Files covered: `precision/UNO_R3_DIP/**`, `models/UNO_R3_DIP/*` (except omitted unsealed assembly).
- Adapted mechanical geometry distributed under CC BY-SA 4.0; see [LICENSE](LICENSE).

## 2. Independent KiCad Arduino compatible footprints

- Original library: **Arduino KiCad Library**.
- Author/copyright: **Nicholas Parks Young / Alarm-Siren (2017–2023 and subsequent contributors as applicable)**.
- Upstream: https://github.com/Alarm-Siren/arduino-kicad-library
- License: **Creative Commons Attribution-ShareAlike 4.0 International**, with an exception for electronic designs using library data, documented in the upstream README and LICENSE.
- Upstream source paths: `footprints/arduino-library.pretty/Arduino_Micro_Socket.kicad_mod`, `Arduino_Due_Shield.kicad_mod`, `Arduino_Giga_R1_WiFi_Shield.kicad_mod`, `Arduino_Leonardo_Shield.kicad_mod`, `Arduino_Uno_R4_WiFi_Shield.kicad_mod`.
- Modifications/transformation: transformed numerical shield/socket mating contours, mounting/connector coordinates, and nominal thickness into procedural mechanical STL/STEP solids. Added representative components of **unverified geometry**. These are **mating footprint references**, not physical component coordinates from manufacturer board CAD. No `.kicad_mod`, logos, upstream documents or third-party images copied here.
- Files covered: `precision/{ARDUINO_MICRO,DUE,GIGA_R1_WIFI,LEONARDO,UNO_R4_WIFI}/**` and `models/` files with `KICAD_REF` in their path.
- Conservatively treated as CC BY-SA 4.0 adapted geometry, with license notice and attribution preserved even where the library's exception may apply.

## 3. Other board families: numeric specification references

- Remaining `models/` files were **generated procedurally by ChatGPT (OpenAI)** from broadly available numerical nominal dimensions and common 2.54-mm mechanical pitches, not imported from outside mesh files or maker drawings. Many component bodies and locations are estimates. These original portions are offered under CC BY-SA 4.0 only to the extent the publisher has the relevant rights.
- General manufacturer hardware information: https://docs.arduino.cc/ ; https://www.arduino.cc/en/trademark .
- Manufacturer descriptions are factual reference links, not a grant of their branding, marks, illustrations, patents or files.

## Licensing / distribution limits

- License text: https://creativecommons.org/licenses/by-sa/4.0/legalcode
- Attribution, changes and ShareAlike are required for adapted materials where applicable.
- Manufacturer names identify compatible/reference boards only; no endorsement or affiliation.
- NO third-party downloaded EAGLE, KiCad, STEP, PDF, product photos, screenshots, logos or source hardware drawings are included in this release.
- Other source-derived models were removed from this candidate pending a separate clearance; see EXCLUDED_PRIVATE.md.
