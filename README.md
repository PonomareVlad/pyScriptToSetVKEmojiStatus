Этот скрипт использует закрытые методы vk api (status.setImage, status.getImage, status.getImageList)
Которые позволяют поставить, прочесть и получить список эмодзи статусов.

Если у вас не стоит python и библиотека requests, то советую воспользоваться подготовленным батником. Запустите "first_run(via installed python).bat".
В любом случае для работы кода требуется библиотека requests. Установить её можно вот этой вот командой в консоль:
И ещё требуется установленный python3.8 и новее

pip install requests

При первом запуске понадобиться получить все токены, чтобы скрипт смог обратиться к серверу, получить список, записать себе в базу( для базы использую sqllite3), и потом ей пользоваться.
После удачного получения вам выпадет список, из которого вам стоит выбрать id эмодзи статуса, рядом будет написано их название(некоторые строки названий будут пусты, из-за отсутсвия описания на сервере), вы можете посмотреть, как они выглядят в базе генерируемой скриптом(там есть поле url, в котором храниться ссылка на сервер с фото).

В конце он вам выдаст строку, на подобии: "response: 200 set id: 8 Name of emoji: Работаю из дома"

В случае, если статус не ставиться, то стоит обновить базу, есть вероятность, что токен был обнулен(администрацией, или же прошло время токена).
Для этого надо удалить генерируемый файл: "vk_status.getImageList.db", после снова запускать скрипт и вставлять токены.