# Data dictionary

CSV encoding is UTF-8. A blank numeric field reads as NA in R. Zero is used only for an inapplicable energy mode or fuel grade, never as a replacement for missing maintenance. Source IDs are semicolon-separated references to source_log.csv.

| Vehicle field | Meaning and unit |
|---|---|
|vehicle_id|Stable identifier V01–V10|
|vehicle_label|Short display label; not a substitute for exact_variant|
|brand|Brand name|
|model|Model family|
|exact_variant|Trim, drive/configuration and distinguishing identity|
|model_year|Model-year label; not purchase or capture date|
|powertrain|BEV, PHEV, EREV, HEV, ICE or MHEV|
|analysis_group|Five analysis groups; ICE and MHEV share Fuel-dominant|
|seat_count|Seats, including driver|
|msrp_cny|List-price scenario, VAT assumed included; CNY|
|market_price_cny|Historical market-reference scenario, CNY; offer conditions matter|
|battery_capacity_kwh|Recorded traction-battery capacity, kWh; NA if unavailable/inapplicable|
|cltc_ev_range_km|Recorded CLTC electric range, km; descriptive, not used to predict electric distance share|
|electricity_kwh_100km|Recorded electric-mode consumption, kWh/100 km; certification-style/provisional|
|fuel_l_100km|Recorded fuel-mode consumption, L/100 km; cycle comparability incomplete|
|fuel_grade|92 or 95 petrol; 0 for BEV|
|maintenance_60000_cny|Raw provisional maintenance estimate for 60,000 km, CNY; eight NA|
|tax_category|NEV or ICE_HEV; exact official catalogue eligibility remains an assumption|
|price_source_ids|References for price/identity evidence|
|energy_source_ids|References for energy evidence|
|maintenance_source_ids|References for raw maintenance evidence, blank if missing|
|identity_status|Historical collector status; not new certification|
|evidence_status|Historical completeness/evidence description|
|missing_reason|Why a raw value is missing|
|notes|Historical conditions and limitations; preserved unchanged|

| Scenario field | Meaning and unit |
|---|---|
|scenario_id / scenario_label|Stable ID and readable household description|
|annual_km|Assumed annual distance, km/year|
|ownership_years|Ownership duration, years|
|home_charging_share|Home share of externally purchased electricity, 0–1|
|phev_electric_share|PHEV electric distance fraction, 0–1|
|erev_electric_share|EREV electric distance fraction, 0–1|
|home_electricity_cny_kwh|Assumed home electricity price, CNY/kWh|
|public_electricity_cny_kwh|Assumed public charging price, CNY/kWh|
|petrol_92_cny_l / petrol_95_cny_l|Historical/assumed energy-price baselines, CNY/L|
|residual_rate|Assumed resale fraction of selected purchase-price basis, 0–1|
|mandatory_fees_cny|Controlled CNY 500 allowance; not a full statutory charge schedule|

| Control field | Meaning |
|---|---|
|control_id|Control version/description identifier|
|maintenance_60000_cny|Uniform baseline CNY 6,000 per 60,000 km|
|maintenance_low_cny / maintenance_high_cny|Independent vehicle allowance bounds, CNY 3,000–9,000 per 60,000 km|
|rationale / source_basis|Explanation of why the control is an assumption|

Derived costs are in CNY. `tco_cny` is depreciation + purchase tax + fees + electricity + fuel + controlled maintenance. `cost_per_km_cny` divides this partial TCO by ownership distance. Ranks are within scenario and price basis. A calculated row is a scenario output, not an additional observed vehicle.
