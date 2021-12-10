---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №7"
subtitle: "Элементы криптографии. Однократное гаммирование"
author: "Динькиев Валерий"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
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
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the υalue makes tex try to haυe fewer lines in the paragraph.
  - \interlinepenalty=0 # υalue of the penalty (node) added after each line of a paragraph.
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
  - \usepackage{amsmath}
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Освоить на практике применение режима однократного гаммирования.

# Выполнение лабораторной работы

1. Для выполнения данной лабораторной работы использовал язык программирования Python. Написал функции для последующей работы. (рис. -@fig:001)
   Функция generate_key берет на вход размер строки (size) в виде целового числа  и строку символов с помощью которых мы будем генерировать ключ (в нашем случае мы будем использовать буквы английского алфавита и числа). А возвращает сгенерированный ключ в строковом формате (string).
   Функция hex_form берет на вход строку и возвращает её 16-ный вид данной строки.
   Функция gamming берет на вход строку и сгенерированный ключ. А возвращает зашифрованную строку методом однократного гаммирования.
   Функция unencrypt берет на вход шифрованную строку и ключ. А возвращает дешифрованную строку.
   Фунцкия open_text берет на вход шифрованную строку и исходную строку (которую мы введем вначале). А возврашает строку.

![Функции](image/1.png){ #fig:001 width=50% height=50% }

2. Использовал функции выше для определения новых переменных для дальнейшей работы. (рис. -@fig:002)
   Переменная input_string - это строка, которую мы вводим с клавиатуры. В нашем случае это строка "С Новым Годом, друзья!"
   Переменная gen_key - это сгенерированный ключ, который мы получили из функции generate_key.
   Переменная encrypted_string - это зашифрованная строка, которую мы получили из функции gamming.
   Переменная new_key - это новый ключ, которую мы получили из функции generate_key.
   Переменная unencrypted_key - это дешифрованный ключ, которую мы получили из функции unencrypt.
   Переменная input_key - это начальный ключ,  которую мы получили из функции open_text.
   Переменная unencrypted_input_key - это расшифрованный шифротекст.

![Переменные](image/2.png){ #fig:002 width=50% height=50% }

3. Выполняем первое задание. Для начала выводим зашифрованный текст, которые мы получили с помощью однократного гаммирования. (рис. -@fig:003)
 
![1 задание](image/3.png){ #fig:003 width=50% height=50% }

4. Выполняем второе задание. Выводим расшифрованный шифротекст. (рис. -@fig:004)

![2 задание](image/4.png){ #fig:004 width=50% height=50% }

# Выводы

Освоил на практике применение режима однократного гаммирования.