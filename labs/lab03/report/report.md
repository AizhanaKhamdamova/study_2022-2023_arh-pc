---
## Front matter
title: "Архитектура компьютеров"
subtitle: "Лабораторная работа №3"
author: "Хамдамова Айжана"


# "Содержание":
1. Цель работы 
2. Ход работы
3. Самостоятельная работа 
4. Вывод

# Цель работы
Целью работы является изучить идеологию и применение средств контроля версий. Приобрести практические навыки по работе с системой git.


# Выполнение лабораторной работы
##II.Ход работы:
1. Первым делом создаю учётную запись на сайте https://github.com/ и заполняю основные данные. Ввожу email, пароль и username.
![]
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/'Изображения'/'Снимки экрана'/1.jpg
2.     2. Сначала сделаем предварительную конфигурацию git. Открываю терминал и ввожу следующие команды, указав имя и email владельца репозитория:
git config --global user.name "<AizhanaKhamdamova >"
git config --global user.email "<1032225989@pfur.ru >"
Настроим utf-8 в выводе сообщений git:
git config --global core.quotepath false
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/2.png
3. Затем набираем следующие команды, чтобы задать имя начальной ветки (будем называть её master):
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/3.png
4. Параметр autocrlf:
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/4.png
5. Для последующей идентификации пользователя на сервере репозиториев я сгенерировала пару ключей с помощью следующих команд: 
ssh-keygen -C "AizhanaKhamdamova<1032225989@pfur.ru>"
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/5.png
6. Далее необходимо загрузить сгенерированный открытый ключ. Для этого  я зашла на сайт http://github.org/ под своей учётной записью и перешла в меню Setting . После этого выбрала в боковом меню SSH and GPG keys и нажала кнопку New SSH key . Скопировав из локальной консоли ключ в буфер обмена  cat ~/.ssh/id_rsa.pub | xclip -sel clip я вставила ключ в появившееся на сайте поле и указала для ключа имя (dk-4.3).
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/6.png
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/7.png
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/8.png

7. Затем мне нужно создать каталог для предмета «Архитектура компьютера»:
 mkdir -p ~/work/study/2022-2023/"Архитектура  компьютера"
 /afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/9.png
8. Далее я перешла на станицу репозитория с шаблоном курса https://github.com/yamadharma/course-directory-student-template. Нажала на иконку: Use this template.
 /afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/10.png
9. В открывшемся окне нужно задать имя репозитория (Repository name) study_2022–2023_arh-pc и создать репозиторий (кнопка Create repository from template).
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/11.png
10.     9. Открываю терминал и перехожу в каталог курса:
cd ~/work/study/2022-2023/"Архитектура компьютера" клонирую созданный репозиторий: git clone --recursive
↪ git@github.com:<AizhanaKhamdamova>/study_2022–2023_arh-pc.git arch-pc
  Ссылку для клонирования копирую на странице     созданного репозитория Code -> SSH:
  /afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/12.png
  /afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/13.png
11.     10. После переходим в каталог курса: 
cd ~/work/study/2022-2023/"Архитектура компьютера"/arch-pc
и удаляем лишние файлы (rm package.json ).Создадим необходимые каталоги: echo arch-pc > COURSE  
Make
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/14.png
12.     12. Отправляю файлы на сервер:
git add .
git commit -am 'feat(main): make course structure'
git push
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/15.png
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/16.png
# Задания для самостоятельной работы:
 1. Я скопировала отчеты по первой и второй лабораторных работ в соответствующие каталоги созданного рабочего пространства из раздела «загрузки». (в lab01 и lab02)
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/ср1.png
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/ср2.png
2. Затем мы загружаем эти же файлы в github через теримнал, т.е отправляем на сервер с помощью команд: 
git add .
git commit -am 'feat(main): make course structure'
git push
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/ср3.png
3. Проверяем репозиторий github. Должны появиться файлы. Отчет по выполнению лабораторной работы №3 я загружу аналогично как 1ый и 2ой. В соответствующем каталоге рабочего пространства (labs>lab03>report).
/afs/.dk.sci.pfu.edu.ru/home/a/k/akhamdamova/Изображения/Снимки экрана/ср4.png


# Вывод
В ходе выполнения данной лабораторной работы я приобрела практические навыки по работе с системой git. Научилась работать с репозитория

