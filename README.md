# embinotec todo display made for esphome

[![CI](https://github.com/embinotec/embinotec-esphome-tododisplay/actions/workflows/ci.yml/badge.svg)](https://github.com/embinotec/embinotec-esphome-tododisplay/actions/workflows/ci.yml)
[![Made for ESPHome](https://img.shields.io/badge/Made%20for-ESPHome-blue?logo=esphome)](https://esphome.io/guides/made_for_esphome/)
[![ESPHome Version](https://img.shields.io/badge/ESPHome-%E2%89%A52026.8.0-green)](https://esphome.io/changelog/)
[![License](https://img.shields.io/github/license/embinotec/embinotec-esphome-tododisplay)](LICENSE)

![Made for ESPHome](https://esphome.io/images/made-for-esphome-black-on-white.svg)

Eink Display zur Anzeige von ToDo-Listen aus HomeAssistant.


## Hardware

**Hardware could be purchased at [embinotec.de](https://www.embinotec.de/produktseite/todo-display).**  
![TodoDisplay](./assets/todo_display.jpeg "Display on fridge")

## Install esphome device

Besides the preconfigure device setup in section `Fallback wifi` you have two possibilities to setup your device in your own esphome instance.

1. Copy the tododisplay.yaml into your ´esphome/config/´ folder. OR
2. Setup a new device in your esphome builder and import the tododisplay.yaml as configuration. OR
3. Add a new plain ESP32s3 generic device in esphome build and add `dashboard_import: https://github.com/embinotec/embinotec-esphome-tododisplay/blob/master/esphome/tododisplay.yaml`

### Fallback wifi

Display will be deliverted preconfigured. Scan your wifi area for a device called todo_display. Connect to the wifi with password `embinotec`. Set your wifi credentials in the captive portal.

## Install in HomeAssistant



### Setting up the template

- Add folder `templates` in homeAssistant/config 
``` bash 
  mkdir templates
```
- Add the following line to your `configuration.yaml` to include all valid templates
  ``` yaml
  template: !include_dir_merge_list templates/
  ```
- Copy the {project}\HomeAssistant\template_todo.yaml into templates folder
- Do a full restart your HomeAssistant instance.