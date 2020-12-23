# Set VK Emoji Status
> Установи эмодзи статус!


Этот проект позволяет установить когда либо существовавшие эмоджи статусы vk(картинки у фамилии). Грубо говоря тут комбинированно 6 приложений(пока что 6). 


## Installation

Скачайте 2 файла __vk_api_closed.exe__ и __appids.txt__
распакуйте их в одной папке, запустите  __vk_api_closed.exe__

___*vk_api_closed.exe* является лишь скомпилированной программой python файла *vk_api_closed.py*___ 

## Usage example

Если вы запустили его впервые, то вас скорее всего попросит получить токены. Это безопасно, во первых потому, что токены выдаются под определённые задачи, например в этом приложении они под установку и чтения статуса, во вторых, он живет 24 часа и не работает если ip не совпадают.

После получения токенов вас спросит, хотите ли вы обновить список? нажмите кнопку y на клавиатуре и Enter. дальше будут отправлены соответсвующие запросы и будут получены "эмоджи статусы".
В самом конце вам предложат выбрать ID эмоджи статуса, который вы хотите установить.

__P.S__
Файл __*appids.txt*__ можно дополнять новыми id приложений, которые имеют emoji status'ы

## Development setup

Перед дальнейшей установкой, у вас должен стоять python(желательно 3.8 и выше). Скачать его можно [здесь][py].

Установим библиотеку для работы скрипта:
```sh
pip install requests
```
(*необязательно*) Для создания __exe__ файла использовалась библиотека pyinstaller.
```sh
pip install pyinstaller
```
Переходим в папку распакованного архива, открываем консоль в этой папке, и пишем:
```sh
pyinstaller --onefile vk_api_closed.py
```
через пару секунд у нас появилась куча папок. В папке dist находиться сгенерированный exe файл

## Release History
* 0.2.0
    * Реализованно меню отладки
    * многий функционал занесен в try except и ошибка выводиться, не закрывая программу
    * Доступен вывод url
* 0.1.1
    * Обновлены основные функции приложения
    * Добавлены более интуитивные подсказки
    * Переработана система получения токенов
* 0.0.1
    * Создан проект, работает 4 приложения

<!-- Markdown link & img dfn's -->
[py]: https://www.python.org/
