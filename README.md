# 2022 04 25 _ 19

## Пакаджи
* [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлен темплейт перевода давления ГПа в мм рт. ст, с проверкой на корректность данных
* [lr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light.yaml) - добавлены описания светильников
* [lr_switch_power.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_switch_power.yaml) - новый пакадж для реле и розеток, добавлены описания, запись показаний энергомониторинга

## Интерфейс, в режиме yaml
* [07_dd_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_control.yaml) - добавлены графики с датчика климата - температура, влажность, давление
* [02_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/02_control.yaml) - добавлены динамические карты, отображающие switch с потреблением более 10 Ватт, включенные светильники, таймеры

Страница 02_control.yaml
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0013.png)

# 2022 03 29 _ 18

## Пакаджи
* [dd_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_heat.yaml) - добавлена автоматизация которая при отключении режима отопления устанавливает на термоголовке t 15
* [da_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_heat.yaml) - аналогично
* [lr_heat_1.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_1.yaml) - аналогично
* [lr_heat_2.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_2.yaml) - аналогично
* [kn_heat.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_heat.yaml) - по шаблону добавлено управление последней, пятой термоголовкой
* [kn_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_sensors.yaml) - пакадж для сенсоров в кухне

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница управления для кухни - климат
* [04_kn_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/04_kn_climate.yaml) - страница климата и управление термостатом для кухни

Страница 04_kn_climate.yaml
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0012.png)

# 2022 03 28 _ 17

## Пакаджи
* [kn_boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_KN/kn_boiler.yaml) - пакадж управления вторым бойлером на кухне, в отличии от первого - он, при активации режима нагрева, работает в течении дня, схема немного проще.

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница управления для кухни - бойлер
* [04_kn_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/04_kn_control.yaml) - страница управления для кухни - бойлер

По остальным картинкам - косметические изменения. 


# 2022 03 26 _ 16

## Пакаджи
* [bt_alarm.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_alarm.yaml) - добавлены автоматизации по обнаружению протечки. уведомление в телеграм, голосом через шлюз Xiaomi, световая. после устранения - так же уведомление

## Интерфейс, в режиме yaml
* [06_bt_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/06_bt_control.yaml) - на страницу добавлены датчики протечек, немного изменен формат отображения данных


# 2022 03 25 _ 15

## Пакаджи

* [ip_camera.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/ip_camera.yaml) - добавлены камеры, rtsp потоки
* [da_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_light) - добавлены дополнительные автоматизации и сущности для освещения в детской А
* [da_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_switch.yaml) - добавлены новые описания switch 
* [lr_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_light.yaml) - пакадж для управления освещением в гостиной (начал перевод с старых серверов)

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница управления для гостиной
* [05_lr_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_control.yaml) - добавлены потолочные светильники для гостиной
* [08_da_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_control.yaml) - добавление новых сущностей на страницу управление, изменение шаблона (информация по zigbee датчикам)

Страница 08_da_control.yaml
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0011.png)

# 2022 03 23 _ 14

## Пакаджи
* [bt_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_sensors.yaml) - добавление описаний новых сенсоров
* [bt_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_light.yaml) - управление освещением, яркость в зависимости от времени суток, длительность работы таймера автоотключение в зависимости от времени и состояния двери
* [bt_vent.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/bt_vent.yaml) - управление вентиляцией, включение по превышению порога влажности, таймер автоотключения, условие на время работы

## Интерфейс, в режиме yaml
* [06_bt_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/06_bt_control.yaml) - страница для ванной комнаты, освещение, вентиляция, добавлен данные с сенсора климата

Страница 06_bt_control.yaml
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0010.png)

# 2022 03 21 _ 13

Не совсем корректно стал работать мой старый пакадж по управлению бойлером. Пришлось переписать, сразу на новом сервере.

## Пакаджи
* [boiler.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_BT/boiler.yaml) 

Бойлер можно включить только когда активирован режим нагрева бойлера - связка шаблонного выключателя и бинарного сенсора на платформе mqtt. Есть проверка на его состояние, если он отключен, то питание будет выключаться. В автоматическом режиме работает по часу утром и вечером - интервалы установлены в бинарных сенсорах платформы tod (time of day). Так же возможно ручное включение, для этого сделан еще один шаблонный switch - связанный с часовым таймером. После ручного включения бойлер также будет работать 1 час - по таймеру.

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлена страница ванной комнаты
* [06_bt_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/06_bt_control.yaml) - страница для ванной комнаты, управление бойлером. Для таймера применена карта flipdown-timer-card

## Конфигурация
* [configuration.yaml](https://github.com/kvazis/newHA/blob/master/configuration.yaml) - добавлена карта flipdown-timer-card

Страница 06_bt_control.yaml
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0009.png)


# 2022 02 24 _ 12

## Обновление которое планировалось на 24 февраля после выхода урока по голосовым уведомлениям. Война, развязанная россией против народа Украины - поменяла все планы. Фактическая дата публикации - 18 марта, на сегодняшний день я в порядке, как будет дальше - неизвестно, обстрелы ежедневно. 

## Пакаджи 
* [dd_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - добавление автоматизаций по управлению освещением
* [dd_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_switch.yaml) - добавлены новые сущности в customize, управление принтером
* [dd_hum.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_hum.yaml) - управление увлажнителем воздуха через реле выключателя с энергомониториноом,
* [da_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_light) - управление освещением
* [da_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_switch.yaml) - добавлены описания switch 
* [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавление описаний новых сенсоров
* [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - добавление описаний новых сенсоров
* [lr_air_quality.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_air_quality.yaml) - контроль и уведомления о качестве воздуха - CO2, [урок по голосовым уведомлениям](https://youtu.be/xKbEj7pE9iU)
* [lr_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_sensors.yaml) - добавление описаний новых сенсоров

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлены новые страницы
* [07_dd_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_control.yaml) - страница управления, добавлены новые сущности
* [08_da_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_control.yaml) - новая страница управления по шаблону
* [05_lr_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_climate.yaml) - добавление данных по CO2, изменени формат вывода

# 2022 02 21 _ 11

Перенес управление отоплением еще в одной комнате, суть таже, кроме того, что используются 2 одинаковые  термоголовки. За счет использования шаблонных пакаджей - перенос занимает до 5 минут. 

## Пакаджи 
* [lr_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_sensors.yaml) - сенсоры для климат контроля в гостиной
* [lr_heat_1.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_1.yaml) - управление термоголовкой TV01
* [lr_heat_2.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_LR/lr_heat_2.yaml) - управление термоголовкой TV01
* [dd_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_sensors.yaml) - добавлен сенсор освещенности, перенос switch в новый пакадж
* [da_sensors.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_sensors.yaml) - перенос switch в новый пакадж
* [dd_light.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_light.yaml) - добавлены иконки для светильников в секции customize
* [dd_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DD/dd_switch.yaml) - пакадж для switch - подбор шаблона для отображения сущностей розеток и реле
* [da_switch.yaml](https://github.com/kvazis/newHA/blob/master/includes/packages/Room_DA/da_switch.yaml) - пакадж для switch

## Интерфейс, в режиме yaml
* [ui-lovelace.yaml](https://github.com/kvazis/newHA/blob/master/ui-lovelace.yaml) - добавлены новые страницы
* [05_lr_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/05_lr_climate.yaml) - страница управления термоголовками и мониторинг датчика климата
* [07_dd_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_climate.yaml) - добавлен график по освещенности
* [07_dd_control.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/07_dd_control.yaml) - страница управления, добавлены светильники, розетка, несколько сенсоров (пока в поиске универсального шаблона)
* [08_da_climate.yaml](https://github.com/kvazis/newHA/blob/master/lovelace/08_da_climate.yaml) - косметические изменения

Страница 07_dd_control.yaml Вариант оформления страницы управления 
![screenshot](https://raw.githubusercontent.com/kvazis/newHA/master/img/0008.png)


# Для удобства, чтобы не перегружать файл, старые итерации переносятся в архив
* [Архив 001-010](https://github.com/kvazis/newHA/blob/master/archive/001-010/README.md)