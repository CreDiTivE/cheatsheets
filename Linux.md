Linux
=====

Информация о системе
--------------------

*`free -m` количество оперативной памяти
* `df -h` количество места на жестком диске
* `lscpu` архитектура процессора
* `uptime` нагрузка системы за 1, 5, 15 минут

Выключение, запуск программ
---------------------------

* `shutdown -h now` выключение системы
* `restart` перезагрузка

Установка программ
------------------

### Установка шрифтов Microsoft

    sudo apt-get install msttcorefonts
    sudo fc-cache -fv

Назначение прав
---------------

* `find . -type f -exec chmod 644 \{\} \;` рекурсивная установка прав для файлов
* `find . -type d -exec chmod 755 \{\} \;` рекурсивная установка прав для каталогов

Программы
---------

* `which <программа>` узнать каталог в котором физически находится исполняемый файл программы

Работа с SSH
------------

* `ssh-keygen` создание публичного и приватного ключей
* `ssh-copy-id -i ~/.ssh/id_dsa.pub username@host` передача открытого ключа на другой компьютер

Работа с файлами
----------------

* `head <файл>` показать первые 10 строк файла
* `tail -n <кол-во строк> <файл>` показать последние 10 строк файла
* `less <файл>` построчное чтение файла с навигацией
* `cat <файл>` вывод содержимого файла
* `touch <файл>` создание пустого файла
* `file -i <файл>` узнать кодировку файла
* `recode CP1251 <файл>` сменить кодировку файла

### Проверка целостности файла

    md5sum <файл> > md5sum.txt
    md5sum -c md5sum.txt
