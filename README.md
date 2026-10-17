# The Planet Zero record

What the Planet Zero site (planetzero.ai) showed, kept every hour from 16 Oct 2026: the data each view was drawn from, and pictures of
what it drew, so anyone can go back and check. It is a record, not a measurement: the smoke in each picture is an estimate from a
computer model (CAMS), adjusted to the monitors.

- `hours/<YYYY-MM-DDTHH>/data/`: the hour's data, as the site read it (each file gzipped). The site replays a kept hour from these files.
- `hours/<YYYY-MM-DDTHH>/manifest.json`: what the hour was built from, what was late, what was left out and why, the credit line.
- `hours/<...>/*.webp`: pictures the site drew: the default view (Globe, Real Earth) every hour as a thumbnail and every 3 hours at full
  size; each day's worst hour over Southeast Asia in 4 views (Globe and Flat, on Real Earth and Plain).
- `days/<date>.json`, `index.json`: each day's hours and its worst hour; every hour kept.
- `real/`: the day's Real Earth picture, once a day. `history/`: the feed's own record of the monitors, once.

Written every hour by the public feed's Action (yheushen/planetzero-feed). The terms of each source, and what is left out of the record
because of them (aqicn's values; OpenAQ locations under CC BY-SA 4.0): see the credit line in each manifest.

Credits: Copernicus Atmosphere Monitoring Service information 2026 (neither the European Commission nor ECMWF is responsible for any use);
NOAA GFS via NOMADS; NASA FIRMS (LANCE, ESDIS); NASA GIBS (ESDIS); NEA via data.gov.sg (Singapore Open Data Licence 1.0); DOE Malaysia
(Malaysian Government Open Data Terms of Use 1.0); OpenAQ and each owner under its licence; Natural Earth; OpenFreeMap, © OpenMapTiles,
© OpenStreetMap contributors.
