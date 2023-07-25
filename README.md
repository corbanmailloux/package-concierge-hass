# Package Concierge Scraper Component for Home Assistant

**This component is not currently maintained**

Home Assistant custom component for [Package Concierge](https://packageconciergeadmin.com) that can login and get a count (maximum 5) of packages waiting to be picked up from the Package Concierge package locker system.
It also supports multiple users by registering multiple sensors.

It exposes a sensor (by default `sensor.package_concierge_USERNAME`, but overridden by setting `name:`) that is a count of the number of packages in the "Delivered" status.

## Installation Using HACS

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)

This custom component can be installed using HACS. Follow [these steps](https://hacs.xyz/docs/faq/custom_repositories) and use the repository URL `https://github.com/corbanmailloux/package-concierge-hass`

## Manual Installation

Copy the contents of the `custom_components/package_concierge/` folder to `<config_dir>/custom_components/package_concierge/` on your Home Assistant installation.

## Configuration

Add the following to your `configuration.yaml` file (or a package file):

```yaml
# Example configuration.yaml entry
sensor:
  - platform: package_concierge
    name: package_concierge_corban # Optional
    username: "USERNAME"
    password: "0000" # PIN
```
