---
## Front matter
lang: ru-RU
title: Отчет по лабораторной работе №5
author: |
	Valery A. Dinkiev\inst{1}
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
date: 13 November 2021 Moscow,  Russia

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---
# Цель выполнения работы

## Цель работы

Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов. 
Получение практических навыков работы в консоли с дополнительными атрибутами. 
Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# Результаты выполненной работы

## Создание программы simpleid.c

![Программа simpleid.c](image/4.png){ #fig:001 width=90% }

## Создание программы simpleid.c

![Компиляция программы и проверка комадной id](image/5.png){ #fig:002 width=90% }

## SetUid-бит 

![](image/6.png){ #fig:003 width=90% }

![](image/7.png){ #fig:004 width=90% }

## Программа readfile.c 

![](image/8.png){ #fig:005 width=90% }

## Программа readfile.c 

![](image/10.png){ #fig:006 width=90% }

## Программа readfile.c 

![](image/9.png){ #fig:007 width=90% }

## Работа с файлом file01.txt от пользователя guest2 при наличии Sticky-бита  

![](image/14.png){ #fig:008 width=90% }

## Работа с файлом file01.txt от пользователя guest2 без Sticky-бита  

![](image/15.png){ #fig:009 width=90% }

![](image/16.png){ #fig:010 width=90% }

# Выводы по работе

## Выводы

Изучил механизмы изменения идентификаторов, применения SetUID- и Sticky-битов. Получил практические навыки работы в консоли с дополнительными атрибутами. 
Рассмотрел работу механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов


## {.standout}

Спасибо за внимание!
