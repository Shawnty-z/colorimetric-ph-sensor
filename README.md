# Colorimetric pH Sensor

This repository contains the final report for my colorimetric pH sensor project. The goal was to reduce the subjectivity of manual pH test-strip reading using a low-cost, portable device.

## What I built
A Raspberry Pi + camera system in a controlled enclosure to standardize illumination and capture strip images, then estimate pH from the reaction-pad color.

## Technical approach (high level)
- Color represented in CIE L*a*b* space
- Dominant pad color extracted (clustering/segmentation)
- pH estimated via calibration-based interpolation against reference colors

## Key outcome
The full design, implementation, and evaluation are documented in the report.

## Document
- `Colorimetric_Sensor_Final_Report.pdf` — Final project report (includes system design, pipeline details, and results)

Author: Xuanye (Caleb) Zeng
