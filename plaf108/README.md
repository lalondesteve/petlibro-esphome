# Petlibro PLAF108 Standalone Feeder

This configuration file implements a full pet feeder management system for the PLAF108.

There are up to 8 meal times supported. Each meal has its own:

- enable switch
- scheduled time
- meal size

There is also a separate `Manual Meal Size` control used by the manual `Dispense Meal` button.

The schedule-related entities are marked as configuration items so Home Assistant groups them in the device's Configuration section instead of mixing them with runtime controls and sensors.

## Home Assistant setup

After flashing and adopting the device in Home Assistant:

1. Open the feeder device page.
2. In the Configuration section, set `Meal Time 1` through `Meal Time 8` as needed.
3. Turn on the matching `Meal Time X Enable` switch for each schedule you want active.
4. Set `Meal X Size` for each enabled schedule.
5. Use `Manual Meal Size` to control the portion used by the `Dispense Meal` button.

Example: you can set `Meal Time 1` to `06:00:00` with `Meal 1 Size` set to `2`, then set `Meal Time 2` to `18:00:00` with `Meal 2 Size` set to `4`.

There is detection for Out Of Food, Motor Stall and Excessive duration for meal dispensing
which will activate the `Alarm` light which can be used for notifications with Home Assistant.
