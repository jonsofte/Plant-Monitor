
# Plant Monitor

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

A simple sketch for monitoring of plants with the [LILYGO® T-Higrow ESP32 board](https://www.banggood.com/LILYGO-T-Higrow-ESP32-WiFi-+-bluetooth-+-DHT11-Soil-Temperature-And-Humidity-Sensor-Module-p-1196250.html). Created for monitoring of my chilli plants with InfluxDB and Grafana. Project setup and library dependencies is handled with [PlatformIO](https://platformio.org) Visual Studio Code extension.

The app will log the following data to InfluxDB:

* Air temperature and humidity
* Light amount
* Soil moisture and salinity
* Device voltage  
  
## Application Configuration

In the **src/** directory, rename file **configuration_template.h** to **configuration.h**. Edit file and set configuration values as described in the section below. Enable configuration by uncommenting *setConfigurationPreferences()* in the *setup()* method in **main.cpp** file. Configuration properties will then be persisted to nvram memory and will be used during startup.

Add the following values:

**UpdateInSeconds:** Interval in seconds for posting data to InfluxDB  
**WifiSSID:** SSID for wifi network  
**WifiPassword:** Wifi password  
**NtpServer:** Network Time Protocol server (like europe.pool.ntp.org)  
**InfluxDBHost:** Hostname or IP address of InfluxDB server  
**InfluxDBPort:** InfluxDB port (Default 8086)  
**InfluxDBDB:** Database name on InfluxDB server  
**IDBMeasure:** InfluxDB measurement name  
**PlantID:** ID for plant to identify measurement on InfluxDB  

![grafana](https://user-images.githubusercontent.com/24587666/119537556-6efad180-bd8a-11eb-8dee-9b082d36a78b.jpg)
![LILYGO-T-Higrow-1](https://user-images.githubusercontent.com/24587666/119539268-483d9a80-bd8c-11eb-9342-01e8fe1b8522.jpg)
![LILYGO-T-Higrow-2](https://user-images.githubusercontent.com/24587666/119539278-4a9ff480-bd8c-11eb-8715-5e3dae471080.jpg)
