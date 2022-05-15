### 2022 05 15 Итерация 25

Изменен формат файлов описаний `README.md` - на мой взгляд так более удобочитабельнее

#### Интеграции
:arrow_right: Установлена [Reverso TTS / tts](https://github.com/rt400/ReversoTTS-HA)    
:arrow_right: Установлена [Ukraine Alarm](https://github.com/home-assistant/core/tree/dev/homeassistant/components/ukraine_alarm)    

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлен reversotts подробнее в [Блог. Home Assistant - Text to speech, озвучка уведомлений, Reverso TTS](https://youtu.be/bDdn7lRqAko)    

#### Пакаджи    
:arrow_right: [entity_reboot.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/entity_reboot.yaml) - продолжаются тесты, поэтому файл меняется    
:arrow_right: [da_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_hum.yaml) - доработка автоматизации увлажнения, чтобы не было лишних срабатываний    
:arrow_right: [dd_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_hum.yaml) - доработка автоматизации увлажнения, чтобы не было лишних срабатываний    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - проверял некоторые идеи, но в результате они не прижились, файл менялся, но по сути изменений нет    
  
#### Интерфейс, в режиме yaml    
Много косметических, незначительных изменений    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - страница телеметрии, добавлен раздел для медиа плееров, что сейчас играет    
:arrow_right: [05_lr_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_control.yaml) - тут также выведены карточки медиа плееров, см. скриншот    

Страница `05_lr_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0016.png)

____
### 2022 05 08 Итерация 24

#### Конфигурация    
:arrow_right: [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - закомментирован раздел updater - интеграция выпадала в ошибку    

#### Пакаджи    
:arrow_right: [entity_reboot.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/entity_reboot.yaml) - здесь будут собираться автоматизации по перезагрузке отдельных устройств, склонных к произвольному отключению    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - добавлены сенсоры для обновлений, подробнее в [Уроки Home Assistant - Телеметрия, часть 1. Отслеживание состояний в режиме онлайн](https://youtu.be/VuRrD-YYV70)    
:arrow_right: [bt_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_alarm.yaml) - добавлены описания сенсоров    
:arrow_right: [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлены описания сенсоров    
:arrow_right: [kn_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_alarm.yaml) - пакадж уведомлений при срабатывания датчика дыма и протечки в кухне    
:arrow_right: [kn_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_light.yaml) - пакадж, заготовка под управление освещением в кухне    
:arrow_right: [kn_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - добавлены описания сенсоров    

###### Интерфейс, в режиме yaml        
Много косметических, незначительных изменений    
:arrow_right: [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - страница телеметрии, добавлен раздел для обновлений    

Страница `02_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0015.png)

____
### 2022 05 05 Итерация 23

#### Интеграции
:arrow_right: Установлена [Reolink IP camera](https://github.com/fwestenberg/reolink_dev)    

#### Пакаджи    
:arrow_right: [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - перенос камер на платформе generic в UI    
:arrow_right: [cr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_CR/cr_light.yaml) - ручное управление освещением в коридоре    
:arrow_right: [cr_sensor.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_CR/cr_sensor.yaml) - описание сенсоров в коридоре    
:arrow_right: [en_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_camera.yaml) - несущественные изменения    
:arrow_right: [en_sensor.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_sensor.yaml) - описание сенсоров в прихожей    
:arrow_right: [en_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_switch.yaml) - описание свичей в прихожей    
:arrow_right: [system_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/system_sensors.yaml) - перенос сенсора filesize для home-assistant_v2.db в UI    
:arrow_right: [telemetry.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/telemetry.yaml) - добaвлен подсчет общего числа и недоступных камер    

#### Интерфейс, в режиме yaml    
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница для коридора    
* [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - страница телеметрии, добавлен раздел для камер - всего и недоступно    
* [03_cr_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/03_cr_control.yaml) - страница управления сущностями в коридоре    

Страница `03_cr_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0014.png)

____
### 2022 04 26 Итерация 22

#### Пакаджи    
:arrow_right: [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - добавлены IP камеры    
:arrow_right: [en_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_EN/en_camera.yaml) - пакадж отправки уведомлений и фото при открытии входной двери в [блоге](https://youtu.be/YxzUqcTerSE)    

#### Интерфейс, в режиме yaml    
:arrow_right: [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница для прихожей    
:arrow_right: [04_kn_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/01_en_control.yaml) - страница для прихожей и камеры на этаже, карточки для камер показаны в [блоге](https://youtu.be/YxzUqcTerSE)    

Страница `01_en_control.yaml`    
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0014.png)

____
### 2022 04 14 Итерация 21

#### Пакаджи    
:arrow_right: [lr_tv_control.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_tv_control.yaml) - управление телевизором через ИК базу Broadlink кнопок подробнее в [блоге](https://youtu.be/R2jMUh-5PCE)    

#### Интерфейс, в режиме yaml    
Добавление новых элементов на страницы комнат, ключевых изменений нет    

____
### Для удобства, чтобы не перегружать файл, старые итерации переносятся в архив    
:arrow_right_hook: [Архив 001-010](https://github.com/kvazis/newHA/blob/master/archive/001-010/README.md)    
:arrow_right_hook: [Архив 011-020](https://github.com/kvazis/newHA/blob/master/archive/011-020/README.md)    

____
### Как поддержать развитие проекта?
* [Стать спонсором моего Youtube](http://kvazis.link/sponsorship)
* [Подписаться на Patreon](http://kvazis.link/patreon)
* [Перевод через Paypal](http://kvazis.link/paypal)
* Webmoney - Z243592584952
* BTC - 1Gzr7WQugfnPuWVawu47EiCMTDUBqCAshj
* ETH - 0xa0ce3E29Cf537013649Ae9cdbc08C4853fF91FAc
* LTC - ltc1qs493yk2wk9ywx5h6aruk4p9zm75hx42ekv4ym2
* TRX - TFTCLqvS1tMBwokRHBwz1TCDJ4oD1Z5zPk