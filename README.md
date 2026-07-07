# Solar Panel Detection

Development of a spectral index for automated detection and mapping
of photovoltaic solar panels using multispectral satellite imagery.

---

## Background

Existing spectral indices (NDVI, NDWI, NDBI) are designed for
natural land cover. Solar panels present a unique spectral signature
— low reflectance in visible bands, moderate in NIR, and distinct
SWIR absorption — that none of the existing indices isolate cleanly
from spectrally similar surfaces such as water bodies, dark rooftops,
and asphalt roads. This work formulates a dedicated index to exploit
that signature for automated panel delineation.

---

## Current Status

| Stage | Status |
|---|---|
| Literature review of existing built-up and water indices | Complete |
| Spectral signature analysis of solar panels vs confusable classes | Complete |
| Index formulation | Complete |
| Classification accuracy validation | In progress |
| Manuscript preparation | Planned |

---

## Methodology

**Platform:** Google Earth Engine (JavaScript API)  
**Imagery:** Multispectral satellite imagery (Sentinel-2 MSI L2A)  
**Target:** Photovoltaic solar panel surfaces  
**Confusable classes:** Water bodies, dark rooftops, asphalt, shadow

**Approach:**
1. Spectral signature extraction for solar panels and confusable 
   surfaces across diverse geographic and seasonal conditions
2. Band ratio formulation to maximize separability between panels
   and background classes
3. Optimal threshold determination using training samples
4. Validation across varied land surface backgrounds and climatic zones

---

## Repository Structure

```
├── src/
│   ├── spectral_signature_analysis.js  ← GEE: signature extraction
│   ├── index_formulation.js            ← GEE: index computation
│   └── validation.js                   ← GEE: accuracy assessment
├── results/
│   └── separability_analysis.csv
├── figures/
│   └── spectral_signatures.png
└── docs/
    └── index_rationale.md
```

---

## Data

- Sentinel-2 MSI L2A — `COPERNICUS/S2_SR_HARMONIZED`
- Training samples collected via visual interpretation in Google Earth Pro
- No raw imagery stored — see `data/README.md`

---

## Note

This project is ongoing. Code and results will be updated as
validation progresses. A manuscript is planned upon completion
of cross-scene validation.
