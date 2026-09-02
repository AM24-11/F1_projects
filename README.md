# F1 Telemetry & Strategy Analysis
 
A growing collection of motorsport data analysis projects built on the [FastF1](https://github.com/theOehrly/Fast-F1) Python API. Each project pulls real session telemetry and timing data to explore driver performance, race strategy, and car behavior.
 
## Why this repo
 
I'm a Computational Science Master's student interested in applying numerical modeling and data analysis to motorsport engineering. These projects are how I'm learning the domain — starting from raw telemetry and working toward the kind of strategy and performance questions race engineers actually deal with.
 
## Projects
 
### 1. Driver Telemetry Comparison — 2023 Brazil GP Qualifying
 
Compares fastest qualifying laps for three drivers (Verstappen, Hamilton, Alonso) using speed, throttle, and brake telemetry. Includes:
- Speed trace and 3D track-mapped speed visualization
- Lap delta-time analysis to identify where time was gained or lost
- Corner-level breakdown of braking points
**Key finding:** Verstappen's advantage came primarily from earlier brake release and earlier throttle application out of corners, converting into a straight-line speed advantage rather than raw cornering speed.
 
### 2. Tyre Degradation Model — 2023 Monaco GP
 
Models tyre performance drop-off across a stint using lap time and compound data from race sessions. Includes:
- Lap time vs. tyre age curves by compound
- Degradation rate estimation
- Discussion of how Monaco's track characteristics have a higher influence on lap times than tyre degradation alone.
## Planned additions
 
- [ ] Multi-circuit extension of the driver comparison, to test whether braking/throttle patterns are driver traits or circuit-specific
- [ ] Pit stop strategy simulation
- [ ] Race pace vs. quali pace correlation
## Setup
 
```bash
pip install fastf1 pandas numpy matplotlib
```
 
Each project notebook caches session data locally via `fastf1.Cache` — first run for a given session will be slower as data downloads and subsequent calling will be faster.
 
## Data source
 
All timing and telemetry data via the [FastF1](https://github.com/theOehrly/Fast-F1) API, which sources official F1 timing data.
