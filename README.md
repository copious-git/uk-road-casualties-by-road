# UK motorcyclist and cyclist casualties by road (STATS19, 2025)

Motorcyclist and pedal cyclist casualties on every **numbered road** in Great Britain, derived from the
Department for Transport's STATS19 road casualty open data, 2025 final release.

Nobody else publishes UK casualty counts broken down per numbered road and per police force area, so this
repository exists to make that derivation open, checkable and reusable.

## What's here

| File | Contents |
|---|---|
| `data/dangerous-roads-2025.json` | 2025 final release: GB totals plus the top 30 roads by KSI for motorcyclists and for cyclists |
| `data/dangerous-roads-2024.json` | Same structure for 2024, for comparison |

Each road record carries `killed`, `serious`, `slight`, `ksi` and `total`.
KSI means killed or seriously injured.

## Headline figures, 2025 (Great Britain)

| Road user | Killed | Seriously injured | Slightly injured |
|---|---|---|---|
| Motorcyclists | 386 | 5,616 | 9,445 |
| Cyclists | 79 | 4,224 | 11,739 |

Worst road for motorcyclist KSI: **A38** (48). Worst for cyclist KSI: **A4** (36).

## Method

Computed from the DfT casualty and collision files for 2025 (the final release, published 30 July 2026).
Casualties are assigned to the **first road of the collision**. Roads without a number, including
unclassified and C roads, are excluded. Severity is **as reported by the police and not adjusted**.

That last point matters when comparing with DfT's published totals. DfT applies a severity adjustment for
changes in police reporting systems since 2016, so its published figures are 386 / 5,710 / 9,351 where the
unadjusted counts here are 386 / 5,616 / 9,445. The death count is identical and both reconcile to 15,447
casualties in total.

Cyclist casualties are the most under-reported of any road user group, because cyclists have no obligation
to report a collision to the police. Treat these counts as a floor.

## Licence and attribution

Source data: Department for Transport, published under the
[Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
Contains public sector information licensed under the Open Government Licence v3.0.

This derived dataset is released under the same terms.

## Source

- DfT road accident and casualty statistics: https://www.gov.uk/government/collections/road-accidents-and-safety-statistics
- Interactive tables and per-force-area breakdown: https://bikers.co.uk/data/dangerous-roads
- All 44 police force areas: https://bikers.co.uk/data/dangerous-roads/regions
- Cyclist-specific analysis: https://bikers.co.uk/data/dangerous-roads/cyclists
