# Colorimetric pH Sensor

A low-cost, portable colorimetric pH sensor that automates pH test-strip reading using controlled illumination and a Raspberry Pi imaging pipeline.

## What this project does
Manual interpretation of pH strips is subjective, while lab equipment is often too expensive for field use. This project builds a proof-of-concept device that:
- Captures a test strip image under consistent white LED lighting
- Extracts the reaction-pad color and maps it to a pH value
- Displays the estimated pH on an LCD screen

## System overview
- Hardware: Raspberry Pi + Pi Camera, controlled white LED illumination, enclosure to reduce ambient-light variation, LCD output.
- Algorithm:
  1) Represent strip color in **CIE L\*a\*b\*** color space
  2) Use **K-means** to isolate the dominant reaction-pad color (reduce noise/background influence)
  3) Estimate pH via interpolation against **pre-calibrated reference colors** (color-to-pH mapping)

## Results
Across a range of test solutions, the device achieved:
- Mean Absolute Error (MAE): ~0.28 pH
- Mean standard deviation: ~0.057
- Correlation coefficient: R² ~ 0.985

## Repository contents
- Colorimetric_Sensor_Final_Report.pdf — full final report (design, theory, implementation, evaluation)

## Author
Xuanye (Caleb) Zeng
