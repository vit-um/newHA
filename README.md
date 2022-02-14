# 2022 02 14 _ 4

## Пакаджи 
* [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml)  - сенсоры определяющие общее количество объектов системе, активные, неактивные, недоcтупные, для доменов автоматизаций, скриптов, светильников и свичей

## Интерфейс, в режиме yaml
* [01_system.yaml - добавлен сенсор количества обновлений для HACS](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml)
* [02_control.yaml - добавлена карты для пакаджа telemetry - для каждого домена вывод значений в multiple-entity-row и перечень недоступных объектов в auto-entities](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml)

Страница 02_control.yaml Пример вывода в auto-entities недоступного светильника

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0003.png)

# 2022 02 13 _ 3

## Пакаджи 
* [control_mode.yaml - добавлен еще один шаблонный выключатель с хранением состояния в MQTT, для управлением режимом отопления](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml)
* [dd_heat.yaml - управление термоголовкой TV01](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_heat.yaml), описание в [видеоуроке](https://youtu.be/Y0bkyzhKHh8)

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml - корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml)
* [02_control.yaml - заготовка под страницу телеметрии системы, добавлен переключатель режима отопления](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml)
* [07_dd_climate.yaml - заготовка под страницу климат контроля одной из комнат, выведены параметры термостата из пакаджа dd_heat.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_climate.yaml)

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0002.png)

# 2022 02 13 _ 2
## Интеграции
* Установлена Xiaomi MIoT

## Пакаджи - шаблонные сеноры переписаны в modern style
* [includes/packages/google_backup.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/google_backup.yaml) 



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
* [control_mode.yaml - реализован шаблонный выключатель с хранением состояния в MQTT, нужен для условий автоматизаций, используется при переключении управления с одного сервера на другой](https://github.com/kvazis/newHA/blob/master/includes/packages/control_mode.yaml)
* [google_backup.yaml - созданы шаблонные сенсоры на основании значений атрибутов сенсора аддона Home Assistant Google Drive Backup](https://github.com/kvazis/newHA/blob/master/includes/packages/google_backup.yaml) 
* [system_sensors.yaml - системные сенсоры для мониторинга системы.](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml)

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml - корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml)
* [01_system.yaml - первая страница интерфейса с мониторингом системы и данными о установленных аддонах](https://github.com/kvazis/newHA/blob/master/lovelace/01_system.yaml)

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0001.png)
