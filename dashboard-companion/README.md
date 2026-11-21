# Lumineze Dashboard Companion

One Marketplace/HACS dashboard plugin for any number of Lumineze controller dashboards. Requires Home Assistant 2026.5 or newer and the current two-lamp Lumineze profile. No other custom cards are required.

Follow the [installation instructions](../README.md#installation) to install the companion through HACS. Reload the browser. In **Settings → Dashboards → Add dashboard**, select **Lumineze Dashboard Companion** under Community dashboards. Choose the controller and, optionally, up to two illuminance sensors and one UV index sensor. Repeat the dashboard creation step for each vivarium. A selected sensor should measure the same lamp and position used during its calibration sweep.

For each sweep, record 0% with the lamp off, then hold each level for at least two minutes. The graph uses lamp-reported power, discards the first two one-minute samples after a level change, and shows measured lux and lux above the measured 0% ambient baseline. Recorder must retain the selected sensors' history. The graph is observational and does not change controller settings.

Marketplace requires root-level `hacs.json` and `dist/lumineze-dashboard.js`. The build copies the self-contained source to `dist/`. Attach the built file as `lumineze-dashboard.js` when publishing a release; the release workflow verifies the published asset.

Local checks: `cd dashboard-companion && npm run check`.
