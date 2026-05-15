# 36Cl Terrestrial Age Calculator

A browser-based calculator for the terrestrial age of stony meteorites from 36Cl measurements in metal extracts.

**Live app:** https://csadaka2.github.io/terr-age-meteorite-app/

## What it does

Two-step workflow, all in a single self-contained HTML page (no install, no server):

1. **Saturation activity (A_sat)** — from sample Fe/Ni composition and the Leya & Masarik (2009) production-rate table embedded in the app. Pick a pre-atmospheric radius R and depth range, paste a `Sample;Fe;Ni` CSV.
2. **Terrestrial age** — from the measured 36Cl/35Cl ratio, spike mass, and metal mass. Computes A_meas via the spike, then `t = (T½/ln 2) · ln((A_sat − A_T)/(A_meas − A_T))` with full 1σ propagation.

Outputs a table of ages ± σ in ka and a downloadable CSV.

## Based on

- [`Leya&Mas2009_model`](https://github.com/csadaka2/meteorites/tree/main/Leya%26Mas2009_model) — A_sat from elemental production rates
- [`chlore_terr_ages`](https://github.com/csadaka2/meteorites/tree/main/chlore_terr_ages) — age + uncertainty propagation

Constants and formulas mirror those repos (`T½ = 301,000 yr`, `σT½ = 1,500 yr`, `M(36Cl) = 35.976 g/mol`, `C_spike = 6.00 mg/g`, `A_T = 0.001 dpm/kg`).

## Running locally

Open `index.html` in any modern browser. That's it.
