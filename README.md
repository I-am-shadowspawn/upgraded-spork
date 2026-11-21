# Lumineze Dashboard Companion

A Home Assistant community dashboard for the
[Lumineze ESPHome controller](https://github.com/I-am-shadowspawn/lumineze-controller-esphome).
Install the companion once and create a separate dashboard for each controller.
It requires Home Assistant 2026.5 or newer and the current two-lamp controller
profile. No other custom cards are required.

## Installation

1. In HACS, add `https://github.com/I-am-shadowspawn/upgraded-spork` as a
   custom repository in the **Dashboard** category.
2. Install **Lumineze Dashboard Companion**. If no release is available, select
   the default branch. Reload your browser.
3. In **Settings → Dashboards → Add dashboard**, select **Lumineze Dashboard
   Companion** under Community dashboards. Select the controller and optional
   illuminance and UV index sensors. Repeat for each controller.

See the [companion guide](dashboard-companion/README.md) for calibration
details. The [legacy YAML dashboard](dashboards/README.md) is also available
and has separate custom card requirements.

## Development

With Node.js installed, run `cd dashboard-companion && npm run check` to run the
tests, build the self-contained HACS asset, and check that `dist/` is current.
Commit the rebuilt `dist/lumineze-dashboard.js` with source changes. Releases
must include that file as an asset.

This is an independent, unofficial project and is not affiliated with or
endorsed by Arcadia Reptile.
