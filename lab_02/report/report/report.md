---
# Front matter
title: "Отчет по лабораторной работе 1"
subtitle: "Дискреционное разграничение прав в Linux. Основные атрибуты"
author: "Динькиев Валерий"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---


# Цель работы

Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах 
с открытым кодом на базе ОС Linux.


# Выполнение лабораторной работы

1. В установленной при выполнении предыдущей лабораторной работы
операционной системе создал учётную запись пользователя guest (использую учётную запись администратора) (рис. -@fig:001)

![Создание учетной записи пользователя guest](image/0.png){ #fig:001 width=90% }


2. Задал  пароль для пользователя guest (использую учётную запись администратора) (рис. -@fig:002)

![Пароль](image/1.png){ #fig:002 width=90% }

3. Вошел в систему от имени пользователя guest 
4. Поставил root пароль и создал пользователя 
5. Уточнил имя вашего пользователя командой whoami (рис. -@fig:003)

![Пользователь guest](image/2.png){ #fig:003 width=90% }

6. Уточнил имя пользователя, его группу, а также группы, куда входит пользователь, командой id. Запомнил выведенные значения uid, gid и др. Сравнил вывод id с выводом команды groups (они совпадают). (рис. -@fig:004)

![Уточнение имени пользователя](image/3.png){ #fig:004 width=90% }

7. Сравнил полученную информацию об имени пользователя с данными,выводимыми в приглашении командной строки. 
   Полученная информация более подробно описывает пользователя (его uid..) а приглашение командной строки только имя пользователя и его домен.

8. Просмотрел файл /etc/passwd командой cat /etc/passwd. Нашел в нем учетную запись. Определил uid, gid пользователя. 
   Найденные значения совпадают со значения в прошлых пунктах (рис. -@fig:005)

![Содержимое файла /etc/passwd](image/4.png){ #fig:005 width=90% }

9. Определил существующие в системе директории командой ls -l /home/. Удалось получить список поддиректорий директории /home. 
   Права установлены так, чтобы только пользователь мог читать и писать в этот каталог (полные права только у пользователя данной директории). (рис. -@fig:006)
 
![Существующие директории](image/5.png){ #fig:006 width=90% }

10. Проверил, какие расширенные атрибуты установлены на поддиректориях, находящихся в директории /home, командой lsattr /home 
    Удалось только увидеть расширенные атрибуты директории guest
    Расширенные атрибуты других директорий мне не удалось увидеть. (рис. -@fig:007)

![Расширенные атрибуты](image/7.png){ #fig:007 width=90% }

11. Создал в домашней директории поддиректорию dir1 (рис. -@fig:008)
    Определил командами ls -l и lsattr, какие права доступа и расширенные атрибуты были выставлены на директорию dir1.(рис. -@fig:009)

![Создание поддиректории](image/8.png){ #fig:008 width=90% }

![Права доступа и расширенные атрибуты](image/9.png){ #fig:009 width=90% }

12. Снял с директории dir1 все атрибуты командой chmod 000 dirl и проверил с её помощью правильность выполнения команды (рис. -@fig:010)

![Создание поддиректории](image/10.png){ #fig:010 width=90% }

13. Попытался создать в директории dir1 файл file1 (рис. -@fig:011)
    Получаю отказ в создании файла, потому что в прошлом пункте снял с директории все атрибуты
    Сообщение об ошибки никак не отразилось на создании файла, потому что файл не создался в данной директории
    Проверил командой ls -l /home/guest/dir1 действительно ли файл file1 не находится внутри директории dir1, но проверить не получилось из-за прав доступа к файлам директории. (рис. -@fig:012)

![Попытка создания](image/11.png){ #fig:011 width=90% }

![Проверка командой](image/12.png){ #fig:012 width=90% }

14. Заполнил таблицу «Установленные права и разрешённые действия», выполняя действия от имени владельца директории (файлов), определив опытным путём, какие операции разрешены, а какие нет.
    Если операция разрешена, занес в таблицу знак «+», если не разрешена, знак «-». (рис. -@fig:013)
	
![Таблица прав](image/13.png){ #fig:013 width=90% }

![Таблица прав](image/14.png){ #fig:014 width=90% }

![Таблица прав](image/15.png){ #fig:015 width=90% }

15. На основании заполненной таблицы определите те или иные минимально необходимые права для выполнения операций внутри директории
    dir1 (рис. -@fig:016)

![Минимальные права для совершения операций](image/16.png){ #fig:016 width=90% }

# Выводы

Получил практические навыков работы в консоли с атрибутами файлов, закрепил теоретические основ дискреционного разграничения доступа в современных системах 
с открытым кодом на базе ОС Linux.

