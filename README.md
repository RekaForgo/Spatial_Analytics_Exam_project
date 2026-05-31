# Spatial Analytics Exam Project

## Spatial Equity of Social Infrastructure Across Neighbourhoods in Aarhus, Denmark

Project work for the **Spatial Analytics** course (Cultural Data Science elective), Aarhus University, 2026. Author: Réka Forgó.

This project measures how evenly walkable access to everyday "third places" (parks, libraries, cafés, fitness centres, community centres) is distributed across Aarhus, using network distances on a routable walking graph, hex-level coverage, LISA cluster detection, and a MAUP robustness check.

### Explore the result

Interactive coverage map (opens in your browser, no download needed): [**https://rekaforgo.github.io/Spatial_Analytics_Exam_project/output/maps/coverage_map.html**](https://rekaforgo.github.io/Spatial_Analytics_Exam_project/output/maps/coverage_map.html){.uri}

Tick categories in the top-right control to see which hexes they cover at 400 m and 800 m.

------------------------------------------------------------------------

### Reproduce the analysis

1.  Clone the repo (this includes `data/processed/`).
2.  Open the project in RStudio and run, in order:
    -   `00_setup.Rmd` — installs packages

    -   `01_get_data.Rmd` — data acquisition / preprocessing

    -   `02_analysis.Rmd` — runs the analysis, regenerates the figures, and rebuilds the interactive map

        `02_analysis.Rmd` reads only from `data/processed/`, so it runs offline. Expensive steps (network build, network distances) are cached to disk and skipped on reruns.

### Repository structure

```         
00_setup.Rmd          package setup
01_get_data.Rmd       data acquisition / preprocessing
02_analysis.Rmd       analysis + interactive map
data/processed/        inputs (from Release; gitignored)
output/figures/        static maps and plots
output/maps/           interactive Leaflet product
```
