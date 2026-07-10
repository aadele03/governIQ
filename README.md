# GovernIQ — Citizen Voice Intelligence

A single-page web app that tracks **citizen mood** across Nigerian states, read from public discussion (Nairaland, Nigerian daily news, and public X/Twitter & Facebook reaction).

**Live:** https://aadele03.github.io/governIQ

## What's in it
- **6 states:** Lagos, Oyo, Ogun, Rivers, Kano, FCT (Abuja) — switchable from the sidebar dropdown.
- **12 issues per state:** Traffic, Roads, Flooding, Waste, Cost of living, Security, Healthcare, Education, Housing, Markets, Electricity/Power, Governance & taxation.
- **13 modules:** Dashboard, Mood Trajectory, Heatmap, Issue Trajectories, Top Complaints, Praised Actions, LGA Mood, Project Trust, Anger Spikes, Risk & Action, Your Strategist (Q&A), Executive Brief, Methodology.
- **History:** quarterly series Q1 2020 → present, plus a rolling daily snapshot.

## How it updates
- A nightly scheduled task refreshes the **current** reading for every state from public sources and rewrites this `index.html`.
- The deep history is anchored at the quarter level; the daily view is the live "now".

## Publishing (manual step)
The refresh writes the file into this repo, but publishing is one manual step:

1. Open **GitHub Desktop** (this repo).
2. Review the change to `index.html`.
3. **Commit to main** → **Push origin**.
4. GitHub Pages redeploys in ~1 minute.

> GitHub Pages must be enabled: repo **Settings → Pages → Source = `main`, root**.

## Data caveat
Mood scores, LGA-level figures, complaint intensities and forecasts are **modeled estimates** from public online discussion — directional, not a representative survey. Use as early-warning and prioritisation support; pair high-stakes decisions with official data and on-the-ground verification. See the in-app **Methodology** module for full detail.

## File
- `index.html` — the entire app (self-contained: data, styles, fonts and logic inline). No build step.
