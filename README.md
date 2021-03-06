# Сайт игрового проекта Bobr RP

Это веб сайт где пользователь может подробнее узнать о нашем игровом проекте.

Тестовый просмотр можно увидеть [тут](https://test.mtabobr.ru/)

## Оглавление

1. [В чём суть?](#В-чём-суть?)
2. [Функционал](#Функционал)
3. [User story](#User-story)
4. [Интерфейс разрабатываемого продукта](#Интерфейс-разрабатываемого-продукта)
5. [Запуск сайта](#Запуск-сайта)
6. [Установка и запуск сборщика Phing](#Установка-и-запуск-сборщика-Phing)
7. [Участники](#Участники)


## В чём суть?

Пользователь заходит на наш сайт, где может узнать как установить нашу игру, посмотреть фотографии проекта, для того чтобы понять в чем суть нашего проекта.

## Функционал

* Пополнять виртуальную игровую валюту за реальные деньги.
* Обеспечение просмотра карусель галереи проекта
* Обеспечение просмотра инструкции по установке игры

## User story

| Заголовок |  | Главная страница |
|----:|:----:|:----------|
| Пользователь | Как | Геймер |
| Примечание | Я хочу | Я хочу иметь возможность увидеть на главной странице описание игрового проекта. |
| Цель | Чтобы | Чтобы понять: интересна мне эта игра или же нет. |


| Заголовок |  | Начать играть |
|----:|:----:|:----------|
| Пользователь | Как | Геймер |
| Примечание | Я хочу | Я хочу иметь возможность установить игру и начать играть. |
| Цель | Чтобы | Чтобы насладиться этим шикарным игровым контентом. |


| Заголовок |  | Донат |
|----:|:----:|:----------|
| Пользователь | Как | Геймер |
| Примечание | Я хочу | Я хочу иметь возможность пополнить виртуальную игровую валюту за реальные деньги. |
| Цель | Чтобы | Чтобы стало интересней и проще играть. |


| Заголовок |  | О проекте |
|----:|:----:|:----------|
| Пользователь | Как | Геймер |
| Примечание | Я хочу | Я хочу иметь возможность увидеть рассуждение разработчика на тему его собственной мотивации, сподвигнувшая его на создание этого игрового проекта. |
| Цель | Чтобы | Чтобы в дальнейшем, может быть, опробовать себя в этой деятельности. |

## Интерфейс разрабатываемого продукта

Интерфейс разрабатываемого продукта выполнен в программе Adobe XD. 

Для того чтобы Вы могли посмотреть макет дизайна, Вам нужно скачать [Adobe XD](https://www.adobe.com/ru/products/xd.html), после установки запустить файл **[BobrRP] Сайт.xd**

## Запуск сайта

1. Для запуска сайта Вам потребуется OpenServer
2. Выбираете модули для HTTP - Apache-PHP, для PHP - PHP-7.2, для MySQL - MySQL-5.6
3. Переносите файлы сайта на OpenSrever в папку с сайтами
4. После всех пройденных пунктов, можно запускать локальный сервер

## Установка и запуск сборщика Phing


1. Для начала нужен composer в OpenServer

1.1 В OpenServer открываем: Дополнительно -> Конфигурация -> PHP .....
Проверяем наличие раскомментированного **extension=php_openssl.dll**

1.2 Включаем Консоль OpenServer'a: Дополнительно -> Консоль.
Коммандами консоли windows переходим в папку используемого php. Я использую php-5.5.6 и моя команда выглядит так:
```cd modules/php/PHP-5.5.6/```

1.3 Затем выполняем комманду ```php -r "readfile('https://getcomposer.org/installer');" | php```

1.4 Composer установился и набрав комманду ```php composer.phar -V``` Вы должны увидеть запись подобного рода ```Composer version <версия> < дата обновления >```

1.5 Далее создаем в корневой директории файл composer.json с добавленным кодом 
```
{
    "require-dev": {
        "phing / phing": "2. *"
    }
}
```

2. Устанавливаем командой  ```php composer.phar install```

3. Добавляем файл по адресу **C:\OpenServer\domains\phing\vendor\phing\phing\bin\phing.bat**

4. Запускаем сборку проектов из командой строки вашей OS, для этого перейдем в корневую папку с проектом на OpenServer и введем команду ```phing```

5. Готово! 

## Участники
### Группа ИКБО-18-19
* Макеев Алексей [bobr-a](https://github.com/bobr-a) - создание сайта (css,html,js,php), разработка дизайна
* Журавлев Александр [puplodik](https://github.com/puplodik) - функциональное требование
* Кузнецов Илья [Aktonus](https://github.com/Aktonus) - сборщик пакета Phing
* Савкин Дмитрий [bydywiigenii](https://github.com/bydywiigenii) - запуск сайта на OpenServer
