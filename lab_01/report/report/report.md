---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №1"
subtitle: "Установка и конфигурация операционной системы на виртуальную машину"
author: "Динькиев Валерий"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=MiKTeX
romanfontoptions: Ligatures=MiKTeX
sansfontoptions: Ligatures=MiKTeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: xelatex
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

Приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для
дальнейшей работы сервисов.

# Задание

- Создать виртуальную машину
- Настроить виртуальную машину
- Проверить работу виртуальной машины
- Создать репозиторий на GitHub
- Выгрузить файлы на GitHub
- Сделать свой первый релиз на GitHub


# Выполнение лабораторной работы

1. Создал виртуальную машину (рис. -@fig:001)

![Создание VM](image/0.png){ #fig:001 width=90% }

![Созданная виртуальная машина](image/1.png){ #fig:002 width=90% }

2. Установил образ CentOS 7 на виртуальную машину (рис. -@fig:003)

![Установка образа](image/2.png){ #fig:003 width=90% }

3. Установил CentOS 7 (рис. -@fig:004)

![Установка CentOS 7](image/3.png){ #fig:004 width=90% }

4. Поставил root пароль и создал пользователя (рис. -@fig:005)

![Установка пароля и создание пользователя](image/4.png){ #fig:005 width=90% }

5. Подключил Ethernet и принял лицензию (рис. -@fig:006)

![Подключение Ethernet](image/6.png){ #fig:006 width=90% }

![Лицензия](image/7.png){ #fig:007 width=90% }

6. Успешно запустил систему (рис. -@fig:008)

![Пользователь vadinjkiev](image/8.png){ #fig:008 width=90% }

![Система запущена](image/9.png){ #fig:009 width=90% }

7. Создал репозиторий и выгрузил лабораторную на GitHub (рис. -@fig:010)

![Презентация и отчет на GitHub](image/10.png){ #fig:010 width=90% }

![коммит и пуш в Git](image/11.png){ #fig:011 width=90% }

# Выводы

Приобрел практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для
дальнейшей работы сервисов.
