# Nukabus

NukaBus is a Japan-focused transit map app for riders that shows nearby lines and upcoming departures and, when available, overlays live vehicle positions and route shapes using ODPT data.

## What it does
- For public transport riders in Japan (starting with Tokyo), shows nearby transit options (lines + upcoming departures) from GTFS.
- When realtime is available, shows live vehicle locations and displays the route shape only after the user selects a line (to keep the map clean).

## Demo
- Video: <YouTube link>
- Slides (PDF): <link if you also upload it here>

## How it works (high level)
- Backend (Swift/Vapor + Postgres/PostGIS + Redis): imports GTFS (stops/routes/trips/stop_times/calendar), builds route lines/shapes, polls ODPT realtime where supported, and serves simple JSON APIs.
- iOS (SwiftUI + MapKit): requests nearby lines based on user location; selecting a line fetches /routes/{id}/vehicles and /routes/{id}/shape to render vehicles + the route.

## Status
TestFlight public link could not be generated before the deadline due to Apple ID 2FA (trusted device unavailable). A TestFlight link will be added as soon as access is restored.
