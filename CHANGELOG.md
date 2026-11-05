# Changelog

## v2026.11.05 - 2026-11-05

- Improved automatic sheet placement for Revit 2019 and 2020: edited crop bounds now determine view size, spacing, and the 3 cm bottom gap.
- Corrected title block blank-area bottom detection and migrated existing local placement profiles when loaded.
- Aligned each view in a row independently, preserved configured row spacing, and aligned the left edges of equal-size row patterns such as 2×2.
- Compared crop-based row arrangements against the calibrated title block area; if a trial viewport overflows the top edge, the add-in tries another arrangement or title block.
- Kept placed sheets when viewport annotations extend beyond the detected area, with a warning in the placement report.

## v2026.11.04 - 2026-11-04

- Added separate Revit 2019 and 2020 builds in one installer.
- Added the 「永豐工坊」 ribbon, Chinese panel names, and feature icons.
- Added view crop, view naming, and title block detection for automatic sheet placement.
- Improved structural beam workflows and updated the installation guide.

## v1.0.0 - 2026-05-28

Initial public release.

- Added Yfarch BIM Pro Tools for Revit 2019 installer package.
- Added public download and installation instructions.
- Added Revit 2019 support notes.
