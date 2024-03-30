---
## Front matter
title: "Лабораторная работа №4"
subtitle: "Дискреционное разграничение прав в Linux. Расширенные атрибуты."
author: "Кочарян Никита Робертович"

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

Получение практических навыков работы в консоли с расширенными атрибутами файлов.

# Выполнение лабораторной работы

1.  От имени пользователя guest определите расширенные атрибуты файла /home/guest/dir1/file1

![Опередляем расширенные атрибуты файла file1](image/1.png){#fig:001 width=70%}

2.  Устанавливаем на file1 права, разрешающие чтение и запись для владельца файла.

![Устанавливаем на file1 права, разрешающие чтение и запись для владельца файла](image/2.png){#fig:002 width=70%}

3.  Пробуем установить на файл file1 установить расширенный атрибут a от имени пользователя guest. Получаем отказ.

![Пробуем установить на файл file1 установить расширенный атрибут a](image/3.png){#fig:003 width=70%}

4.  Заходим на третью консоль с правами администратора. Устанавливаем расширенный атрибут а на файл file1 от имени супер-пользователя.

![Устанавливаем расширенный атрибут а на файл file1 от имени супер-пользователя.](image/4.png){#fig:004 width=70%}

5.  От пользователя guest проверяем правильность установления атрибута:

![От пользователя guest проверяем правильность установления атрибута](image/5.png){#fig:005 width=70%}

6.  Выполняем дозапись в файл file1 слова «test». После этого выполянем чтение файла file1.

![Выполняем дозапись в файл file1 слова «test». После этого выполянем чтение файла file1](image/6.png){#fig:006 width=50%}

7.  Пробуем удалить файл file1 либо стереть имеющуюся в нём информацию

![Пробуем удалить файл file1 либо стереть имеющуюся в нём информацию](image/7.png){#fig:07 width=70%}

8.  Пробуем установить на файл file1 права, например, запрещающие чтение и запись для владельца файла. Получаем отказ.

![Пробуем установить на файл file1 права, например, запрещающие чтение и запись для владельца файла](image/8.png){#fig:08 width=70%}

9.  Снимаю расширенный атрибут a с файла file1 от имени суперпользователя.

![Снимаю расширенный атрибут a с файла file1 от имени суперпользователя.](image/9.png){#fig:019 width=70%}

10. Снова пробуем удалить файл file1 либо стереть имеющуюся в нём информацию.

![Снова пробуем удалить файл file1 либо стереть имеющуюся в нём информацию.](image/10.png){#fig:010 width=70%}

# Выводы

В результате выполнения работы вы повысили свои навыки использования интерфейса командой строки (CLI), познакомились на примерах с тем, как используются основные и расширенные атрибуты при разграничении доступа. Имели возможность связать теорию дискреционного разделения доступа (дискреционная политика безопасности) с её реализацией на практике в ОС Linux. Составили наглядные таблицы, поясняющие какие операции возможны при тех или иных установленных правах. Опробовали действие на практике расширенных атрибутов «а» и «i».
