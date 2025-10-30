# Underinsurance Trends in UK Property (2016–2025)

[![Tableau](https://img.shields.io/badge/Tableau-Dashboard-E97627?logo=tableau)]([YOUR_TABLEAU_LINK](https://public.tableau.com/views/UnderinsuranceStory/UnderinsuranceStory?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link))


## Overview

A data visualization project revealing how UK construction costs have outpaced property values, creating a growing underinsurance gap for property owners. This project aims to support property underinsurace awareness.

**Key Finding:** Rebuild costs accelerated significantly faster than market values after 2021, reaching an average gap of 6% by August 2025.

## Data Sources

- **[UK House Price Index](https://www.ons.gov.uk/economy/inflationandpriceindices/datasets/ukhousepriceindexmonthlypricestatistics)** (ONS) — Monthly property prices
- **[BCIS House Rebuilding Cost Index](https://www.bcis.co.uk/insight/index-bcis-house-rebuilding-cost-index/)** — Rebuild cost index percentage changes

**Period:** January 2016 – August 2025 (116 months)

## Methodology

This analysis uses compound indexing to track how rebuild costs (BCIS) diverge from market values (UK HPI), rebased to January 2016 = 100.

**Full methodology:** See [METHODOLOGY.md](Methodology.md)

## Project Structure
```
├── data/
│   ├── raw/          # Original ONS and BCIS data
│   └── processed/    # Cleaned dataset
├── visualizations/   # Tableau workbook and charts
├── METHODOLOGY.md
└── README.md
```

## Outputs

- 🔗 **[Interactive Tableau Dashboard](https://public.tableau.com/views/UnderinsuranceStory/UnderinsuranceStory?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**
- 📊 Processed dataset available in `/data/processed/`

## Tools

Excel • Tableau Public • GitHub

## Use Cases

Relevant for Property Owners, Insurance Professionals, Risk Analysts, and Data Enthusiasts exploring property underinsurance trends.

## License

MIT License — see [LICENSE](LICENSE)  
Source data: ONS ([OGL v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/)), BCIS (fair dealing)

## Author

**Sarima Iyayi**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?logo=linkedin)](www.linkedin.com/in/sarima-iyayi-81a1b6139) [![Email](https://img.shields.io/badge/Email-Contact-D14836?logo=gmail)](mailto:sarimafyne54@gmail.com)

---

⭐ **Star this repo if you found it useful!**
