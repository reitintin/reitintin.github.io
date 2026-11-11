# Reitintin

A fast, map-free HSL journey planner in a single HTML file. Step-by-step
itineraries, no map, no build step at runtime, no tracking.

**Live:** <https://reitintin.github.io/>

This repository only hosts the compiled single-file build. The source,
development server, and API proxy live at
<https://github.com/mistenman/reitintin>.

## API key

The planner talks to the Digitransit routing and geocoding APIs, which need a
subscription key. Get one free at <https://portal-api.digitransit.fi/>.

On first visit the page asks for the key and stores it in this browser's
`localStorage` (`reitintin:api-key`). It is never sent anywhere except
Digitransit. Leave the key out and nothing loads.

## Features

- From/To geocoding limited to the HSL area, GPS for From when it is empty
- Now / Depart at / Arrive by, with a 4-digit time entry that auto-inserts the colon
- Walking speed and transit mode toggles that re-search automatically
- Recent From/To selections, walking speed, and language persist locally
- Every stop and place name links to its coordinates via `geo:`
- Finnish by default, English toggle
- Open the same search in HSL Reittiopas

## Keyboard

- `Tab` / `Shift+Tab` move through fields and suggestions
- `ArrowUp` / `ArrowDown` move through suggestions
- `Enter` picks a suggestion or runs the search
- `Escape` closes the suggestion list

Emergency stops and other service alerts are not shown; this is a timetable
browser, not a disruption monitor.

## License

MIT
