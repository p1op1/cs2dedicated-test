# CS2 Dedicated Server

## Материалы
1. [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD#Downloading_SteamCMD) — главный инструмент от разработчика для загрузки серверных файлов игр.
2. [LinuxGSM CS2](https://linuxgsm.com/servers/cs2server/) — комплексная программа для запуска нескольких серверов с функцией оповещения (telegram, discord и др.)
3. [LinuxGSM Документация](https://docs.linuxgsm.com/getting-started)

**2 GB Memory / 1 Intel vCPU / 70 GB Disk / NL / Debian 11**

```
dpkg --add-architecture i386;
apt update;
apt install curl wget file tar bzip2 gzip unzip bsdmainutils python3 util-linux ca-certificates binutils bc jq tmux netcat lib32gcc-s1 lib32stdc++6
```

```adduser cs2server```

```su - cs2server```

```wget -O linuxgsm.sh https://linuxgsm.sh && chmod +x linuxgsm.sh && bash linuxgsm.sh cs2server```

```./cs2server install```

```./cs2server start```

================================================================

# Цели и задачи

1. Наладить работу 1-го серверного приложения CS2
   - Изучить LinuxGSM (но можно использовать и свой вариант)
2. Реализовать обмен данными, логирование, отправку по таблицам значений из логов
3. Организовать хранение данных
   - Хранение на стороннем сервере с большим обьемом памяти
   - Бекапы
4. Мониторинг нагрузки систем
5. Добавить несколько серверных приложений на существующий сервер
   - Добавить другую серверную машину, установить туда сервера и подключить к общей базе
