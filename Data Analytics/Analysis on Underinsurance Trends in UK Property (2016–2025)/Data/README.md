# Data Dictionary

## Overview
This folder contains the raw and processed datasets used in the underinsurance analysis.

## Files

### `/raw/`
- **`ukhousepriceindexmonthlypricestatistics..xlsx`** - Original ONS UK HPI data (Jan 2016 - Aug 2025)
- **`BCIS Raw Data.xlsx`** - BCIS House Rebuilding Cost Index monthly % changes

### `/processed/`
- **`Underinsurance_Data (2).xlsx`** - Final calculated dataset

## Processed Dataset Structure

| Column Name | Description | Unit/Format |
|-------------|-------------|-------------|
| `Date` | Month and year | YYYY-MM-DD |
| `UK_HPI_AvgPrice` | Average UK house price (market value) | £ |
| `BCIS_Index_Change` | Monthly % change in BCIS index | % |
| `Rebuild_Cost_Index` | Cumulative rebuild cost index (Jan 2016 = 100) | Index |
| `Rebuild_Cost` | Estimated rebuild cost | £ |
| `Underinsurance_Gap` | Difference (Rebuild Cost - Market Value) | £ |
| `Underinsurance_Gap_Pct` | Gap as % of rebuild cost | % |

## Data Sources
- **UK HPI**: [ONS](https://www.ons.gov.uk/economy/inflationandpriceindices/datasets/ukhousepriceindexmonthlypricestatistics)
- **BCIS Index**: [BCIS](https://www.bcis.co.uk/insight/index-bcis-house-rebuilding-cost-index/)

## License
Source data retains original licenses (ONS: OGL v3.0). Processed dataset released under MIT License.
