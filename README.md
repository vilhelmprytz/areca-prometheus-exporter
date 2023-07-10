# areca-prometheus-exporter

Prometheus exporter for Areca RAID cards. Exporter depends on Areca CLI being present.

## Features

- Provides metrics for the Areca RAID card to be scraped by Prometheus.
- Supports the following metrics:
  - `areca_sys_info`: Constant metric with a value of 1 labeled with information about the Areca controller.
  - `areca_raid_set_state`: Areca RAID set state, where 0 represents normal and 1 represents degraded.

## Prerequisites

Before using the Areca Prometheus Exporter, ensure you have the following prerequisites installed:

- `areca.cli64` in `$PATH`

## Contributors ✨

Copyright (C) 2023, Vilhelm Prytz, <vilhelm@prytznet.se>

Licensed under the [MIT license](LICENSE).

Created and maintained by [Vilhelm Prytz](https://github.com/vilhelmprytz).
