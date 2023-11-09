# lutron_custom_component
Lutron custom component for HA using custom veresion of pylutron. Works with and tested for Homeworks QS, and is set up as HACS component.

Features:
- ability to include a `db_file` to the configuration, so that the Lutron component can cache the data
```
lutronqs:
  host: 192.168.1.23
  username: lutron
  password: password
  db_file: 'Lutron.xml'
```
- LEDs in keypad's buttons that are configured as "integration", are created as Light devices `LutronLedLight`, so you can control them
- Binary sensors for Occupancy group
- Buttons to support press, release, hold, double tap, and hold release status
- Added a new `LutronMotorBlind` to support motorized shades/blinds via a Motor output

The custom component is loading the custom `pylutron` version in `manifest.json`.
