Создает конфиг версии RouterOS

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
