# Mick Edition Klipper Macro Pack

## Install

Copy the `macros` folder into your Klipper config folder.

Then add this to `printer.cfg`:

```ini
[include macros/mick_macro_pack.cfg]
```

Remove or comment out your old includes for:

```ini
1.cabinet_lights.cfg
1.Cabinetfans.cfg
1.clean_nozzle.cfg
1.filament_handling.cfg
1.print_start.cfg
1.purge_to_bucket.cfg
```

Do not include both the old files and this pack, or Klipper will throw duplicate macro errors.

## File layout

- `printer_settings.cfg` - central temps, positions, speeds, purge/brush settings
- `print_start.cfg` - PRINT_START / PRINT_END / homing / QGL
- `temperature_wrappers.cfg` - M109 / M190 status wrappers
- `filament_handling.cfg` - load, unload, purge, retract, M600
- `nozzle_clean.cfg` - CLEAN_NOZZLE
- `purge_to_bucket.cfg` - PURGE_TO_BUCKET
- `adaptive_purge.cfg` - ADAPTIVE_PURGE
- `park.cfg` - _MOVE_AWAY / PARK_CENTER_REAR
- `fans.cfg` - Nevermore and Bedfans
- `lights.cfg` - LED pin and LED_ON / LED_OFF
- `service_mode.cfg` - SERVICE_MODE and SERVICE_PARK
- `safety.cfg` - exclude_object

## New useful command

```ini
SERVICE_MODE
```

Parks at the front service position, warms the hotend to service temp, and opens a prompt with Load, Unload, Clean Nozzle, and Purge Bucket.
