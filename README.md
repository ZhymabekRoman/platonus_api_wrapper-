# Platonus API Wrapper - неофициальная Python библиотека для работы с Платонусом (maintenance mode)
[![Maintainability](https://api.codeclimate.com/v1/badges/7a4695ad3d671c96f922/maintainability)](https://codeclimate.com/github/ZhymabekRoman/platonus_api_wrapper/maintainability)
[![Requirements Status](https://requires.io/github/ZhymabekRoman/platonus_api_wrapper/requirements.svg?branch=main)](https://requires.io/github/ZhymabekRoman/platonus_api_wrapper/requirements/?branch=main)

Делаю то, что по определённым причинам не сделали разработчики Платонуса.

## ВНИМАНИЕ!
ПРОЕКТ ЗАБРОШЕН! ИСПОЛЬЗУЙТЕ НА СВОИ СТРАХ И РИСКс

## Введение
Эта библиотека предоставляет Python интерфейс для никем незадокументированного и сделанного только для себя REST API Платонуса. Информации о REST API были получены путем снифинга трафика веб приложении и Android клиента, так как в свободном доступе нету ни исходников Платонуса, ни документации (комерческая тайна).

## Мотивация
Идея создания своей библиотеки-обертки над Платонусом пришло после несколько месяцев мучении во время использовании веб интерфейса. Веб интерфейс очень кривой, имеет очень огромное количество багов. И у меня увы еще и очень слабый ноутбук, на процессоре Celeron, и Платонус загружается катастрофически медленно, и я решил написать бота для Telegram. Но как выяснилось позже, готовых реализации REST API Платонуса нету. Тут я загорелся идеей сделать это.

## Замечание
* Я учусь в колледже и имею доступ только к возможностям студента и не более, соответственно в библиотеке реализован только функционал студента - я не могу реализовать то, к чему я не имею доступ. Ни функции учителя, ни админа не реаизовано, т.к. надо имеет доступ к этим фнукциям и снифить запросы каждого обьекта/функции. Если у кого-то есть доступ к админ или учительской панели Платонуса, и есть желание реализовать это в библиотеке, просьба помочь.
* Так же проблема описанная выше, касается и для учащихся университета - в библиотеке реализован функционал ориентированный для колледжа, но думаю большинство методов/функции/JSON ответов схожи с колледжом. Но самое главное лед сломан, путь открыт, дорога показана.
* Еще одна проблема - Платонус имеет очень много версии: начиная от ~2.00 до ~5.70, и предусмотреть все изменении не возможно, это усложняется тем что нету документации. Например адресс REST API метода `menuTimeDate`, который возвращает серверное время Платонуса, менялся в разных версиях Платонуса, пока точно не известно, в каких конкретных версиях

## Установка
В данное время Вы можете установить библиотеку из исходного кода с помощью pip3:
```
python3 -m pip install https://github.com/ZhymabekRoman/platonus_api_wrapper/archive/main.zip
```

Или же напрямую через setup.py:
```
$ git clone https://github.com/ZhymabekRoman/platonus_api_wrapper --recursive
$ cd platonus-api-wrapper
$ python3 setup.py install
```

## Начало работы
Для работы с бибилотекой нужно впервую очередь импортировать и инициализировать экземпляр класса PlatonusAPI и в качестве аргументов передать главный адресс Платонуса:
```
import logging
from platonus_api_wrapper import PlatonusAPI

logging.basicConfig(level=logging.DEBUG)

platonus_session = PlatonusAPI("http://test4.platonus.kz")
...
```

Больше кода вы можете найти в файле test.py

## Документация
Ее нету и не будет.

## Внесение своего вклада в проект
Внесение своего вклада максимально приветствуется! Есть перечень пунктов, который стоит соблюдать. Каждый пункт перечня расписан в CONTRIBUTING.
