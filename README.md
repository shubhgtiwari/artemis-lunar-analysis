# Artemis Lunar Sample Analysis

NASA mission planning analysis - determining optimal sample collection targets for the Artemis program.

## The Problem

NASA is planning to return humans to the Moon through the Artemis program. With limited capacity for bringing samples back to Earth, astronauts need guidance on what to collect.

The question: Given what we already have from the six Apollo missions (383 kg of lunar material), what should Artemis prioritize to maximize scientific value and fill gaps in our collection?

## Data Source

NASA Lunar Sample and Photo Catalog (curated by the Astromaterials Acquisition and Curation Office)

Coverage: Apollo 11, 12, 14, 15, 16, and 17 missions

## Approach

1. **Data Cleaning**: Converted weights from mixed grams/kilograms to unified metric (kg)
2. **EDA**: Grouped samples by mission and rock type (Basalt, Breccia, Crustal, Soil, Core)
3. **Strategic Planning**:
   - Calculated total weight of existing samples
   - Estimated Artemis mission capacity
   - Developed recommendation algorithm for underrepresented rock types

## Results

- Analyzed 383 kg of existing lunar samples across six Apollo missions
- Calculated Artemis should aim to collect approximately 71 kg of new material
- Generated specific targets:
  - **12 Basalt rocks**
  - **34 Breccia rocks**
  - **20 Crustal rocks**
- Created data-driven collection priority list for mission planning

## Sample Distribution by Mission

| Mission | Sample Weight |
|---------|---------------|
| Apollo 11 | 21.6 kg |
| Apollo 12 | 34.3 kg |
| Apollo 14 | 42.3 kg |
| Apollo 15 | 77.3 kg |
| Apollo 16 | 95.7 kg |
| Apollo 17 | 110.5 kg |

## Tech Stack

- Python
- Pandas
- Matplotlib

## Key Learnings

There is something surreal about writing code that could theoretically influence what astronauts pick up on the Moon. Data science is not just about algorithms - it is about turning data into actionable recommendations. Even simple aggregation and percentage calculations become meaningful when they answer the right question.

## Installation

```bash
git clone https://github.com/ShubhGTiwari/artemis-lunar-analysis.git
cd artemis-lunar-analysis
pip install -r requirements.txt
```

## Author

**Shubham Tiwari** - Data Scientist & ML Engineer
