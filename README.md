#  Artemis Lunar Analysis — Apollo Sample Return Prediction

Data analysis of **2,229 lunar rock samples** from six Apollo missions to predict **Artemis program sample return capacity** based on historical trends in module mass, sample weight, and rock type distribution.

*Built as part of Microsoft's "Explore Space with Python" learning path.*

## Key Findings

### Sample Weight by Mission

| Mission | Samples (kg) | Weight Increase |
|---------|-------------|-----------------|
| Apollo 11 | 21.55 | — |
| Apollo 12 | 34.34 | +12.79 kg |
| Apollo 14 | 41.83 | +7.49 kg |
| Apollo 15 | 75.40 | +33.57 kg |
| Apollo 16 | 92.46 | +17.06 kg |
| Apollo 17 | 109.44 | +16.98 kg |
| **Total** | **375.04** | — |

### Rock Type Distribution

| Type | Description |
|------|-------------|
| Soil | Unsieved lunar regolith |
| Basalt | Volcanic rock (Ilmenite subtype) |
| Core | Subsurface drill samples |
| Breccia | Impact-fused regolith fragments |

## Analysis Pipeline

```
NASA Lunar Catalog → 2,229 samples → Weight/Type analysis → Mission comparison
    → Module mass correlation → Artemis capacity prediction
```

1. **Data Loading:** `rocksamples.csv` (6 columns: ID, Mission, Type, Subtype, Weight, Pristine %)
2. **Unit Conversion:** Grams → kilograms (×0.001)
3. **Mission Aggregation:** GroupBy mission, sum weights, compute inter-mission differences
4. **Module Analysis:** Command module and lunar module mass data from NASA NSSDCA
5. **Correlation:** Sample weight vs. module mass trends across missions
6. **Prediction:** Extrapolate Artemis sample return capacity from Orion/Starship specs

## Dataset

| Source | Records | Features |
|--------|---------|----------|
| NASA Lunar Sample Catalog | 2,229 samples | ID, Mission, Type, Subtype, Weight (g), Pristine (%) |

## Tech Stack

- **Language:** Python (Jupyter Notebook)
- **Libraries:** pandas
- **Data Source:** NASA Astromaterials Acquisition and Curation Office, NASA NSSDCA

## Skills Demonstrated

- **Data Analysis:** Aggregation, trend analysis, inter-mission comparisons
- **Predictive Analysis:** Capacity extrapolation from historical trends
- **Domain Knowledge:** Lunar geology, spacecraft module specifications, sample curation
