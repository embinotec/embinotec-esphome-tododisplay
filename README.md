# embinotec todo display made for esphome

[![CI](https://github.com/embinotec/embinotec-esphome-tododisplay/actions/workflows/ci.yml/badge.svg)](https://github.com/embinotec/embinotec-esphome-tododisplay/actions/workflows/ci.yml)
[![Made for ESPHome](https://img.shields.io/badge/Made%20for-ESPHome-blue?logo=esphome)](https://esphome.io/guides/made_for_esphome/)
[![ESPHome Version](https://img.shields.io/badge/ESPHome-%E2%89%A52026.8.0-green)](https://esphome.io/changelog/)
[![License](https://img.shields.io/github/license/embinotec/weatherstation)](LICENSE)

![Made for ESPHome](https://esphome.io/images/made-for-esphome-black-on-white.svg)

Eink Display zur Anzeige von ToDo-Listen aus HomeAssistant.

## Install in HomeAssistant

### Fallback wifi

Display will be deliverted preconfigured. Scan your wifi area for a device called todo_display. Connect to the wifi with password `embinotec`. Set your wifi credentials in the captive portal.

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