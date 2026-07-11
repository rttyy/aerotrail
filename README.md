# AeroTrail

A companion application for Microsoft Flight Simulator that records your flights,
presents them on a map with detailed statistics, and — if you choose — publishes
them to your Strava account.

AeroTrail runs alongside the simulator and records automatically: begin taxiing
and it starts, land and shut down and the flight is saved with its track,
statistics and a landing rating. It is free and works with both Microsoft Flight
Simulator 2020 and 2024.

## Screenshots

![flight](docs/images/flight.png)
![list](docs/images/list.png)
![Settings](docs/images/settings.png)
![Stats](docs/images/stats.png)

## Features

**Automatic flight recording.** AeroTrail detects the simulator and connects on
its own. Recording starts when the aircraft begins to move or takes off and stops
after landing and engine shutdown. Manual start, pause and stop are always
available. Pauses, time acceleration, crashes and map repositioning are handled
correctly.

**Live map.** While you fly, your track is drawn in real time and the view follows
the aircraft. The map can be tilted into a 3D view showing real terrain relief,
with the flight path drawn at its true altitude.

**Flight history.** Every flight is listed with a map thumbnail, its route
(departure and arrival airports are identified automatically), the aircraft, and a
landing rating. Flights can be filtered by aircraft, airport or name.

**Flight details.** Each flight shows its track coloured by altitude, an
interactive altitude and speed graph synchronised with the map, and summary tiles
for distance, airborne time, maximum altitude, and maximum and average speed.

**Personal records.** AeroTrail tracks your longest flight, greatest distance,
highest altitude, top speed and smoothest landing, along with cumulative totals.

**Strava publishing (optional).** A flight can be published to Strava in one
click, with an automatically generated title and description that you can edit
beforehand. The recorded altitude is preserved on the resulting activity.

**GPX import.** Flights recorded by other tools can be imported from GPX files and
become full AeroTrail flights.

**Localisation.** The interface is available in English and French.

## Requirements

| Component | Purpose | Required |
|---|---|---|
| Windows 10 or 11 (64-bit) | The application | Yes |
| Microsoft Flight Simulator 2020 or 2024 | The flights to record | Yes |
| .NET 8 Desktop Runtime | Runs the application (the installer offers it if missing) | Yes |
| WebView2 runtime | The map (pre-installed on Windows 11) | For the map |
| Internet connection | Map tiles and Strava publishing | For map and Strava |

Recording works fully offline; only the map and Strava publishing require a
connection.

## Installation

1. Download `AeroTrail-0.4.0-setup.exe` from the Releases page.
2. Run it. Because AeroTrail is independent freeware and is not code-signed,
   Windows SmartScreen may show a warning. Select **More info**, then
   **Run anyway**.
3. Follow the installer. You may optionally create a desktop shortcut and have
   AeroTrail start with Windows.

No account or sign-up is required to record and view your flights.

## Getting started

1. Launch AeroTrail and Microsoft Flight Simulator, in either order. The status
   bar shows "Connected to MSFS" once the simulator is detected.
2. Fly. Recording starts automatically as the aircraft begins to move, and the
   application switches to the live map.
3. Land and shut down the engines. After a short standstill the flight is
   finalised and appears in the history with its map, statistics and landing
   rating.
4. Open any flight for the detailed map and graph, and review your bests under
   Records.

All data is stored on your computer, under `%LOCALAPPDATA%\AeroTrail\`. Nothing is
sent anywhere unless you choose to publish a flight to Strava.

## Publishing to Strava

Publishing is optional and requires no setup. Open **Settings → Strava →
Connect Strava**, review the consent screen, and authorise AeroTrail on Strava's
own page in your browser; your credentials are entered on strava.com, never in
AeroTrail. Afterwards, use **Publish** on any flight, or enable automatic
publishing in Settings. You can disconnect and delete your Strava data at any time
from Settings.

Strava publishing is currently available to a limited number of early users while
an agreement with Strava to raise this limit is being finalised. If the connection
is temporarily unavailable, further capacity is on the way.

## Privacy

AeroTrail is local-first and operates no servers of its own. Flight data is
generated and stored only on your computer. Strava authentication tokens are
stored locally and encrypted. Data is sent to Strava only when you publish a
flight, and only to Strava. There are no accounts, tracking or telemetry.

Full privacy policy: <https://rttyy.github.io/aerotrail-legal/>

## Support

For questions, bug reports or suggestions: eliottferry1@gmail.com. When reporting
a problem, the log files under `%LOCALAPPDATA%\AeroTrail\logs\` are useful to
attach.

## Disclaimer

Developed by a320cockpitdiy. AeroTrail is an independent application and is not
affiliated with, endorsed by or sponsored by Strava, Inc. or Microsoft. "Strava"
is a trademark of Strava, Inc.; "Microsoft Flight Simulator" is a trademark of
Microsoft. Map data © OpenStreetMap contributors; terrain elevation data ©
Mapzen / AWS.
