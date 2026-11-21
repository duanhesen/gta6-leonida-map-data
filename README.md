# GTA 6 Leonida Map Marker Dataset

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24412576.svg)](https://doi.org/10.5281/zenodo.24412576)

798 map markers for the six regions of Leonida in Grand Theft Auto VI, published as CSV and
JSON under CC BY 4.0.

The canonical source is the dataset page: **https://gta6maps.io/gta-6/map-data** — that page
states the current update date, the current counts and the citation format. This repository is
a mirror of the same rows so the data can be read, diffed and cited without scraping.

## Files

| File | What it is |
|---|---|
| `data/gta-6-markers.csv` | 798 rows, one per marker, nine columns |
| `data/gta-6-markers.json` | the same rows plus region names, category counts and the field list |

## Fields

| Field | Example | Notes |
|---|---|---|
| `id` | `lm-l2872` | stable identifier for one pin |
| `name` | `Ocean Beach` | place name as shown on the map |
| `category` | `activities` | `landmarks`, `businesses` or `activities` |
| `region` | `vice-city` | one of the six regions below |
| `x`, `y` | `0.6875`, `0.4898` | position as published by the map, normalised 0–1 |
| `status` | `sourced` | see *What `status` means* |

`x` and `y` are the values the map itself uses to place a pin. They are not geographic
coordinates and they are not tied to a particular image size; treat them as relative
position on the map surface.

## Coverage

| Region | Markers |
|---|---:|
| Vice City | 499 |
| Port Gellhorn | 157 |
| Leonida Keys | 60 |
| Mount Kalaga | 32 |
| Ambrosia | 30 |
| Grassrivers | 20 |
| **Total** | **798** |

By category: 486 landmarks, 198 businesses, 114 activities.

## What `status` means

Every row in this release is `sourced`: the pin is supported by published material, and the
name and region are the ones that material uses. A pin only becomes `verified` when there is
something a player can check in game behind it.

The map keeps a public verification log at https://gta6maps.io/gta-6/verification that lists
each pin's evidence state, so "we think this is right" and "this is confirmed" never look the
same. This CSV is deliberately not padded with guesses to reach a round number.

## License

CC BY 4.0. You may copy, adapt and redistribute the data, including commercially, if you
credit GTA6Maps and link to https://gta6maps.io/gta-6/map-data.

## Citation

> GTA6Maps, "GTA 6 Leonida Map Marker Dataset," 798 markers, updated November 20, 2026,
> https://gta6maps.io/gta-6/map-data, CC BY 4.0.

If you quote region or category counts, include the update date — the counts change as new
footage is mapped and pins are verified. The `updated` field inside the JSON names the version
of the data in this repository.

## Related

- Interactive map, all six regions: https://gta6maps.io/gta-6
- Printable A3/A4 map of the same pins: https://gta6maps.io/gta-6/printable-map
- How pins move from sourced to verified: https://gta6maps.io/gta-6/verification

## Archived copy with a DOI

The same data is archived on Zenodo and has a DOI, so it can be cited formally in articles,
papers and tooling docs:

- DOI: [10.5281/zenodo.24412576](https://doi.org/10.5281/zenodo.24412576)
- Record: https://zenodo.org/records/24412576
