# The Planet Zero record

What the Planet Zero site (planetzero.ai) showed, kept every hour from 16 Oct 2026: the data each view was drawn from, and pictures of
the map it drew, so anyone can go back and check. It is a record, not a measurement: the smoke in each picture is an estimate from a
computer model (CAMS), adjusted to the monitors.

- `hours/<YYYY-MM-DDTHH>/data/`: the hour's data, as the site read it (each file gzipped). The site replays a kept hour from these files.
  Since 18 Oct 2026 each hour also keeps the feed's history of the 48 hours to it (`data/history/`), so a replay reads the history as it
  stood then.
- `hours/<YYYY-MM-DDTHH>/manifest.json`: what the hour was built from, what was late, what was left out and why, each data file with its
  size, the credit line.
- `hours/<...>/*.webp`: pictures of the map the site drew (the map alone, never the site's page), each with a strip under it that says
  the hour, that the smoke is an estimate from a computer model, the key with each colour named, the wind's and the fires' times and the
  base: the default view (Globe, Real Earth) every hour as a thumbnail and every 3 hours at full size; each day's worst hour over
  Southeast Asia in 4 views (Globe and Flat, on Real Earth and Plain), added once when the day ends. Thumbnails are half the width.
- `days/<date>.json`, `index.json`: each day's hours (with each picture's strip in words), its worst hour, its 4 views and their
  thumbnails; every hour kept.
- `real/`: the day's Real Earth picture, once a day. `history/`: the feed's own record of the monitors as it was on 18 Oct 2026 (each
  hour keeps its own since then).
- The branch `today`: today's worst hour so far in its 4 views, drawn every 3 hours and replaced each time (1 commit), until the day's
  final 4 are added here. The branch `timelapse`: 1 frame a day, Real Earth and Plain, MP4 and GIF, replaced once a day.

Written once: a kept hour's files are added by the first build of that hour and never changed; only the indexes change from hour to hour.
Nothing is thinned and nothing is deleted. (The hours of 16 to 18 Oct were brought to this shape once, on 18 Oct 2026: their history
added, their pictures drawn again as the map alone.)

Written every hour by the public feed's Action (yheushen/planetzero-feed). The terms of each source, and what is left out of the record
because of them (aqicn's values; OpenAQ locations under CC BY-SA 4.0; BMKG's monitors, shown live only): see the credit line in each
manifest.

Credits: Copernicus Atmosphere Monitoring Service information 2026 (neither the European Commission nor ECMWF is responsible for any use);
NOAA GFS via NOMADS; NASA FIRMS (LANCE, ESDIS); NASA GIBS (ESDIS); NEA via data.gov.sg (Singapore Open Data Licence 1.0); DOE Malaysia
(Malaysian Government Open Data Terms of Use 1.0); OpenAQ and each owner under its licence; Natural Earth; OpenFreeMap, © OpenMapTiles,
© OpenStreetMap contributors.
