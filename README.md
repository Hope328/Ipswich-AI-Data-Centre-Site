# Ipswich AI Data Centre Site Suitability - GIS Project

**Independent ArcGIS Pro portfolio project - Ipswich, Queensland**  
**Current status:** Map 1 complete; suitability analysis in progress

[![ArcGIS Pro](https://img.shields.io/badge/ArcGIS%20Pro-Spatial%20Analysis-2f6f67)](#spatial-method)
[![Project status](https://img.shields.io/badge/Status-Map%201%20complete-d9b56d)](#current-progress)
[![Portfolio site](https://img.shields.io/badge/Project%20page-GitHub%20Pages-46637f)](https://hope328.github.io/ipswich-ai-data-centre-gis/)

## Current output

![Ipswich study area and infrastructure map](docs/assets/ipswich-study-area-map.jpg)

**Map 1 - Study Area and Infrastructure.** This map establishes the Ipswich study area and shows the spatial relationship between major transport, electricity and water infrastructure used in the preliminary site assessment.

## Project question

**Where are the most suitable areas for potential AI data-centre development in Ipswich when infrastructure access, environmental constraints and land-development practicality are considered together?**

This project demonstrates an early-stage, multi-criteria GIS screening workflow. It is designed to identify areas that warrant further investigation - not to nominate a construction site or replace engineering, planning, environmental or commercial due diligence.

## Decision context

Large data-centre developments depend on reliable electricity access, transport connectivity and developable land. At the same time, early screening should identify conflicts with flood risk, waterways, protected vegetation, ecological values, existing urban interfaces and difficult terrain.

The project brings these considerations into one transparent spatial model so that the reasons behind each suitability class can be explained and tested.

## Screening framework

| Theme | Example criterion | GIS treatment | Intended effect |
|---|---|---|---|
| Infrastructure | Major-road access | Euclidean distance / buffers | Prefer more accessible areas |
| Infrastructure | Electricity network context | Proximity screening | Prefer areas nearer relevant infrastructure |
| Environment | Waterways and water bodies | Constraint buffers | Avoid direct conflict and allow setbacks |
| Natural hazard | Flood-risk areas | Exclusion or penalty | Reduce exposure during initial screening |
| Environment | Protected areas and regulated vegetation | Exclusion or penalty | Reduce ecological and approval risk |
| Land use | Urban and planning context | Reclassification | Identify compatible or conflicting areas |
| Terrain | Slope derived from elevation data | Raster reclassification | Prefer flatter, more developable land |

The final weights and thresholds will be documented rather than hidden inside the model. See [`methodology/CRITERIA_AND_SCORING.md`](methodology/CRITERIA_AND_SCORING.md).

## Spatial method

1. Define the Ipswich study area and use an appropriate projected coordinate system.
2. Assemble authoritative Queensland and Ipswich spatial datasets.
3. Clip layers to the study extent and standardise projection, geometry and metadata.
4. Separate **hard constraints** from **weighted suitability factors**.
5. Generate proximity surfaces or buffers for infrastructure and environmental features.
6. Reclassify each criterion to a common suitability scale.
7. Combine weighted factors and erase hard-constraint areas.
8. Inspect candidate areas against aerial imagery, planning context and obvious data limitations.
9. Produce a clear map layout and a concise candidate-area summary.

## Current progress

- [x] Project question and decision context defined
- [x] Initial criteria framework drafted
- [x] Authoritative source inventory prepared
- [x] Ipswich study area and core infrastructure layers mapped
- [x] **Map 1: Study Area and Infrastructure exported**
- [ ] Environmental and hazard constraint layers processed
- [ ] Suitability factors scored and weighted
- [ ] Sensitivity test completed
- [ ] Composite suitability map exported
- [ ] Candidate-area findings and limitations written

## Planned deliverables

- [x] **Figure 1:** Study area and infrastructure context
- [ ] **Figure 2:** Environmental and hazard constraints
- [ ] **Figure 3:** Composite suitability result
- [ ] **Table 1:** Criteria, thresholds, scores and weights
- [ ] **Table 2:** Shortlisted candidate-area comparison
- [ ] **A3 layout:** Final suitability map with title, legend, scale, sources, method note and limitations

## Repository structure

```text
.
├── README.md
├── docs/
│   └── assets/
│       └── ipswich-study-area-map.jpg
└── methodology/
    ├── CRITERIA_AND_SCORING.md
    ├── DATA_SOURCES.md
    ├── OUTPUT_CHECKLIST.md
    └── weighting-template.csv
```

## Limitations

This is a **strategic screening exercise**. It does not assess confirmed electricity capacity or connection cost, land ownership and acquisition, geotechnical conditions, detailed flood hydraulics, biodiversity field surveys, cultural heritage, water demand, telecommunications redundancy, noise, community impacts, development approvals or project economics.

A high GIS suitability score therefore means **"worthy of further investigation"**, not **"approved or feasible."**

## About the analyst

I am a Brisbane-based early-career GIS professional with Queensland Government operational-mapping experience, a Bachelor of Management in Land Resource Management and a Master of Agribusiness from The University of Queensland. My interests include geospatial consulting, environmental and infrastructure screening, spatial data quality and clear cartographic communication.

- GitHub: [@Hope328](https://github.com/Hope328)
- Email: [yuhong.he@student.uq.edu.au](mailto:yuhong.he@student.uq.edu.au)
