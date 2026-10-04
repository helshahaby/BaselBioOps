# BioFlow Guardian

Hack am Rhein Hackathon

Hossam Elshahaby

Date: 3 October 2026

## Links

- App: https://river-flow-finder.lovable.app
- Pitch video: https://youtu.be/rueqBCvdUXA

## Project Summary

BioFlow Guardian is a manufacturing risk and decision dashboard for Basel-area biopharma operations. It converts real public signals from the Rhine, Basel traffic, and weather into operational actions for refrigerated critical materials.

The system recommends whether a material should be:

- **Buffered** in controlled storage
- **Expedited** toward the next production step
- **Rerouted** around logistics disruption
- **Quarantined** for quality review when handling conditions are uncertain

## Challenge

Challenge 4: From a Rhine Signal to Action - Manufacturing in the BioValley

Basel is a major life-sciences manufacturing region. Critical biopharma materials depend on reliable logistics and controlled temperature handling. A disruption outside the factory, such as abnormal Rhine conditions, heavy traffic, or hot weather, can affect production before operators notice the full risk.

## Problem

Factory teams often see external disruption data as separate information streams:

- Rhine water levels and navigation conditions
- Basel road traffic counts
- Weather observations and heat risk
- Cold-chain handling rules

The missing layer is the operational translation: what should the factory do with a critical 2-8°C material right now?

## Solution

BioFlow Guardian connects open data to a manufacturing decision engine.

The prototype follows this pipeline:

Open Data -> Disturbance Detection -> Risk Score -> Manufacturing Decision -> Operator Dashboard

## Key Features

- Live or replayed Basel disruption signals
- Rhine risk detection from water level and discharge
- Traffic anomaly detection from Basel motor traffic counts
- Weather risk from MeteoSwiss and Basel climate observations
- Cold-chain logic based on WHO temperature-sensitive pharmaceutical transport guidance
- Manufacturing risk score from 0 to 100
- Explainable decision cards for Buffer, Expedite, Reroute, and Quarantine
- Scenario replay for normal day, heat plus traffic delay, Rhine disruption, and combined crisis
- Operator dashboard designed for quick manufacturing decisions

## Data Sources

| Source | Link | Use |
|---|---|---|
| Basel Rhine Water Level & Discharge | https://data.bs.ch/explore/assets/100089/ | Rhine logistics reliability |
| Basel Motor Traffic Counts | https://data.bs.ch/explore/assets/100006/ | Congestion and heavy-vehicle anomaly signals |
| MeteoSwiss Open Data | https://opendatadocs.meteoswiss.ch/ | Weather observations and forecast inputs |
| MeteoSwiss Weather Stations | https://opendatadocs.meteoswiss.ch/a-data-groundbased/a1-automatic-weather-stations | Basel-area measurements |
| Basel-Binningen Climate Data | https://data.bs.ch/explore/assets/100254/ | Local temperature and precipitation history |
| Port of Switzerland Rhine Levels | https://port-of-switzerland.ch/hafenservice/pegel/ | Navigation thresholds and operational context |
| WHO Cold-Chain Guidance | https://www.who.int/publications/m/item/trs961-annex9-modelguidanceforstoragetransport | Quality review and cold-chain decision logic |
| Rhine Suspended Solids Substances | https://data.bs.ch/explore/assets/100068/ | Optional chemical and industrial river signal |

## Demo Scenario

A refrigerated oncology reagent is needed for a production step in six hours.

The dashboard detects:

- Elevated traffic around a logistics corridor
- High ambient temperature
- Deteriorating Rhine conditions

BioFlow Guardian raises the manufacturing risk score and recommends **Reroute**. If handling conditions become uncertain, it recommends **Quarantine** for quality review.

## Impact

BioFlow Guardian helps operators act before external disruption reaches the production floor. It supports faster decisions, fewer avoidable production delays, better cold-chain risk awareness, and clearer quality-review triggers.

## Future Work

- Connect live APIs for automated ingestion
- Add route optimization using OpenStreetMap
- Add material-specific stability profiles
- Add alerting for manufacturing, logistics, and quality teams
- Train anomaly models on historical Rhine, traffic, and weather patterns
