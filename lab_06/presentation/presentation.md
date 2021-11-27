---
## Front matter
lang: ru-RU
title: Отчет по лабораторной работе №6
author: |
	Valery A. Dinkiev\inst{1}
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
date: 27 November 2021 Moscow,  Russia

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

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux. Проверить работу SELinx на практике совместно с веб-сервером Apache.

# Результаты выполненной работы

## Добавление параметра ServerName в файле httpd.conf

![Файл httpd.conf](image/1.png){ #fig:001 width=90% }

## Проверка установленного параметра с помощью браузера

![Проверка](image/4.png){ #fig:002 width=90% }

## Создание файла test.html

![Файл test.hmtl](image/9.png){ #fig:003 width=90% }

## Проверка контекста файла test.html 

![](image/10.png){ #fig:004 width=90% }

## Проверка созданного файла test.html

![](image/11.png){ #fig:005 width=90% }

## Проверка и смена контекста  файла test.html

![](image/12.png){ #fig:006 width=90% }

## Проверка файла test.html в браузере

![](image/13.png){ #fig:007 width=90% }

## Смена на прослушивание TCP порта 81

![](image/15.png){ #fig:008 width=90% }

## Добавление привязки http_port_t к 81 порту

![](image/20.png){ #fig:009 width=90% }

## Возвращение контекста httpd_sys_cоntent__t к файлу test.html

![](image/21.png){ #fig:010 width=90% }

## Проверка файла test.html в браузере

![](image/22.png){ #fig:011 width=90% }

## Смена на прослушивание TCP порта 80

![](image/23.png){ #fig:012 width=90% }

## Удаление привязки http_port_t к 81 порту

![](image/24.png){ #fig:013 width=90% }

## Удаление файла test.html

![](image/25.png){ #fig:014 width=90% }



# Выводы по работе

## Выводы

Развил навыки администрирования ОС Linux. Получил первое практическое знакомство с технологией SELinux. Проверил работу SELinx на практике совместно с веб-сервером Apache.


## {.standout}

Спасибо за внимание!
