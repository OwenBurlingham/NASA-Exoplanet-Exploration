# Exoplanet Classification and Habitability Analysis

Exploratory analysis of 6,000+ confirmed exoplanets from NASA's Exoplanet Archive, examining planet-star relationships and assessing habitability potential.

## Overview

This project analyzes patterns in exoplanet discoveries, addressing how observational selection bias affects our understanding of planetary systems. Custom classification systems categorize planets and stars, while PCA reveals physical constraints on planetary characteristics.

## Key Findings

- **Planet-star mass correlation:** Larger planets systematically orbit larger stars
- **Physical constraints:** Strict correlations between mass, radius, and orbital parameters create hard boundaries in parameter space
- **Habitability estimate:** ~0.07% of observed planets meet Earth-similarity criteria (likely underestimate due to detection bias)
- **Tidal circularization:** Short-period planets have circular orbits; long-period planets retain high eccentricity

## Dataset

- **Source:** [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)
- **Size:** 6,147 confirmed planets (deduplicated from 40,000 rows)
- **Key variables:** Planet mass/radius, orbital period, eccentricity, star temperature/mass/metallicity
- **Limitations:** 52% missing mass data, 25% missing radius data; strong selection bias favoring large planets

## Methodology

1. **Data cleaning:** Intelligent duplicate removal (keeping most complete records)
2. **Classification:** Custom systems for planet types (Earth-like, Hot Jupiter, etc.) and star types (by temperature)
3. **Exploratory analysis:** Histograms and bivariate plots revealing distributions and relationships
4. **PCA:** Dimensionality reduction on orbital/physical parameters
5. **Habitability scoring:** Earth-similarity criteria (mass, radius, orbital period, star type)

## Key Insights

### Selection Bias
- Hot Jupiters dominate dataset (~90% transit detections) despite representing ~1% of actual planets
- Red Dwarfs severely underrepresented (5.9% vs ~75% of real stars)
- Small rocky planets systematically underdetected

### Physical Relationships
- **Mass-Radius:** Two distinct regimes (rocky vs gaseous) with composition-driven constraints
- **Period-Eccentricity:** Tidal forces circularize short-period orbits
- **Planet-Star Mass:** Weak positive correlation consistent with protoplanetary disk models

### Habitability
- 1 potentially habitable planet identified: Kepler-22b
- Extrapolated estimate: ~228 million habitable planets in Milky Way, ~456 quintillion in observable universe
- True frequency likely higher due to undersampling of small rocky planets

## Files

- `Final_Project_435_V2.ipynb` - Full analysis with code and interpretation
- `README.md` - This file

**Note:** The dataset (`planets.csv`) is not included due to size. Download directly from [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/).

## Technologies

Python, pandas, plotnine, scikit-learn, matplotlib

## How to Run

```bash
# Install dependencies
pip install pandas plotnine scikit-learn matplotlib numpy

# Download the dataset
# 1. Go to https://exoplanetarchive.ipac.caltech.edu/
# 2. Navigate to the Planetary Systems table
# 3. Download as CSV and save as 'planets.csv' in the project directory

# Run notebook
jupyter notebook Final_Project_435_V2.ipynb
```

## Data Source

Dataset downloaded from NASA Exoplanet Archive (February 2026 snapshot) containing 6,147 confirmed exoplanets with measurements of orbital, physical, and stellar properties.

## Author

Owen Burlingham
