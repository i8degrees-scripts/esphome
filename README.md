---
---

# esphome

*...*

## usage

```shell
substitutions:
  devicename: esplivingroom
  # espbedroom 1 unique name for each ESP device

esphome:
  name: ${devicename}

tvoc:
  name: ${devicename}_ens160_tvoc
```

### hierarchy

- `configs/esp8266`
- *...*

```yaml`
mqtt:
  on_message:
    lamba: |-
      id(my_api)->set_reboot_timeout(0);
```

- Looks like I might be able to use the "wifi.connected" status combined with a "restart_button" and
try to trigger that internally within the automation. Set a "cycle active" flag at the beginning of a watering cycle and clear it at the end of the cycle.
I'll then have a periodic check that "cycle active" is false, that wifi.connected is also false, then call the button press event of a restart_button entity.


## reference documents

[1]: *...*
