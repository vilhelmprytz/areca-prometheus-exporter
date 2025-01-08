# areca-prometheus-exporter

Prometheus exporter for Areca RAID cards. Exporter depends on Areca CLI being present.

## Features

- Provides metrics for the Areca RAID cards to be scraped by Prometheus.
- Supports the following metrics:
  - `areca_up`: '0' if a scrape of the Areca CLI was successful, '1' otherwise.
  - `areca_sys_info`: Constant metric with a value of 1 labeled with information about Areca controllers.
  - `areca_raid_set_state`: Areca RAID set state, where 0 represents normal and 1 represents degraded.
  - `areca_disk_info`: Constant metric with value 1 labeled with info about all physical disks attached to Areca controllers.
  - `areca_disk_state`: Areca controller metric for disk state, 0 for normal, 1 for error
  - `areca_disk_media_errors`: Metric for media errors of all physical disks attached to Areca controllers.

## Config options

| Option               | Description                       | Default       |
| -------------------- | --------------------------------- | ------------- |
| `--collect-interval` | How often to poll each controller | `5s`          |
| `--cli-path`         | Path to Areca CLI binary          | `areca.cli64` |
| `--controllers`      | How many controllers to scrape    | `1`           |

## Prerequisites

Before using the Areca Prometheus Exporter, ensure you have the following prerequisites installed:

- Areca CLI binary in `$PATH` (`areca.cli64`) or at the path specified by option `cli-path`

## Contributors ✨

Copyright (C) 2024, Vilhelm Prytz, <vilhelm@prytznet.se>

Licensed under the [MIT license](LICENSE).

Created and maintained by [Vilhelm Prytz](https://github.com/vilhelmprytz).
