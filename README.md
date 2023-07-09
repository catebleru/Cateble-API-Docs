# Cateble-API-Docs
Все методы API работают через метод запросов POST

Ссылка для методов API - cateble.ru/Api/method.php

# Методы

<h3>chat_create</h3>

Метод для создания чатов.

<b>Параметры:</b>

token (string) - Ключ доступа пользователя.

chat_name (string) - Название создаваемого чата.

send_id (int) - С кем создается чат.


Результат при успешном выполнении - {"chat": "successful creation"}


<b>Возможные ошибки:</b>


Не определен token - {"Error": "token not specified"}


Не определен chat_name - {"Error": "chat_name not specified"}


Не определен send_id - {"Error": "send_id not specified"}


Неверный token - {"Error": "undefinded token"}

<h3>get_chats</h3>

Метод для получения всех чатов, в которых состоит пользователь.

<b>Параметры:</b>

token (string) - Ключ доступа пользователя.

Результат при успешном выполнении - {"chats": [список_чатов]}

<b>Возможные ошибки:</b>

Не определен token - {"Error": "token not specified"}

Неверный token - {"Error": "undefinded token"}

Вы не состоите в чате - {"Error": "chat not found"}

<h3>get_chat_members</h3>

Метод для получения участников чата.

<b>Параметры:</b>

token (string) - Ключ доступа пользователя.

chat_id (int) - Айди чата.

Результат при успешном выполнении - {"Members": [список_участников]}

<b>Возможные ошибки:</b>

Не определен token - {"Error": "token not specified"}

Не определен chat_id - {"Error": "chat_id not specified"}

Неверный token - {"Error": "undefinded token"}

Вы не состоите в чате - {"Error": "chat not found"}
