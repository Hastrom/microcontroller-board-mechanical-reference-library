# Microcontroller board mechanical reference library — public candidate v1.3-rc1

> **🤖 AI-ASSISTED PROJECT — Created with ChatGPT (OpenAI)**
>
> This library was created **with artificial intelligence**: ChatGPT, an AI system developed by OpenAI, was used to reconstruct reference geometry, generate procedural STL/STEP models, and prepare technical documentation. The project was initiated and directed by **Hastrom**, who published it for the maker and engineering community. Third-party engineering source data are credited in [THIRD_PARTY_SOURCES.md](THIRD_PARTY_SOURCES.md).
>
> **Independent project:** neither OpenAI nor Arduino or other hardware manufacturers sponsor, endorse, certify, or guarantee these models. AI-generated geometry is not proof of physical accuracy; verify dimensions on the actual board before fabrication.

**Independent, AI-generated mechanical models for preliminary enclosure layout.**

This is a curated *public candidate* derived from a larger private library. It contains **17 board configurations**, STL meshes and selected STEP mechanical solids. No downloaded original EAGLE/KiCad projects, manufacturer CAD/STEP, images, marks or logos are redistributed.

## IMPORTANT — do not use unverified dimensions for fabrication

These files are **not manufacturer-certified digital twins**. Some board dimensions are published nominal values. Many component bodies, connector protrusions, fastener placements and heights are estimates. Meshes that pass topological checks are *not* verified for physical fit. Test with the **exact revision and physical hardware** before machining or 3D-printing an enclosure or mounting posts. Never infer mains-voltage safety, insulation, thermal or clearance requirements from these files.

### Mechanical evidence levels

- **EAGLE-derived coordinates**: `precision/UNO_R3_DIP/` models are geometrically generated from numerical coordinates in the user's **official UNO R3 Rev3e EAGLE archive**, which explicitly includes a CC BY-SA 4.0 hardware license. Physical heights and manufacturing tolerances remain unverified. The interpretation of overlapping barrel-jack drills as rounded slots is an engineering reconstruction.
- **Third-party KiCad mating footprints**: `precision/{ARDUINO_MICRO,DUE,GIGA_R1_WIFI,LEONARDO,UNO_R4_WIFI}` provides the contour and mating hole reference for companion shields/sockets. **The `ALL_PCB` holes are NOT a verified factory drilling map of the original board.** In particular, the Micro socket NPTH markers should not be assumed to be mounting holes on a real Micro.
- **Approximate assemblies**: `models/` contains original procedural reconstructions. A detailed-looking model is not necessarily accurate. For fasteners, prioritize source-grounded `precision/*_MOUNT_PCB.step` where present and independently check against the physical PCB.

## Navigation

- `models/<BOARD>/` — STL approximations and relevant mating models.
- `precision/<BOARD>/*_V13_MOUNT_PCB.{stl,step}` — PCB contour + mounting/socket references.
- `precision/<BOARD>/*_V13_ALL_PCB.{stl,step}` — additional EAGLE holes or companion footprint connector holes, per origin category.
- `CATALOG.csv` — machine-readable index and evidence status for every delivered model.
- `QA_REPORT.json` — prior geometric validation results; these are NOT physical measurement certificates.
- `PROVENANCE.md` — AI-generation details and exclusions.
- `THIRD_PARTY_SOURCES.md` — required source attribution and transformations.
- `LICENSE` — CC BY-SA 4.0 notice, link to canonical legal text and scope.

STL length unit is millimeters by convention (STL itself does not encode units). PCB thickness is nominally modeled at **1.6 mm**. Many STL assemblies consist of simplified solids; no maker's branding is embedded.

## License and trademark notice

**CC BY-SA 4.0** for material in this candidate to the extent it is controlled by the publishing rightsholder or validly adapted from compatible CC BY-SA 4.0 sources. Observe attribution, indicate changes and license adapted works appropriately. See [LICENSE](LICENSE) and [THIRD_PARTY_SOURCES.md](THIRD_PARTY_SOURCES.md). It does **not** grant patents, trademarks, rights in unrelated third-party works or an IP guarantee.

**Arduino® is a trademark of Arduino S.r.l.**, used here only to identify reference hardware. This project is independently maintained and not affiliated with manufacturers. No logos are supplied.

The models excluded for unclear or different attribution status remain in the private library; see [EXCLUDED_PRIVATE.md](EXCLUDED_PRIVATE.md). A lawyer's review is prudent before promoting the package as cleared of all possible IP claims.
