# A3 Phase 2 — Vehicle Freeze Sources

> Capture date: 2026-08-27. This register freezes the intended comparison variants; it does not claim that all TCO inputs are final. Blank cells remain genuine evidence gaps.

## New and refreshed sources

|ID|Vehicle / purpose|Sources|Authority and use boundary|
|---|---|---|---|
|S27|Current Xiaomi YU7 2026 Rear-Wheel Drive Standard|[Autohome configuration](https://www.autohome.com.cn/config/spec/77835.html); [Xiaomi 2025 manufacturer release](https://www.mi.com/global/discover/article?id=5174)|Current trim values are commercial C1 evidence. Xiaomi's accessible manufacturer release describes the superseded 2025 specification, so it is context only, not the 2026 value source.|
|S28|BYD Tang L DM 2025 DM-i 215KM 2WD LiDAR Flagship|[BYD model page](https://www.byd.com/cn/dynasty-home/models/tang/tang-l-dm); [Dongchedi exact parameters](https://www.dongchedi.com/auto/params-carIds-244350)|Manufacturer A2 confirms the family; exact trim, price and dual-mode energy are C1 cross-checks.|
|S29|Lynk & Co 08 EM-P 2026 160 Long-Range Max|[Lynk & Co launch release](https://www.lynkco.com.cn/brand/news/newslist/2025news/0924); [Autohome configuration](https://www.autohome.com.cn/config/spec/73863.html)|Manufacturer A2 confirms model family, limited price and battery families; exact trim MSRP/energy are C1 cross-checks.|
|S30|2026 New Li L6 Standard|[Li Auto launch](https://ir.lixiang.com/news-releases/news-release-details/li-auto-inc-launches-new-li-l6-versatile-all-wheel-drive-suv); [Li Auto Q2 2026 results](https://ir.lixiang.com/news-releases/news-release-details/li-auto-inc-announces-unaudited-second-quarter-2026-financial)|Company A2 evidence confirms RMB249,800 and the 51 kWh battery. Exact certified energy values remain missing.|
|S31|AITO M6 EREV Max+ Long-Range|[HIMA configuration](https://hima.auto/wenjie/m6/configuration/); [Autohome parameters](https://www.autohome.com.cn/config/spec/76430.html)|Manufacturer A2 confirms identity, price, battery and range; consumption is a C1 cross-check.|
|S32|Honda CR-V e:HEV 2026 Smart Edition|[Dongfeng Honda configuration](https://www.dongfeng-honda.com/cr-v/HEV/js/configuration.html)|Manufacturer A2 source for version, MSRP and WLTC fuel consumption.|
|S33|Volkswagen Tiguan L Pro 2026 Pro 380TSI 2WD R-Line Navigation|[SAIC Volkswagen model page](https://www.svw-volkswagen.com/tiguanlpro/); [Dongchedi parameters](https://www.dongchedi.com/auto/params-carIds-254339)|Manufacturer A2 confirms model entry; exact price, WLTC fuel use and market lead are C1 evidence.|
|S34|Cadillac XT5 2026 28T 2WD Metropolitan|[Cadillac current model list](https://www.cadillac.com.cn/wap/allVehicle.html); [Dongchedi parameters](https://www.dongchedi.com/auto/params-carIds-252233-252234-252235-252236); [Autohome launch/price article](https://www.autohome.com.cn/news/202509/1309216.html)|Manufacturer A2 confirms the current XT5 family; exact 48V trim, fuel use and limited price are commercial cross-checks and must remain condition-labelled.|
|S35|Xiaomi YU7 Beijing retail observation|[Xiaomi Beijing Xiangyun Town listing](https://dealer.yiche.com/100264447/price_detail/189371.html)|C2 dealer/platform observation: RMB233,500 on 2026-08-28, equal to MSRP. Record as a Beijing market observation, not a discount claim.|
|S36|2026 Li L6 Beijing retail observation|[Li Auto Beijing Tongzhou listing](https://dealer.yiche.com/100266682/price_detail/189220.html)|C2 retail observation: RMB249,800 on 2026-08-28, equal to MSRP. Optional benefits are non-cash and excluded from purchase price.|
|S37|2026 Li L6 dual-mode energy parameters|[PCauto exact configuration](https://price.pcauto.com.cn/m140562/config.html); [ZOL exact configuration](https://detail.zol.com.cn/2173/2172567/param.shtml)|Two independent C1 commercial parameter databases agree on 22.3 kWh/100km; PCauto and a Beijing exact-trim dealer page report B-state fuel use of 7.1 L/100km. Keep provisional until a manufacturer/MIIT parameter table is archived.|
|S38|Honda CR-V e:HEV Beijing market observation|[Autohome Beijing dealer listing](https://dealer.autohome.com.cn/65295/spec_74891.html)|C2 condition-bound dealer observation: RMB159,900 for the 2026 e:HEV Smart Edition. A separate dealer page states insurance/finance/trade-in/bundle conditions, so use only as the lower market-price scenario, not a clean cash quote.|

Existing source IDs S09, S11, S14–S18 and S21–S26 remain defined in the master workbook and `Data/A3_MVP/Source_Notes.md`.

## What changed in this freeze

- Replaced the old Xiaomi YU7 2025 launch row with the current 2026 Rear-Wheel Drive Standard target. The two versions must not be mixed.
- Frozen exact Tang L DM, 08 EM-P, M6, CR-V e:HEV, Tiguan L Pro and XT5 trims.
- Replaced the final-target L6 identity with the 2026 Ultra; the separate three-car MVP deliberately retains the 2025 L6 so the completed vertical slice remains reproducible.
- Kept maintenance blank for eight vehicles rather than applying a fabricated common amount.
- Corrected the final-target L6 trim label to `2026 Ultra`, and cross-checked its 22.3 kWh/100km electricity use and 7.1 L/100km B-state fuel use across commercial parameter sources.
- Added timestamped Beijing price observations for YU7, L6 and CR-V. The CR-V quote is explicitly condition-bound.
- Added `method_controls.csv`: a uniform 6,000 CNY/60,000 km maintenance control with a 3,000-9,000 CNY sensitivity range. It is an analytical assumption and does not fill the raw maintenance evidence cells.

## Remaining evidence priorities

1. Replace the 2026 L6 commercial energy cross-check with a manufacturer/MIIT archive when available.
2. Auditable 60,000-km scheduled-maintenance totals for V02–V06 and V08–V10.
3. Replace the condition-bound CR-V quote and other volatile platform prices with clean cash observations.
4. Model- or segment-specific 3-year/5-year residual evidence; until then, residual value stays a scenario sensitivity rather than a forecast.
