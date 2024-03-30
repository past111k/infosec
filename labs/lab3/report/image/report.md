---
## Front matter
title: "Лабораторная работа №3"
subtitle: "Дискреционное разграничение прав в Linux. Два пользователя."
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

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Выполнение лабораторной работы

1.  Используя учетную запись администратора создаем учетную запись guest и задаем ей пароль.

![Создание учетной записи guest и пароля для нее](image/1.png){#fig:001 width=70%}

2.  Создаем пользователя guest2 и задаем ему пароль.

![Создаем пользователя guest2](image/2.png){#fig:002 width=70%}

3.  Добавляем пользователя guest2 в группу guest 

![Добавляем пользователя guest2 в группу guest](image/3.png){#fig:003 width=70%}

4.  Осуществляем вход в систему от двух пользователей на двух разных консолях: guest на первой консоли и guest2 на второй консоли.

![Заходим в систему от имени пользователя guest](image/4.png){#fig:004 width=50%}

![Заходим в систему от имени пользователя guest2](image/5.png){#fig:005 width=50%}

5.  Для обоих пользователей командой pwd определяем директорию, в которой мы находимся.

![Определяем директорию, в которой мы находимся1](image/6.png){#fig:006 width=50%}

![Определяем директорию, в которой мы находимся2](image/7.png){#fig:007 width=50%}

6.  Уточняем имя нашего пользователя, его группу, кто входит в нее и к каким группам принадлежит он сам. Определяем командами groups guest и groups guest2, в какие группы входят пользователи guest и guest2. Сравниваем вывод команды groups с выводом команд id -Gn и id -G

![Определяем в какой группе пользователь-админ](image/8.png){#fig:008 width=50%}

![Определяем в каких группах пользователи guest & guest2](image/9.png){#fig:009 width=50%}

![Вывод команд id -Gn & id -G для пользователя админа](image/10.png){#fig:010 width=50%}

![Вывод команд id -Gn & id -G для пользователя guest](image/11.png){#fig:011 width=50%}

![Вывод команд id -Gn & id -G для пользователя guest2](image/12.png){#fig:012 width=50%}

7.  Сравнивакм полученную информацию с содержимым файла /etc/group.

![Сравниваем полученную информацию с содержимым файла /etc/group1](image/13.png){#fig:013 width=50%}

![Сравниваем полученную информацию с содержимым файла /etc/group2](image/14.png){#fig:014 width=50%}

8.  От имени пользователя guest2 выполяем регистрацию пользователя guest2 в группе guest

![Выполяем регистрацию пользователя guest2 в группе guest](image/15.png){#fig:015 width=70%}

9.  От имени пользователя guest изменяем права директории /home/guest, разрешив все действия для пользователей группы

![Изменяем права директории /home/guest](image/16.png){#fig:016 width=70%}

10.От имени пользователя guest снимаем с директории /home/guest/dir1 все атрибуты

![снимаем с директории /home/guest/dir1 все атрибуты](image/17.png){#fig:017 width=70%}


# Выводы

С помощью данной лабораторной работы мы  получили практических навыков работы в консоли с атрибутами файлов для групп пользователей.

