# RC Beam Design to ACI 318

A browser calculator for singly reinforced rectangular concrete beams, designed to ACI 318-25, 318-19 or 318-14 in SI units. Enter the section, materials, loads and bars, click Calculate, and it works through flexure, shear, torsion, detailing and serviceability. Every step shows the formula, the numbers used and the code clause, and each check is marked pass or fail.

## What it checks

- Materials and cover: minimum f'c, maximum fy, and cover for the chosen exposure (Table 20.5.1.3.1)
- Minimum depth for deflection (Table 9.3.1.1)
- Flexure: required and minimum steel, neutral axis depth, net tensile strain, φ from Table 21.2.2, the beam strain limit of 9.3.3.1, and φMn ≥ Mu
- Shear: Vc, Vs, the section size limit, minimum shear steel and stirrup spacing
- Torsion: threshold torque, the cross-section limit, closed stirrups for shear plus torsion, longitudinal torsion steel on each face, bar spacing around the perimeter and bar size
- Detailing: bar clear spacing, crack-control spacing and development length

After each calculation, the input panel shows the steel each group of bars needs next to what you provided. The results page ends with a summary table, a cross-section and elevation drawing of the reinforcement, and a bar schedule. You can export the full calculation as a PDF or an Excel workbook.

## How to use it

Open `index.html` in a web browser. Nothing needs installing, and everything runs on your computer, so no data leaves the page. The PDF and Excel libraries are in the `lib` folder.

To put it online, turn on GitHub Pages for this repository (Settings, then Pages, then deploy from the main branch).

## Limits

- One layer of tension bars and no compression steel. Hanger bars are not counted in flexural strength.
- Normal-weight concrete, uncoated bars, no axial force, solid section, nonseismic design.
- Not covered: hollow sections for torsion, lap splices, bar cut-off points, calculated deflections and seismic detailing.
- For ACI 318-25, the Vc, development length and torsion provisions follow the 318-19 form. Check them against the 2025 text before relying on them.

This is a design aid. Results should be checked by a qualified engineer.

## Third-party libraries

- [jsPDF](https://github.com/parallax/jsPDF) and [jsPDF-AutoTable](https://github.com/simonbengtsson/jsPDF-AutoTable), MIT licence
- [SheetJS Community Edition](https://github.com/SheetJS/sheetjs), Apache 2.0 licence
- [DejaVu Sans](https://dejavu-fonts.github.io/) font, subset and embedded for PDF output, free licence

Developed by Aarakshya Kandel
