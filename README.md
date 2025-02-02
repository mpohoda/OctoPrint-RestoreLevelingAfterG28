# OctoPrint Plugin – Restore Leveling After G28

[![Python](https://github.com/Xennis/OctoPrint-RestoreLevelingAfterG28/workflows/Python/badge.svg?branch=master&event=push)](https://github.com/Xennis/OctoPrint-RestoreLevelingAfterG28/actions?query=workflow%3APython+event%3Apush+branch%3Amaster)

Automatically keeps bed leveling on after `G28` (Auto Home).

Marlin code `G28` disables bed leveling. The plugin restores the prior state:

* Before the `G28` command a `M420 V` is send to check if leveling is enabled or not.
* If leveling was enabled: After the `G28` command a `M420 S1 Z2` is send to enable leveling.
* Fixed compensation for professional firmware

That same behaviour can be enabled in the Marlin firmware via `RESTORE_LEVELING_AFTER_G28`.

## Setup

Install via the bundled [Plugin Manager](https://docs.octoprint.org/en/master/bundledplugins/pluginmanager.html)
or manually using this URL:

```
https://github.com/mpohoda/OctoPrint-RestoreLevelingAfterG28/archive/master.zip
```

## Configuration

The plugin has no configuration and does not adjust the UI.
