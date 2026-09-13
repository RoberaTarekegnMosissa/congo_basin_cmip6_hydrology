# Diagnosing Hydrological Cycle Biases in CMIP6 Models over the Congo Basin

Code and documentation for the MSc thesis ***“Diagnosing Hydrological Cycle Biases in State-of-the-Art CMIP6 Climate Models over the Congo Basin.”*** The project evaluates how CMIP6 climate models represent precipitation, evaporation, and atmospheric moisture transport across the Congo Basin during the historical reference period 1985–2014.

> **Project status:** **Active research.** The repository structure, methods, and results will evolve as the thesis progresses.

## Research overview

The Congo Basin is a major component of the global climate system, yet its hydrological cycle remains difficult to observe and simulate. Climate-model evaluation is complicated by sparse ground observations, differences among satellite and reanalysis products, and uncertainty in land–atmosphere processes.

This project evaluates CMIP6 simulations against multiple observation-based and reanalysis datasets. Using several reference products avoids treating any single product as error-free and helps characterize observational uncertainty.

## Objectives

1. Evaluate CMIP6 precipitation and evaporation over the Congo Basin using observation-based and reanalysis products.
2. Quantify spatial, monthly, and seasonal biases.
3. Assess variability across CMIP models.
4. Investigate precipitation–evaporation coupling and atmospheric moisture convergence.
5. Evaluate consistency with the atmospheric water-balance framework.

## Analysis workflow

1. Inventory and quality-check the input datasets.
2. Standardize coordinates, calendars, missing values, and units.
3. Aggregate daily data to monthly values.
4. Crop, conservatively regrid to 1°, and mask the Congo Basin.
5. Calculate monthly, seasonal, and annual climatologies for 1985–2014.
6. Evaluate biases, ensemble spread, and reference-product uncertainty.
7. Diagnose moisture convergence and produce validated figures and tables.

## Variables and units

| Quantity | Typical CMIP6 variable | Native unit | Analysis unit |
|---|:---:|:---:|:---:|
| Precipitation | `pr` | kg m⁻² s⁻¹ | mm day⁻¹ |
| Surface latent heat flux | `hfls` | W m⁻² | Evaporation in mm day⁻¹ |
| Specific humidity | `hus` | kg kg⁻¹ | kg kg⁻¹ |
| Zonal wind | `ua` | m s⁻¹ | m s⁻¹ |
| Meridional wind | `va` | m s⁻¹ | m s⁻¹ |

Evaporation is derived from surface latent heat flux using an appropriate latent heat of vaporization and a documented sign convention.

## Repository structure

```text
congo-basin-cmip6-hydrology/
├── config/
├── data/
│   ├── raw/
│   ├── interim/
│   └── processed/
├── docs/
├── hpc/
│   ├── cdo/
│   └── slurm/
├── notebooks/
├── results/
│   ├── figures/
│   └── tables/
├── scripts/
├── src/
├── tests/
├── .gitignore
├── environment.yml
└── README.md
```

## Author

### Robera Tarekegn Mosissa
MSc Interuniversity Master of Water Resources Engineering (IUPWARE)
KU Leuven and Vrije Universiteit Brussel, Belgium

## Supervision:

- Prof. Wim Thiery — Vrije Universiteit Brussel

- Margo Cabuy(PhD Candidate) — daily supervisor


