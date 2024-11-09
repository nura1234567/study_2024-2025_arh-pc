---
## Front matter
title: "Лабораторная работа № 5"
subtitle: "Основы работы с Midnight Commander (mc). Структура программы на языке ассемблера NASM. Системные вызовы в ОС GNU Linux"
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

lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение практических навыков работы в Midnight Commander. Освоение инструкций
языка ассемблера mov и int.

# Выполнение лабораторной работы

1) С помощью команды mc я открыла Midnight Commander.

![Окно Midnight Commander](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image001.jpg){#fig:001 width=70%}

2) Используя клавиши перемещения курсора перешла в каталог ~/work/arch-pc созданный
при выполнении лабораторной работы No4

![Окно Midnight Commander. Переход в каталог](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image002.jpg){#fig:002 width=70%}

3) С помощью функциональной клавиши F7 создала каталог lab05

![Окно Midnight Commander. Создание каталога](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image003.jpg){#fig:003 width=70%}

 и перешла в созданный каталог lab05.
![Окно Midnight Commander. Переход в каталог](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image004.jpg){#fig:004 width=70%}

4) Пользуясь строкой ввода и командой touch создала файл lab5-1.asm

![Окно Midnight Commander. Создание файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image005.jpg){#fig:005 width=70%}

5) С помощью функциональной клавиши F4 открыла файл lab5-1.asm для редактирования во встроенном редакторе и ввела в него код программы.

![Текст в файле lab5-1.asm](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image007.jpg){#fig:007 width=70%}

6) С помощью функциональной клавиши F3 открыла файл lab5-1.asm для просмотра и убедилась, что файл содержит текст программы.

![Текст в файле lab5-1.asm. Проверка клавишей F3](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image009.jpg){#fig:009 width=70%}

7) Оттранслировала текст программы lab5-1.asm в объектный файл. Выполнила компоновку объектного файла, запустила получившийся исполняемый файл.
Программа вывела "Введите строку", ввела свое ФИО - Карцова Анна Сергеевна

![Программа lab5-1](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image010.jpg){#fig:010 width=70%}

8) С помощью функциональной клавиши F5 создала копию файла lab5-1.asm с именем lab5-2.asm.

![Создание файла lab5-2.asm](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image011.jpg){#fig:011 width=70%}

9) Cкачала файл in_out.asm с ТУИС и перенесла в каталог lab05. Исправила текст программы в файле lab5-2.asm с использование подпрограмм из внешнего файла in_out.asm.

![Файл lab5-2 с изменениями](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image012.jpg){#fig:012 width=70%}

10) Создала исполняемый файл и проверила его.

![Программа lab5-2](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image013.jpg){#fig:013 width=70%}

11) В файле lab5-2.asm заменила подпрограмму sprintLF на sprint. Создала исполняемый файл и проверила его работу. Разница между sprintLF и sprint в том, что при использовании sprintLF мы вводим текст на другой строке, а при использовании sprint - на той же, где и текст запроса.

![Файл lab5-2 с изменениями](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image014.jpg){#fig:014 width=70%}

![Проверка программы lab5-2 с изменениями](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image015.jpg){#fig:015 width=70%}


# Самостоятельная работы

1) Создала копию файла lab5-1.asm, назвала ее lab5-3.asm. Внесла изменения в программу, так чтобы после приглашения “Введите строку:” строка вводилась с клавиатуры и затем выводилась на экран.

![Создание файла lab5-3](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image016.jpg){#fig:016 width=70%}

2) Создала исполняемый файл lab5-3 и проверила его работу.
![Проверка программы lab5-3](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image017.jpg){#fig:017 width=70%}

3) Создала копию файла lab5-2.asm, назвала ее lab5-4.asm. Внесла изменения в программу, так чтобы после приглашения “Введите строку:” строка вводилась с клавиатуры и затем выводилась на экран.

![Создание файла lab5-4](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image018.jpg){#fig:018 width=70%}

4) Создала исполняемый файл lab5-4 и проверила его работу.
![Проверка программы lab5-4](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image019.jpg){#fig:019 width=70%}

5) Я загрузила файлы на Github.

![Проверка программы lab5-4](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab05/report/image/image020.jpg){#fig:020 width=70%}


# Выводы
Я приобрела практические навыки работы с Midnight Commander и освоила инструкции языка ассемблера mov и int.



