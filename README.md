# Tinxy addon for home assistant


Can be used for the smart switches from [Tinxy.in](https://tinxy.in/)

# Usage 


Install HACS

https://hacs.xyz/


Add custom repository to hacs 

```
https://github.com/arevindh/tinxy-hacs
```

Install `Tinxy Smart Devices` from `hacs`

Restart Home Assistant

Get the `api key` from the Tinxy application.

Add the following config in `configuration.yaml` which is located in `<PATH_TO_HOME_ASSISTANT_CONFIG_DIR>/configuration.yaml`

```
switch:
  - platform: tinxy
    api_key : 12345678901234567890
    scan_interval: 10
fan:
  - platform: tinxy
    api_key : 12345678901234567890
    scan_interval: 10
light:
  - platform: tinxy
    api_key : 12345678901234567890
    scan_interval: 10
```

Restart Home Assistant

# Current issues

Due to the reponse delay via they api the toggle will have a delay for approx 3s . Status change can be adjusted using `scan_interval` parameter (better to keep this above `7` to avoid slowing the HA server)
