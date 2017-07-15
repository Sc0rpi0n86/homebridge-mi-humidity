# homebridge-mi-humidity

This is Xiaomi Mi Humidity plugin for [Homebridge](https://github.com/nfarina/homebridge). Since Apple Homekit is not supporting air purifier device yet, this plugin will add the air purifier as **Fan** to your Home app.


### Features

* Switch on / off.

* Control modes:

  - `Idle / Off`: Lift fan speed to 0% from Home app.

  - `Auto`: Lift fan speed between 1 - 60%.

  - `Silent`: Lift fan speed between 61 - 80%.

  - `Favorite / High`: Lift fan speed great than 80%.

    **Notes:** Alternatively, you can ask Siri to change the fan speed within the range to adjust the air purifier mode. Example:

    ```
    Hey Siri, change the air purifier speed to 100.
    ```

    ​

* Display temperature.

* Display humidity.

* Display air quality.

  ​

  ​



### Installation

1. Install required packages.

   ```
   npm install -g homebridge-mi-humidity miio
   ```

   ​

2. Add following accessory to the `config.json`.

   ```
     "accessories": [
       {
         "accessory": "MiHumidity",
         "name": "Humidity",
         "showTemperature": true,
         "showHumidity": true,
       }
     ]
   ```

   ​**Notes:** Set value for `showTemperature`, `showHumidity` to **true** or **false** to show or hide these sensors in Home app.

   ​

3. Restart Homebridge, and your Mi air purifier will be discovered automatically.



### License

See the [LICENSE](https://github.com/Sc0rpi0n86/homebridge-mi-humidity/blob/master/LICENSE) file for license rights and limitations (MIT).
