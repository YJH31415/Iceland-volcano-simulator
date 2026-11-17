# YJH's Iceland Volcano Simulator

A web interface prototype for an Eyjafjallajökull (2010) volcanic ash dispersion simulator.

## Live site

After enabling GitHub Pages, the site will be available at:

https://yjh31415.github.io/Iceland-volcano-simulator/

## Current implementation

- Responsive glass-style scientific dashboard
- MapLibre GL JS map centered on Iceland and Europe
- Eyjafjallajökull vent marker and five city markers
- Timeline controls and playback speed selector
- City alert panel and the project's five concentration thresholds
- Experiment parameter controls
- Demo JSON and chart PNG export

## Scientific status — read before interpreting the display

This repository currently contains the **front-end prototype only**. The ash plume shown on the map is generated illustrative geometry for testing the interface. It is **not** a measured 2010 ash cloud, a forecast, or the output of a validated atmospheric model. Concentration metrics are intentionally shown as unavailable until a physical solver is connected.

The planned scientific implementation is a 3-D Eulerian, multi-size-bin concentration model using conservative finite-volume transport, meteorological reanalysis fields, gravitational settling, turbulent diffusion, and wet/dry deposition. The model will require independently verified eruption-source data and validation against published observations and established models before its outputs can be described as scientific results.

## Run locally

This is a static site. Open `index.html` in a browser, or serve the repository directory:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Deployment

In GitHub, open **Settings → Pages**, select **Deploy from a branch**, choose **main** and **/(root)**, then save. The included `.nojekyll` file is compatible with root-based static hosting.

## External libraries

- MapLibre GL JS
- Google Fonts

The map style is loaded from the MapLibre demo tile service. A production deployment should select a suitable tile provider and review its usage terms.
