# Cateble-API-Docs
Все методы API работают через метод запросов POST

Ссылка для методов API - cateble.ru/Api/method.php

# Методы

<h3>chat_create</h3>

Метод для создания чатов.

<b>Параметры:</b>

token (string) - Ключ доступа пользователя.

chat_name (string) - Название создаваемого чата.

members (json array) - Участники создаваемого чата.


Результат при успешном выполнении - {"chat": "successful creation"}


<b>Возможные ошибки:</b>


Не определен token - {"Error": "token not specified"}


Не определен chat_name - {"Error": "chat_name not specified"}


Не определен members - {"Error": "members not specified"}


Неверный token - {"Error": "undefinded token"}

<h3>get_chat</h3>

Метод для получения всех чатов, в которых состоит пользователь.

<b>Параметры:</b>

token (string) - Ключ доступа пользователя.

Результат при успешном выполнении - {"chats": [список_чатов]}

<b>Возможные ошибки:</b>

Не определен token - {"Error": "token not specified"}

Неверный token - {"Error": "undefinded token"}
