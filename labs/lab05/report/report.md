---
## Front matter
title: "Лабораторная работа №5"
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

Освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Задание

Выполнить задания из самой лабораторной работы, а также задания для самостоятельной работы.

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

1. Программа Hello world!

Я создаю отдельный каталог для работы на языке ассемблера NASM с помощью mkdir и ключа -p.
Создаю текстовый файл с именем hello.asm с помощью touch и открываю его в gedit.
Ввожу данный в лабораторной работе текст, а затем компилирую его (превращаю в объектный код) использую nasm -f elf. 
Смотрю, что получилось и вижу файл hello.asm и файл hello.o с скомпилированным кодом. 
Дальше я компилирую исходный файл hello.asm в obj.o и смотрю созданные файлы, например, list.lst.

Проверю команды man nasm и nasm -hf для более подробной информации и получения списка форматов объектного файла. 

Для получения исполняемой программы передаю на обработку компоновщику объектный файл и проверяю создан ли файл hello.
С помощью ключа -о задаю файл main и проверяю.

Запускаю на выполнение созданный исполняемый файл с помощью ./hello
 
 2. Задания для самостоятельной работы
 
 Создаю в нужном каталоге копию файла hello.asm с именем lab5.asm и в текстовом редакторе изменяю текст на своё имя и фамилию.
 Оттранслирую текст в объектный файл и выполню компоновку объектного файла, запущу получившийся исполныемый файл.
 Дальше-скопирую файлы hello.asm и lab5.asm в мой локальный репозиторий и загружу файлы на Github. 
 
 (рис. [-@fig:001])

![Название рисунка](image/placeimg_800_600_tech.jpg){ #fig:001 width=70% }

# Выводы

Я освоила некоторые процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Список литературы{.unnumbered}

::: {#refs}
:::
