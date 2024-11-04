---
## Front matter
title: "Лабораторная работа № 3"
subtitle: "Язык разметки Markdown"
author: "Карцова Анна Сергеевна"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Целью работы является освоение процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.


# Выполнение лабораторной работы

2.1. Я открыла терминал на домашнем компьютере.

2.2. Перешла в каталог курса сформированный при выполнении лабораторной работы No2. Обновила локальный репозиторий, скачав изменения из удаленного репозитория.

![Обновление репозитория](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image01.jpg){#fig:001 width=120%}

2.3. Перешла в каталог с шаблоном отчета по лабораторной работе № 3. Провела компиляцию шаблона, используя команду make.

![Компиляция шаблона командой make](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image02.jpg){#fig:002 width=120%}

Удалила полученные файлы командой make clean.

![Удаление командой make clean](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image03.jpg){#fig:003 width=120%}

Проверила, что файлы после применения команды make clean файлы report.pdf и report.docx были удален.

![Проверка удаления файлов](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image04.jpg){#fig:004 width=120%}

Открыла файл report.md с помощью текстого редактора.

![Открытие файла текстовым редактором](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image05.jpg){#fig:005 width=120%}

Изучила структуру открытого файла.

![Шаблон файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image06.jpg){#fig:006 width=120%}

Заполнила отчет по лабораторной работе.

![Титульная страница отчета](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image07.jpg){#fig:007 width=120%}

Основной отчет.

![Отчет](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab03/report/image/image08.jpg){#fig:008 width=120%}




# Выводы

Здесь кратко описываются итоги проделанной работы.


