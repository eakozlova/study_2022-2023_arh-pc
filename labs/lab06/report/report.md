---
## Front matter
title: "Лабораторная работа №6"
subtitle: "по архитектуре компьютеров"
author: "Екатерина Алексеевна Козлова"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
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
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение практических навыков работы в Midnight Commander. Освоение инструкций языка ассемблера mov и int.

# Задание

Здесь приводится описание задания в соответствии с рекомендациями
методического пособия и выданным вариантом.

# Теоретическое введение


В табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно об Unix см. в [@gnu-doc:bash;@newham:2005:bash;@zarrelli:2017:bash;@robbins:2013:bash;@tannenbaum:arch-pc:ru;@tannenbaum:modern-os:ru].

# Выполнение лабораторной работы

Открываю Midnight Commander и при помощи клавиш перехожу в созданный ранее каталог ~/work/arch-pc. При помощи F7 создаю папку lab06 и перехожу в созданный каталог, дальше с помощью touch создаю файл lab6.asm. 

(рис. [-@fig:001]) [1](image/1){ #fig:001 width=70% }

Открываю этот файл клавишей F4в редакторе mcedit. 

(рис. [-@fig:001]) ![2](image/2){ #fig:002 width=70% }

Ввожу туда текст из листинга 6.1, файл сохраняю и закрываю. Просматриваю файл клавишей F3.

(рис. [-@fig:001]) ![3](image/3){ #fig:003 width=70% }

Оттрансирую текст программы файла в объектный файл, выполню компоновку и запущу исполняемый файл, проверяю действие. 

(рис. [-@fig:001]) ![4](image/4){ #fig:004 width=70% }

Скачиваю с ТУИС файл in_out.asm и переношу его клавишами в нужный мне каталог. 
Дальше создаю копию lab6-1.asm с именем lab6-2.asm и исправляю код в соответствии с листингом 6.2.
Создаю испольняемый файл и проверяю работу (теперь ввод программы осуществляется на одной строке, без переноса: заменила подпрограмму sprintLF на sprint).

(рис. [-@fig:001]) ![5](image/5){ #fig:004 width=70% }




# Выводы

Я приобрела практические навыки работы в Midnight Commander и освоила инструкций языка ассемблера mov и int.

# Список литературы{.unnumbered}

::: {#refs}
:::
