# Automated Lighting
This blueprint can help you automate your lights.

## It can do the following:
- Turn on/off lights.
- Turn on different lights during the day and evening/night.
- If a button/remote/switch has been pressed (and gives an action) a cooldown will be triggered. This way if you just switched on/off the lights and moved out the room during the lights won't change.

## Options:
##### ++ You have to fill in all the fields for the blueprint to work ++'
- Select lights for during the day (lights_day)
- Select lights for during the evening/night (lights_night)
- Select what time the day lights will start (start_time)
- Select what time the evening/night lights will start (end_time)
- Select the cooldown input_boolean created earlier (cooldown)
- Select the duration of the cooldown (cooldown_time)
- Select the occupation binary_sensor created earlier. This way you can track mutliple motion or other sensors via one entity (trigger_occupied)
- Select button/switch/remote sensor entity to use a trigger.
- Write button/switch/remote sensor as text. For example: left/right/up/down/on/off/single_left/double_left etc. (trigger_remote_1) 

## This blueprint requires a few things:
- Set up a helper: toggle.
- Set up a binary_sensor in yaml mode (see binary_sensor.yaml and include that in your configuration).

