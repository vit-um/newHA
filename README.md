# Хроники Home Assistant часть 1

Аппаратная часть - Raspberry Pi 4B 8GB + Argon One M.2 + SSD 128 GB

Операционная система - RaspiOS x64 Lite, Debian 11 Bullseye

Установленные пакеты - jq wget curl udisks2 apparmor-utils libglib2.0-bin network-manager dbus

Дополнительно - git mc argonone-config

Home Assistant:

Адд-оны - File editor, Home Assistant Google Drive Backup, MariaDB, Mosquitto broker, Samba share, 2 x Zigbee2mqtt
Интеграции - HACS, MQTT, Raspberry Pi Power Supply Checker, Tuya, Version, Xiaomi Gateway 3, Xiaomi Miio, Yeelight, Локальный IP-адрес
Пакаджи - 
control_mode.yaml
Здесь реализован шаблонный выключатель с хранением состояния в MQTT, нужен для условий автоматизаций, используется при переключении управления с одного сервера на другой.
google_backup.yaml
Здесь созданы шаблонные сенсоры на основании значений атрибутов сенсора аддона Home Assistant Google Drive Backup
system_sensors.yaml
Системные сенсоры для мониторинга системы.
Интерфейс, в режиме yaml
ui-lovelace.yaml
Корневой файл, в нем содержится общий заголовок и ссылки на файлы, каждый файл - отдельная страница
lovelace/01_system.yaml
Первая страница интерфейса с мониторингом системы и данными о установленных аддонах -

![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0001.png)
