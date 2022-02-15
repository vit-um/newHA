# 2022 02 15 _ 5

## Пакаджи 
* [dd_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - управление освещением, люстра Philips 620 (mihome) и zigbee лампа Aqara
* [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - добавлены сенсоры для термоголовок (climate), сенсоров и бинарных сенсоров

## Интерфейс, в режиме yaml
* [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - аналогично добавление объекты climate, sensor, bimnary sensor + карта вывода батареек с уровнем заряда менее 30% с цветным оформлением карты battery-state-card


# 2022 02 14 _ 4

## Пакаджи 
* [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - сенсоры определяющие общее количество объектов системе, активные, неактивные, недоcтупные, для доменов автоматизаций, скриптов, светильников и свичей

## Интерфейс, в режиме yaml
* [01_system.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml) - добавлен сенсор количества обновлений для HACS
* [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - добавлена карты для пакаджа telemetry - для каждого домена вывод значений в [multiple-entity-row](https://youtu.be/m8WkJv7M9CY) и перечень недоступных объектов в [auto-entities](https://youtu.be/cxDDZkOl-EM)

Страница 02_control.yaml Пример вывода в auto-entities недоступного светильника

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0003.png)

# 2022 02 13 _ 3

## Пакаджи 
* [control_mode.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml) - добавлен еще один шаблонный выключатель с хранением состояния в MQTT, для управлением режимом отопления
* [dd_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_heat.yaml) - управление термоголовкой TV01, описание в [видеоуроке](https://youtu.be/Y0bkyzhKHh8)

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница
* [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - заготовка под страницу телеметрии системы, добавлен переключатель режима отопления
* [07_dd_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_climate.yaml) - заготовка под страницу климат контроля одной из комнат, выведены параметры термостата из пакаджа dd_heat.yaml

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0002.png)

# 2022 02 13 _ 2
## Интеграции
* Установлена [Xiaomi MIoT](https://github.com/ha0y/xiaomi_miot_raw)

## Пакаджи 
* [google_backup.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/google_backup.yaml) - шаблонные сеноры переписаны в modern style

# 2022 02 13 _ 1

## Платформа
* Аппаратная часть - Raspberry Pi 4B 8GB + Argon One M.2 + SSD 128 GB
* Операционная система - RaspiOS x64 Lite, Debian 11 Bullseye
* Установленные пакеты - jq wget curl udisks2 apparmor-utils libglib2.0-bin network-manager dbus
* Дополнительно - git mc argonone-config

## Home Assistant:
* Адд-оны - File editor, Home Assistant Google Drive Backup, MariaDB, Mosquitto broker, Samba share, 2 x Zigbee2mqtt
* Интеграции - HACS, MQTT, Raspberry Pi Power Supply Checker, Tuya, Version, Xiaomi Gateway 3, Xiaomi Miio, Yeelight, Локальный IP-адрес

## Пакаджи 
* [control_mode.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml) - реализован шаблонный выключатель с хранением состояния в MQTT, нужен для условий автоматизаций, используется при переключении управления с одного сервера на другой
* [google_backup.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/google_backup.yaml) - созданы шаблонные сенсоры на основании значений атрибутов сенсора аддона Home Assistant Google Drive Backup
* [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - системные сенсоры для мониторинга системы

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница
* [01_system.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml) - первая страница интерфейса с мониторингом системы и данными о установленных аддонах

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0001.png)
