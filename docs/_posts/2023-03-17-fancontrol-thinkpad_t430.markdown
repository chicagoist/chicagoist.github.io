---
layout: post
title:  "Задолбался с перегревом ноутбука"
date:   2023-03-17
categories: post posts
---
![Signature](/favicon.ico)

После обновления Ubuntu на ноутбуке ThinkPad T430 начал получать жесткий
перегрев с выключением ноута. Пришлось разобраться с мануальными настрой-
ками управления куллера. Помогла статья с Gentoo Wiki:

1.[ThinkPad T430-fancontrol]: https://wiki.gentoo.org/wiki/Fan_speed_control/lm_sensors%27_fancontrol
2.[ThinkPad T430-Gentoo Wiki]: https://wiki.gentoo.org/wiki/Lenovo_Thinkpad_T430

С настройками утилиты thinkfan вообще не было проблем в автоматическом 
режиме, а вот fancontrol пришлось настраивать вручную, используя утилиту 
lm_sensor, поэтому решил забекапить тут настройки конфигов для данной 
модели ноутбука на будущее.

FILE /etc/thinkfan.conf
{% highlight bash %}

hwmon /sys/class/hwmon/hwmon0/subsystem/hwmon1/temp1_input
hwmon /sys/class/hwmon/hwmon0/subsystem/hwmon3/temp1_input
hwmon /sys/class/hwmon/hwmon0/subsystem/hwmon3/temp2_input
hwmon /sys/class/hwmon/hwmon0/subsystem/hwmon3/temp3_input
hwmon /sys/class/hwmon/hwmon0/subsystem/hwmon4/temp1_input
hwmon /sys/class/hwmon/hwmon0/subsystem/hwmon4/temp2_input
hwmon /sys/class/hwmon/hwmon0/subsystem/hwmon4/temp3_input

tp_fan /proc/acpi/ibm/fan

(0, 0,  55)
(1, 53, 60)
(2, 58, 65)
(3, 63, 70)
(4, 68, 75)
(5, 73, 80)
(6, 78, 85)
(7, 83, 90)
(127, 88, 32767)

{% endhighlight %}




