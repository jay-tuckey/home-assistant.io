---
title: Epson
description: Instructions on how to integrate Epson projector into Home Assistant.
ha_category:
  - Media Player
ha_release: 0.72
ha_iot_class: Local Polling
ha_domain: epson
ha_codeowners:
  - '@pszafer'
ha_config_flow: true
---

The `epson` platform allows you to control a Epson projector from Home Assistant.

To add Epson to your installation go to Integration page and add Epson Projector or configure via `configuration.yaml`.

### Configuration

Add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
media_player:
  - platform: epson
    host: 192.168.0.123
```

{% configuration %}
host:
  description: The host name or address of the Epson projector
  required: true
  type: string
port:
  description: The HTTP port number.
  required: false
  type: integer
  default: 80
name:
  description: The name of the device used in the frontend.
  required: false
  type: string
  default: "EPSON Projector"
{% endconfiguration %}

### Supported features

- turn on/off
- set input
- set/get color mode
- increase/decrease volume
- mute/unmute audio
- send next/previous track

### Supported devices

- Epson projectors supporting ESC/VP21 protocol.

### Tested devices

- Epson EH-TW5350
- Epson EH-TW7000

To make this module work you need to connect your projector to your LAN.
The best is to use iProjection app by Epson to test if it is working.
