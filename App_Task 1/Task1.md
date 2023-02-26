# Задание 1

1)   Используйте команды операционной системы Linux и создайте две новых директории – «Игрушки для школьников» и «Игрушки для дошколят»
2)   Создайте в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»
3)   Создайте в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»
4)   Объединить 2 директории в одну «Имя Игрушки»
5)   Переименовать директорию «Имя Игрушки» в «Игрушки»
6)   Просмотреть содержимое каталога «Игрушки».
7)   Установить и удалить snap-пакет. (Любой, какой хотите)
8)   Добавить произвольную задачу для выполнения каждые 3 минуты (Например, запись в текстовый файл чего-то или копирование из каталога А в каталог Б).

================================================================
```bash
┌────────────────────────────────────────────────────────────────────┐
│                        • MobaXterm 20.6 •                          │
│            (SSH client, X-server and networking tools)             │
│                                                                    │
│ ➤ SSH session to grafany@192.168.100.15                            │
│   • SSH compression : ✔                                            │
│   • SSH-browser     : ✔                                            │
│   • X11-forwarding  : ✔  (remote display is forwarded through SSH) │
│   • DISPLAY         : ✔  (automatically set on remote server)      │
│                                                                    │
│ ➤ For more info, ctrl+click on help or visit our website          │
└────────────────────────────────────────────────────────────────────┘

Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.19.0-32-generic x86_64)

* Documentation:  https://help.ubuntu.com
* Management:     https://landscape.canonical.com
* Support:        https://ubuntu.com/advantage

* Introducing Expanded Security Maintenance for Applications.
  Receive updates to over 25,000 software packages with your
  Ubuntu Pro subscription. Free for personal use.

  https://ubuntu.com/pro

Расширенное поддержание безопасности (ESM) для Applications выключено.

0 обновлений может быть применено немедленно.

1 дополнительное обновление безопасности может быть применено с помощью ESM Apps                                                                                                         .
Подробнее о включении службы ESM Apps at https://ubuntu.com/esm

Last login: Sun Feb 26 10:51:41 2023 from 192.168.100.5

# 1)   Используйте команды операционной системы Linux и создайте две новых директории – «Игрушки для школьников» и «Игрушки для дошколят»

grafany@grafany-linux:~/devel$ mkdir Игрушки_для_школьников
grafany@grafany-linux:~/devel$ mkdir Игрушки_для_дошколят
grafany@grafany-linux:~/devel$ ls -l
итого 8
drwxrwxr-x 2 grafany grafany 4096 лют 26 11:58 Игрушки_для_дошколят
drwxrwxr-x 2 grafany grafany 4096 лют 26 11:57 Игрушки_для_школьников

# 2)   Создайте в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»

grafany@grafany-linux:~/devel$ cd Игрушки_для_школьников/
grafany@grafany-linux:~/devel/Игрушки_для_школьников$ ll
итого 8
drwxrwxr-x 2 grafany grafany 4096 лют 26 11:57 ./
drwxrwxr-x 4 grafany grafany 4096 лют 26 11:58 ../
grafany@grafany-linux:~/devel/Игрушки_для_школьников$
grafany@grafany-linux:~/devel/Игрушки_для_школьников$ cat > Роботы
Роботы
grafany@grafany-linux:~/devel/Игрушки_для_школьников$
grafany@grafany-linux:~/devel/Игрушки_для_школьников$ echo "Конструктор" > Конструктор
grafany@grafany-linux:~/devel/Игрушки_для_школьников$ cat > Настольные_игры
Настольные игрыgrafany@grafany-linux:~/devel/Игрушки_для_школьников$
grafany@grafany-linux:~/devel/Игрушки_для_школьников$ ll
итого 20
drwxrwxr-x 2 grafany grafany 4096 лют 26 12:31 ./
drwxrwxr-x 4 grafany grafany 4096 лют 26 11:58 ../
-rw-rw-r-- 1 grafany grafany   23 лют 26 12:28 Конструктор
-rw-rw-r-- 1 grafany grafany   29 лют 26 12:31 Настольные_игры
-rw-rw-r-- 1 grafany grafany   13 лют 26 12:04 Роботы
grafany@grafany-linux:~/devel/Игрушки_для_школьников$
grafany@grafany-linux:~/devel/Игрушки_для_школьников$ cd ..
grafany@grafany-linux:~/devel$ ll
итого 16
drwxrwxr-x  4 grafany grafany 4096 лют 26 11:58 ./
drwxr-x--- 23 grafany grafany 4096 лют 26 11:56 ../
drwxrwxr-x  2 grafany grafany 4096 лют 26 11:58 Игрушки_для_дошколят/
drwxrwxr-x  2 grafany grafany 4096 лют 26 12:31 Игрушки_для_школьников/

# 3)   Создайте в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»

grafany@grafany-linux:~/devel$ cd Игрушки_для_дошколят/
grafany@grafany-linux:~/devel/Игрушки_для_дошколят$ touch Мягкие_игрушки Куклы Машинки
grafany@grafany-linux:~/devel/Игрушки_для_дошколят$ ls
Куклы  Машинки  Мягкие_игрушки
grafany@grafany-linux:~/devel/Игрушки_для_дошколят$ cd ..
grafany@grafany-linux:~/devel$ ls
Игрушки_для_дошколят  Игрушки_для_школьников
grafany@grafany-linux:~/devel$ mkdir Имя_Игрушки
grafany@grafany-linux:~/devel$ tree
.
├── Игрушки_для_дошколят
│   ├── Куклы
│   ├── Машинки
│   └── Мягкие_игрушки
├── Игрушки_для_школьников
│   ├── Конструктор
│   ├── Настольные_игры
│   └── Роботы
└── Имя_Игрушки

3 directories, 6 files

# 4)   Объединить 2 директории в одну «Имя Игрушки»


grafany@grafany-linux:~/devel$ mv Игрушки_для_дошколят/   Игрушки_для_школьников/ Имя_Игрушки/
grafany@grafany-linux:~/devel$ ls
Имя_Игрушки
grafany@grafany-linux:~/devel$ tree
.
└── Имя_Игрушки
├── Игрушки_для_дошколят
│   ├── Куклы
│   ├── Машинки
│   └── Мягкие_игрушки
└── Игрушки_для_школьников
├── Конструктор
├── Настольные_игры
└── Роботы

3 directories, 6 files

# 5)   Переименовать директорию «Имя Игрушки» в «Игрушки»


grafany@grafany-linux:~/devel$ mv Имя_Игрушки/ Игрушки

# 6)   Просмотреть содержимое каталога «Игрушки».

grafany@grafany-linux:~/devel$ tree -g
[grafany ]  .
└── [grafany ]  Игрушки
├── [grafany ]  Игрушки_для_дошколят
│   ├── [grafany ]  Куклы
│   ├── [grafany ]  Машинки
│   └── [grafany ]  Мягкие_игрушки
└── [grafany ]  Игрушки_для_школьников
├── [grafany ]  Конструктор
├── [grafany ]  Настольные_игры
└── [grafany ]  Роботы

3 directories, 6 files

# 7)   Установить и удалить snap-пакет. (Любой, какой хотите)

grafany@grafany-linux:~/devel$ sudo snap find
Поисковый запрос пуст. Но имеются некоторые snap-пакеты, которые могут вас заинтересовать:

Название     Версия                            Издатель               Примечание  Описание
jami         20230130.1037.1b9159ac            sfljami                -           Privacy-oriented voice, video, chat, and conference platform and SIP phone
krita        5.1.1                             krita✓                 -           Digital Painting, Creative Freedom
thunderbird  102.8.0-2                         canonical✓             -           Mozilla Thunderbird email application
notepadqq    1.4.8                             danieleds              -           A Notepad++-like editor for Linux.
postman      10.10.9                           postman-inc✓           -           API Development Environment
mailspring   1.10.8                            foundry376✓            -           The best email app for people and teams at work
spotify      1.1.84.716.gc5f8b819              spotify✓               -           Music for everyone
slack        4.29.149                          slack✓                 -           Team communication for the 21st century.
foobar2000   1.6.16                            mmtrt                  -           foobar2000 is an advanced freeware audio player.
gimp         2.10.30                           snapcrafters           -           GNU Image Manipulation Program
hugo         0.110.0                           hugo-authors           -           Fast and Flexible Static Site Generator
inkscape     1.2.2-732a01da63-2022-12-09-cust  inkscape✓              -           Vector Graphics Editor
juju         2.9.38                            canonical✓             classic     Juju - a model-driven operator lifecycle manager for K8s and machines
skype        8.94.0.426                        skype✓                 -           One Skype for all your devices. New features. New look. All Skype.
litteris     master                            raibtoffoletto         -           Penpal Correspondence Organized
musescore    3.6.2                             musescore✓             -           Create, play and print beautiful sheet music.
newsboat     r2.30.1                           minoru                 -           An RSS/Atom feed reader for text terminals
qownnotes    23.2.5                            pbek                   -           Plain-text file markdown note taking with Nextcloud/ownCloud integration
retroarch    1.14.0                            libretro               -           RetroArch is the official reference frontend for the libretro API.
audacity     3.1.3                             diddledani✪            -           Audio software for multi-track recording and editing
bitwarden    2023.2.0                          bitwarden✓             -           Bitwarden
obs-studio   27.1.3                            snapcrafters           -           Free and open source software for live streaming and screen recording
gitkraken    9.1.1                             gitkraken✓             classic     For repo management, in-app code editing & issue tracking.
keepassxc    2.7.4                             keepassxreboot         -           Community-driven port of the Windows application “KeePass Password Safe”
vlc          3.0.18                            videolan✓              -           The ultimate media player
powershell   7.3.2                             microsoft-powershell✓  classic     PowerShell for every system!

Введите поисковый запрос так, чтобы результаты поиска были наиболее точны.
grafany@grafany-linux:~/devel$ snap info powershell
name:      powershell
summary:   PowerShell for every system!
publisher: Microsoft PowerShell✓
store-url: https://snapcraft.io/powershell
contact:   https://github.com/powershell/powershell
license:   MIT
description: |
PowerShell is an automation and configuration management platform.
It consists of a cross-platform (Windows, Linux, and macOS)
command-line shell and associated scripting language.

See https://docs.microsoft.com/powershell/scripting/powershell-support-lifecycle for support
details.
snap-id: JSNnoJl3EqkMuWoy5Dgq8PMqZ0uNcpie
channels:
latest/stable:    7.3.2 2023-01-25 (229) 74MB classic
latest/candidate: ↑
latest/beta:      ↑
latest/edge:      ↑
lts/stable:       7.2.9 2023-01-25 (228) 72MB classic
lts/candidate:    7.2.8 2022-12-13 (227) 71MB classic
lts/beta:         7.2.8 2022-12-13 (227) 71MB classic
lts/edge:         7.2.8 2022-12-13 (227) 71MB classic
grafany@grafany-linux:~/devel$ sudo snap install powershell
ошибка: This revision of snap "powershell" was published using classic confinement and thus
may perform arbitrary system changes outside of the security sandbox that snaps are
usually confined to, which may put your system at risk.

              If you understand and want to proceed repeat the command including --classic.
grafany@grafany-linux:~/devel$ sudo snap install powershell --classic
powershell 7.3.2 от Microsoft PowerShell✓ установлен
grafany@grafany-linux:~/devel$ sudo snap remove powershell
powershell удалён
grafany@grafany-linux:~/devel$

# 8)   Добавить произвольную задачу для выполнения каждые 3 минуты (Например, запись в текстовый файл чего-то или копирование из каталога А в каталог Б).

grafany@grafany-linux:~/devel$ nano script.sh
grafany@grafany-linux:~/devel$ touch testcron.log
grafany@grafany-linux:~/devel$ ls
script.sh  testcron.log  Игрушки
grafany@grafany-linux:~/devel$ tail script.sh
#!/bin/bash
echo $(date) >> /home/grafany/devel/testcron.log
grafany@grafany-linux:~/devel$ ll
итого 16
drwxrwxr-x  3 grafany grafany 4096 лют 26 13:21 ./
drwxr-x--- 23 grafany grafany 4096 лют 26 11:56 ../
-rw-rw-r--  1 grafany grafany   61 лют 26 13:21 script.sh
-rw-rw-r--  1 grafany grafany    0 лют 26 13:21 testcron.log
drwxrwxr-x  4 grafany grafany 4096 лют 26 12:48 Игрушки/
grafany@grafany-linux:~/devel$ sudo chmod ugo+x /home/grafany/devel/script.sh
[sudo] пароль для grafany:
grafany@grafany-linux:~/devel$ ll
итого 16
drwxrwxr-x  3 grafany grafany 4096 лют 26 13:21 ./
drwxr-x--- 23 grafany grafany 4096 лют 26 11:56 ../
-rwxrwxr-x  1 grafany grafany   61 лют 26 13:21 script.sh*
-rw-rw-r--  1 grafany grafany    0 лют 26 13:21 testcron.log
drwxrwxr-x  4 grafany grafany 4096 лют 26 12:48 Игрушки/
grafany@grafany-linux:~/devel$ crontab -e
crontab: installing new crontab
grafany@grafany-linux:~/devel$ sudo cat /var/log/syslog | grep CRON
Feb 26 11:09:01 grafany-linux CRON[40210]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
Feb 26 11:17:01 grafany-linux CRON[40299]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)
Feb 26 11:30:01 grafany-linux CRON[40307]: (root) CMD ([ -x /etc/init.d/anacron ] && if [ ! -d /run/systemd/system ]; then /usr/sbin/invoke-rc.d anacron start >/dev/null; fi)
Feb 26 11:33:14 grafany-linux cron[755]: (CRON) INFO (pidfile fd = 3)
Feb 26 11:33:14 grafany-linux cron[755]: (CRON) INFO (Running @reboot jobs)
Feb 26 11:39:01 grafany-linux CRON[2198]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
Feb 26 12:09:01 grafany-linux CRON[4469]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
Feb 26 12:17:01 grafany-linux CRON[4539]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)
Feb 26 12:30:01 grafany-linux CRON[4546]: (root) CMD ([ -x /etc/init.d/anacron ] && if [ ! -d /run/systemd/system ]; then /usr/sbin/invoke-rc.d anacron start >/dev/null; fi)
Feb 26 12:39:01 grafany-linux CRON[4612]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
Feb 26 13:09:01 grafany-linux CRON[4762]: (root) CMD (  [ -x /usr/lib/php/sessionclean ] && if [ ! -d /run/systemd/system ]; then /usr/lib/php/sessionclean; fi)
Feb 26 13:17:01 grafany-linux CRON[5080]: (root) CMD (   cd / && run-parts --report /etc/cron.hourly)
Feb 26 13:30:01 grafany-linux CRON[5192]: (root) CMD ([ -x /etc/init.d/anacron ] && if [ ! -d /run/systemd/system ]; then /usr/sbin/invoke-rc.d anacron start >/dev/null; fi)
Feb 26 13:33:01 grafany-linux CRON[5272]: (grafany) CMD (/home/grafany/devel/script.sh)
grafany@grafany-linux:~/devel$ tail /home/grafany/devel/testcron.log
Няд 26 лют 2023 13:33:01 +03
Няд 26 лют 2023 13:36:01 +03
Няд 26 лют 2023 13:39:01 +03
Няд 26 лют 2023 13:42:01 +03

grafany@grafany-linux:~/devel$
```
