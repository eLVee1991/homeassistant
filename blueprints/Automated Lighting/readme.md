# Automated Lighting
This blueprint can help you automate your lights.

## It can do the following:
- Turn on/off lights.
- Turn on different lights during the day and evening/night.
- If a button/remote/switch has been pressed (and gives an action) a cooldown will be triggered. This way if you just switched on/off the lights and moved out the room during the lights won't change.

## Options:
###### +++ You have to fill in all the fields for the blueprint to work +++
- Select lights for during the day (lights_day)
- Select lights for during the evening/night (lights_night)
- Select what time the day lights will start (start_time)
- Select what time the evening/night lights will start (end_time)
- Select the cooldown input_boolean created earlier (cooldown)
- Select the duration of the cooldown (cooldown_time)
- Select the occupation binary_sensor created earlier. This way you can track mutliple motion or other sensors via one entity (trigger_occupied)
- Select the occupation binary_sensor time before turning off the lights. For exaple 5 minutes (trigger_occupied_time)
- Select button/switch/remote sensor entity to use a trigger. This must be a sensor entity (trigger_remote)
- Give a button/switch/remote sensor action as text. For example: left/right/up/down/on/off/single_left/double_left etc. (trigger_remote_action_1 and 2) 

## This blueprint requires a few things:
- Set up a helper in the devices section of the UI. Select the 'toggle' type. This creates an input_boolean for the cooldown entity used in the script.
- Set up a binary_sensor in yaml mode (see binary_sensor.yaml and include that in your configuration). This sensor can track multiple entities for given states so that you can track multiple motion sensors or other room occupancy trackers in one sensor. If one is one, the room will be occupied thus the sensor will be on.

