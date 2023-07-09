# Cateble-API-Docs
Все методы API работают через метод запросов POST


Ссылка для методов API - cateble.ru/Api/method.php


------------------------------------------------------------


Методы:
chat_create - Метод для создания чатов.


Параметры:

token (string) - Ключ доступа пользователя.

chat_name (string) - Название создаваемого чата.

members (json array) - Участники создаваемого чата.


Результат при успешном выполнении - {"chat": "successful creation"}


Возможные ошибки:


Не определен token - {"Error": "token not specified"}


Не определен chat_name - {"Error": "chat_name not specified"}


Не определен members - {"Error": "members not specified"}


Неверный token - {"Error": "undefinded token"}

------------------------------------------------------------

get_chat - Метод для получения всех чатов, в которых состоит пользователь
token (string) - Ключ доступа пользователя.


Результат при успешном выполнении - {"chats": [список_чатов]}


Возможные ошибки:


Не определен token - {"Error": "token not specified"}


Неверный token - {"Error": "undefinded token"}
