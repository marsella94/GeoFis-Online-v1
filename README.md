# GeoFIS
### Geotechnical Fuzzy Inference System for Rock Slope Stability Assessment
### Sistema de Inferencia Difusa para Evaluación de Estabilidad de Taludes Rocosos

**GeoFIS** is a standalone web application implementing a Mamdani fuzzy inference system for the geotechnical assessment of rock slope stability. The system integrates 11 fuzzy modules and 15 input variables derived from rock mass classification criteria (RMR), enabling a comprehensive evaluation of stability conditions without requiring specialized software installation.

---

## Features

- 11 chained Mamdani FIS modules covering rock mass quality, discontinuity geometry and contact quality, surface physical condition, slope geometry, and block hazard
- 15 input variables with real-unit entry and automatic normalization based on RMR classification criteria
- Bilingual interface (Spanish / English)
- Light and dark display modes
- Interactive PDF report generation with project data
- Project save and load in `.etd` format
- Fully standalone — single HTML file, no dependencies, no installation required

---

## System Architecture

| Module | FIS | Inputs |
|--------|-----|--------|
| Rock Mass Quality | FIS-1 | RQD, UCS |
| Structural Definition | FIS-2 | Spacing, Persistence |
| Geometric Condition D | FIS-3 | FIS-2, Orientation |
| Contact D | FIS-4 | Aperture, Roughness |
| Contact Quality D | FIS-5 | FIS-4, Infill |
| Surface Condition | FIS-6 | Weathering, Moisture |
| Physical Condition | FIS-7 | FIS-5, FIS-6 |
| Geometric Condition T | FIS-8 | Inclination, Height |
| Block Hazard | FIS-9 | Large, Medium, Small block |
| Geometric Stability | FIS-10 | FIS-3, FIS-8, FIS-9 |
| Global Stability | FIS-11 | FIS-1, FIS-7, FIS-10 |

---

## Usage

Download `GeoFIS.html` and open it in any modern web browser. No internet connection is required after download.

---

## Technical Details

- Fuzzy engine: Mamdani, implemented in pure JavaScript
- And method: minimum
- Aggregation: maximum
- Defuzzification: centroid (N = 200)
- Membership functions: gaussmf, sigmf, dsigmf, gbellmf, pimf, smf, zmf

---

## Authors

This tool was developed by the following researchers:

1. M.I.T. Marsella Gissel Rodríguez Servín
2. Dr. José Eleazar Arreygue Rocha
3. Dr. Mariana Lobato Báez
4. Dr. Juan Carlos López Pimentel
5. Ing. José Manuel Díaz Barriga García
6. Dr. Luis Alberto Morales Rosales

**Institution:** Universidad Michoacana de San Nicolás de Hidalgo, Morelia, Michoacán, Mexico

**Program:** Doctorado en Ingeniería Civil

**Laboratory:** Laboratorio de Modelación Computacional para Infraestructura Inteligente (LAMCII)

---

## License

Academic use only. All rights reserved. Copyright 2025 LAMCII-UMSNH.

Reproduction or redistribution without authorization is prohibited.
