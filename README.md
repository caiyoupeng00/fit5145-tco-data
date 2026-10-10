# China family SUV TCO demonstration data

Review freeze: 10 October 2026. Earlier August observations remain historical and provisional. This directory preserves raw inputs from the existing TCO project. It is a reproducibility snapshot, not a newly verified current price database.

## Files and interpretation

| File | Role |
|---|---|
|[vehicles.csv](vehicles.csv)|Ten exact-variant records, 25 fields; raw missing maintenance values retained|
|[scenarios.csv](scenarios.csv)|Three assumed household profiles; CNY energy prices and residual assumptions|
|[method_controls.csv](method_controls.csv)|Uniform baseline maintenance allowance and sensitivity bounds|
|[source_log.csv](source_log.csv)|Export of the existing workbook's Source Log; old verification labels refer to old collection|
|[Historical_Source_Notes.md](Historical_Source_Notes.md)|Unchanged copy of the earlier project notes; statements are historical, not re-certified here|
|[Data_Dictionary.md](Data_Dictionary.md)|Field meanings, units and missing-value rules|
|[Current_Source_Check.md](Current_Source_Check.md)|Scope of October source retrieval and remaining verification needs|
|[SHA256SUMS.txt](SHA256SUMS.txt)|File hashes for identifying this snapshot|

The calculated results use a separate maintenance assumption of CNY 6,000 per 60,000 km for every vehicle. They do not fill the eight raw missing values with observed estimates. Home charging share weights electricity purchased at home versus public chargers. PHEV/EREV electric distance shares split distance between electric and fuel modes.

The sample has two vehicles in each analysis group. It is selected, heterogeneous and small. It cannot identify population-level or causal powertrain advantages. MSRP and market-reference price are separate scenarios. Dealer-reference prices may require finance, insurance, trade-in, registration or other conditions and are not guaranteed transaction prices. The earlier source register and notes retain the relevant evidence limitations.

The model assumes nominal CNY, a 2026 purchase, 13% VAT included in price, qualifying-NEV tax relief, CNY 500 fixed fees, uniform maintenance and assumed residual rates. Exact eligibility, compatible consumption measurements and vehicle-specific costs still require review. Insurance, finance, parking, repairs, charging losses and time costs are excluded. A common residual rate is a control, not a forecast.

## Download and reproduction

Download the repository with **Code > Download ZIP**, or open a CSV and use **Download raw file**. The three input tables are `vehicles.csv`, `scenarios.csv` and `method_controls.csv`. The source register and notes record provenance and unresolved evidence. `SHA256SUMS.txt` identifies the files in this public snapshot.

The accompanying analysis is submitted separately as a self-contained R Markdown document with identical embedded input tables. The public repository contains the demonstration data and provenance only.

This selected ten-vehicle snapshot is for an educational scenario demonstration. It does not establish actual ownership costs, guaranteed dealer quotes, or a population-level powertrain advantage. Missing raw maintenance observations remain missing; calculation controls are explicit assumptions. No customer records or course source documents are included.

Compiled facts do not grant rights to reproduce entire source websites. Preserve attribution and review source-platform terms when extending or distributing the collection. No licence over third-party material is claimed.
