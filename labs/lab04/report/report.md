---
## Front matter
title: "Лабораторная работа № 4"

subtitle: "*Создание и процесс обработки программ на языке ассемблера NASM*"

author: "**Карцова Анна**"

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

Освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Выполнение лабораторной работы

Создаю каталог lab04 для работы с программами на языке ассемблера NASM и перехожу в этот каталог. 

![Создание каталога и переход в него](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image001.jpg){#fig:001 width=100%}




Создаю текстовый файл с именем hello.asm. Открываю его с использованием текстового редактора gedit

![Создание и открытие файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image002.jpg){#fig:002 width=100%}


ввожу текст

![Текстовый файл](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image003.jpg){#fig:003 width=100%}


NASM превращает текст программы в объектный код. Например, для компиляции приведённого выше текста программы «Hello World»  мне необходимо написать:

![Объектный файл передан на обработку компановщику](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image004.jpg){#fig:004 width=100%}


Полный вариант командной строки nasm представлен первой строкой на рис. 5. Данная команда скомпилирует исходный файл hello.asm в obj.o. С помощью команды ls проверяю, что файлы были созданы.

![Компиляция и проверка файлов](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image005.jpg){#fig:005 width=100%}

Чтобы получить исполняемую программу, объектный файл необходимо передать на обработку компоновщику.

![Получение исполняемого файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image006.jpg){#fig:006 width=100%}

Далее запускаю на выполнение созданный исполняемый файл, находящийся в текущем каталоге.

![Результат работы исполняемого файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image007.jpg){#fig:007 width=100%}


# Выполнение самостоятельной работы

В каталоге ~/work/arch-pc/lab04 с помощью команды cp создаю копию файла hello.asm с именем lab4.asm. С помощью команды ls убеждаюсь, что файл создан.

![Копирование файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image008.jpg){#fig:008 width=100%}


С помощью текстового редактора вношу изменения в текст программы в файле lab4.asm так, чтобы вместо Hello world! на экран выводилась строка с моей фамилией и именем Карцова Анна.

![Внесение изменений в текстовый файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image009.jpg){#fig:009 width=100%}


Транслирую полученный текст программы lab4.asm в объектный файл. Выполняю компоновку объектного файла и запускаю получившийся исполняемый файл.

![Трансляция, компоновка и запуск исполняемого файла](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image010.jpg){#fig:010 width=100%}

Далее копирую файлы hello.asm и lab4.asm в локальный репозиторий в каталог ~/work/study/2024-2025/"Архитектура компьютера"/arch-pc/labs/lab04/. Загружаю файлы на Github.

![Перенос файлов на Github](/home/sergisa/work/study/2024-2025/Архитектура компьютера/arch-pc/labs/lab04/report/image/image011.jpg){#fig:011 width=100%}



# Выводы

В ходе выполнения лабораторной работы я освоила процедуры компиляции и сборки программ, написанных на ассемблере NASM.


