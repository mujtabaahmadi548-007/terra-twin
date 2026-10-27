# Terra Twin

A real-time 3D digital twin of Earth that runs in the browser, built with CesiumJS.

**Live site:** https://mujtabaahmadi548-007.github.io/terra-twin/

## Features

- Google Photorealistic 3D Tiles, or Cesium World Terrain with OSM Buildings
- Physically based atmosphere, real sun and moon positions, shadows, weather presets
- Cinematic post-processing: HDR, ambient occlusion, bloom, light shafts, colour grading
- Drone free-flight (F + WASD) and cinematic orbit
- **Live planet**
  - Satellites and the ISS on their real orbits (CelesTrak data, SGP4)
  - Earthquakes from the last 24 hours (USGS)
  - Live aircraft (ADS-B: adsb.fi, adsb.lol, airplanes.live), only when run locally with the helper
- Follow any plane or satellite, ride along with the ISS, or take a plane's cockpit view
- On-screen compass and turn, tilt and zoom buttons

## Using the live site

The first visit asks for a free [Cesium ion access token](https://ion.cesium.com/tokens).
The token is saved only in your own browser.

Live aircraft do not work on the website, because the free flight feeds block web pages
(they send no CORS headers).

## Running it on your own PC (needed for live aircraft)

1. Put `index.html` in a folder.
2. Open the site, turn on **Aircraft**, and click **Download helper**.
3. Put `terra-server.py` in the same folder.
4. In that folder run `python terra-server.py`.
5. Open http://localhost:8000.

The helper needs Python 3.7 or newer and nothing else.

## Updating the site

Upload a new `index.html` to this repository (**Add file → Upload files → Commit changes**).
GitHub Pages republishes it within a minute or two.

## Data sources

- Satellites: [CelesTrak](https://celestrak.org)
- Earthquakes: [USGS](https://earthquake.usgs.gov/earthquakes/feed/)
- Aircraft: [adsb.fi](https://adsb.fi), [adsb.lol](https://adsb.lol), [airplanes.live](https://airplanes.live)

All three aircraft feeds are crowd-sourced; adsb.fi is for personal, non-commercial use.
