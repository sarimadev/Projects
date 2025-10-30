# Data Source Documentation and Verification
## Dataset Overview
This dataset uses monthly data from January 2016 to August 2025 (116 months). The market/insured value series is obtained from the UK House Price Index (UK HPI) – Average Price, published by the Office for National Statistics (ONS). The rebuild cost series is derived from the Building Cost Information Service (BCIS) House Rebuilding Cost Index, using monthly percentage change data.
Both sources are industry-recognised: ONS as the UK's official statistics agency, and BCIS as a specialist cost data provider for the built environment and insurance sectors. The BCIS House Rebuilding Cost Index specifically measures residential reinstatement costs for insurance purposes, making it the appropriate index for underinsurance analysis (as distinct from the General Building Cost Index or Tender Price Index).
## Methodology
### Data Sources and Treatment
The UK HPI uses hedonic regression methodology and transaction data across all residential property types. The BCIS House Rebuilding Cost Index reflects changes in costs of labour, materials and overheads for residential reinstatement, originally referenced to a base period of 1985 = 100. For clarity in this visualisation, the rebuild cost index has been re-based to January 2016 = 100.
### Calculation Process
### Step 1: Calculate Rebuild Cost Index
The index is built cumulatively from the base month (January 2016 = 100):
```
Rebuild_Cost_Index(t) = Rebuild_Cost_Index(t-1) × (1 + BCIS_Index_Change(t) / 100)

**Example:**
- January 2016: Index = 100 (base period)
- February 2016: If BCIS % change = +0.25, then Index = 100 × (1 + 0.0025) = 100.25
- March 2016: If BCIS % change = +0.32, then Index = 100.25 × (1 + 0.0032) = 100.57
```
This creates a smooth monthly index growth line directly tied to BCIS changes.

### Step 2: Derive Rebuild Cost (£)

The UK HPI values are then multiplied by the index ratio:
```
Rebuild_Cost(£) = UK_HPI_AvgPrice(£) × (Rebuild_Cost_Index / 100)

```
This "rebases" the market value to account for the rising cost of rebuilding.

## Assumptions and Limitations
### Core Assumptions

**Market/insured value** is assumed equivalent to the average house price series from UK HPI
**Rebuild cost** is derived from indexed values calculated using BCIS monthly percentage increases
**January 2016 equivalence:** For modelling purposes, we assume January 2016 market values approximate rebuild costs (i.e., both start at the same baseline). The analysis focuses on the divergence rate between indices rather than absolute underinsurance at any point in time

### Underinsurance Metrics
The underinsurance gap is calculated as:
```
Gap (£) = Rebuild Cost (£) – Market/Insured Value (£)
Gap (%) = Gap (£) ÷ Rebuild Cost (£) × 100
```
### Limitations
While both series provide robust industry-level indicators, individual property circumstances may vary. Actual rebuild costs depend on property-specific factors including construction type, location, and specification.
## Data Integrity Verification
### Completeness Check
✓ Both series span 116 months (January 2016 to August 2025) with no missing data points
✓ BCIS monthly percentage change data aligns with publication schedules
✓ UK HPI monthly average price data verified as complete across the time series
### Methodology Changes
The ONS introduced an improved imputation method for August 2025 HPI data. We assessed whether this created a discontinuity in the series: no outliers or breaks were detected, and the series remains consistent for trend analysis.
## Data Sources

UK House Price Index: Office for National Statistics
https://www.ons.gov.uk/economy/inflationandpriceindices/datasets/ukhousepriceindexmonthlypricestatistics
BCIS House Rebuilding Cost Index: Building Cost Information Service
https://www.bcis.co.uk/insight/index-bcis-house-rebuilding-cost-index/
