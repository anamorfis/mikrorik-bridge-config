# О сервисе
Ансибл плейбук создает конфиги радимоста мастер-слейв версии RouterOS 6.46 и конфиги для мониторинга в nagios.


Конфиги храятся в путях `./config/mikrotik` и `./config/nagios`

# Настройки
`vars.yml` редактируются переменные в которых указываются необходимые параметры для работы радиомоста:

```
- { frequency: 5825, ssid: test_wireless, master_ip: 172.16.31.1, slave_ip: 172.16.31.2, gateway: 172.16.31.13, nv2_security: nv2pass1234, wpa2_key: wpa2pass1234 }
```

Переменная | Описание 
:---:| :--- 
**frequency** | частота на которой будет работать радиомост
**ssid** | имя радиомоста
**master_ip** | IP-адрес мастер станции
**slave_ip** | IP-адрес слейв станции
**gateway** | маршрут по-умолчанию
**nv2_security** | пароль от nv2
**wpa2_key** | пароль в шифровании wpa2


# Использование
Для максимально быстрой и без проблемной  настройки использую `netinstall` c офф. сайта https://mikrotik.com/download. Оттуда же скачать прошивку и сохранить в одной директории с `netinstall`. 

В запущенном `netinstall` нажать `Net booting`, отметить `Boot Server enabled` и в `Client IP address` прописать например `192.168.88.1`. В системе назначить адрес из этой же подсети, например `192.168.88.2/24`.


На микротик подается питание с заранее зажатой кнопкой `reset`, отпускается, как только перестанет мигать индикатор `user led`. 


В поле `Routers/Drivers` увидим загруженный микротик, отмечаем его и отмечаем `Configure script` правее в поле указываем путь до скрипта. 

Затем нажимаем кнопку `Install`, микрот форматируется, прошивается и настраивается автоматически по скрипту. 


Пароля по умолчанию для входа нет, необходимо задать самостоятельно после проверки работоспособности конфигурации радиомоста.
