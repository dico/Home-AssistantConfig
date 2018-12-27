
# Home Assistant config

Some of the things I test is posted on my [blog](https://robert.stadsbygd.net/category/internetofthings/).

![alt text](https://github.com/dico/Home-AssistantConfig/blob/master/screenshots/01_main_12_2018.jpg)

## Components and controllers (GW)
- [Aeotec Z-stick Gen 5](https://home-assistant.io/components/zwave/)
- [Telldus](https://home-assistant.io/components/tellduslive/)
- [IKEA Trådfri (Tradfri)](https://home-assistant.io/components/tradfri/)
- [Sensibo](https://home-assistant.io/components/climate.sensibo/)
- [Netatmo](https://home-assistant.io/components/netatmo/)
- [Verisure](https://home-assistant.io/components/verisure/) / [Verisure Lock](https://home-assistant.io/components/lock.verisure/)
- [Ubiquiti Unifi direct AP](https://home-assistant.io/components/device_tracker.unifi_direct/)
- [MQTT](https://home-assistant.io/components/mqtt/)
- [Intesishome - pyIntesisHome (custom)](https://github.com/jnimmo/pyIntesisHome) (Not in use atm)
- [Plex](https://home-assistant.io/components/media_player.plex/)
- [Samsung Smart TV](https://home-assistant.io/components/media_player.samsungtv/)
- [Apple TV](https://home-assistant.io/components/apple_tv/)
- [Steam](https://home-assistant.io/components/sensor.steam_online/)





## Devices
### Z-wave
- [FIBARO Wall Plug](https://products.z-wavealliance.org/products/1653)
- [FIBARO Motion Sensor](https://products.z-wavealliance.org/products/2762)
- [FIBARO Double Switch 2](https://products.z-wavealliance.org/products/2731)
- [FIBARO Button](https://products.z-wavealliance.org/products/1944) (not in use atm)
- [FIBARO Smoke Sensor (FGSD-002)](https://products.z-wavealliance.org/products/1273)
- [NorthQ Power Reader & Power Manager](https://products.z-wavealliance.org/products/69) (not in use atm)
- [Multireg Z-Wave Thermostat](https://products.z-wavealliance.org/products/1182)
- [Aeotec Smart Dimmer 6](https://products.z-wavealliance.org/products/1519)
- [Vision Motion Detector (with Temperature Sensor)](https://products.z-wavealliance.org/products/1070)
- [Vision Siren with LED strobe light](https://products.z-wavealliance.org/products/1009)
- [Telldus Plug-in Switch (Schuko)](https://products.z-wavealliance.org/products/1536)
- [IKEA Trådfri (Tradfri) bulbs](http://www.ikea.com/no/no/catalog/categories/departments/lighting/36812/)
- [Mco Home Air Quality Monitor Co2](https://www.dustin.no/product/5011024221/air-quality-monitor-co2) (Used with Tellstick and MQTT to HA)
- [Aeotec Wallmote](https://aeotec.com/z-wave-wireless-switch)

### Other
- [RX-Multi for garage doors](https://www.portspesialisten.com/fjernkontroll/mottaker-433mhz/)  [(Tutorial)](https://robert.stadsbygd.net/2015/05/10/open-garage-port-with-telldus/)
- [MQTT - Nissan LEAF](https://robert.stadsbygd.net/2017/08/18/nissan-leaf-in-home-assistant/)
- [Div. china IP/WiFi cameras](https://robert.stadsbygd.net/2017/06/13/two-new-ipwifi-cameras/)
- Different temperature/humidity sensors (433MHz) [Teknikmagasninet (NO)](https://www.teknikmagasinet.no/produkter/hjem-o-husholdning/termometre/remote-thermo-sensor), [Clas Ohlson (NO)](https://www.clasohlson.com/no/Temperaturgiver-hygrometer/36-1797)

Devices like Apple TV, Sensibo, Verisure doorlock, Intesishome, etc. should be self explanatory based on the component-list above.



## Automations
### Washmachine notification
Using av Fibaro Wall Plug to monitor power usage for the washingmachine, to then send a notification when it's done.

### Lights and motion
Turning on/off lights if motion triggered.
Good morning lights if motion triggered between 06:00 and 10:00.

### Other notifications
Alert if CO2 levels are over 1000ppm and 2000ppm.

## Multiple Tellstick to HA
I have created a simple docker image to fetch Tellstick sensor values from the local API to HA, as HA does not support multiple Tellstick's at this time.
The code can be found here: https://github.com/dico/tellstick_mqtt


## Theme

[Midnight theme](https://community.home-assistant.io/t/midnight-theme/28598) from HA Community