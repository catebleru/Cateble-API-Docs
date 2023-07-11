# Cateble-API-Docs
Все методы API работают через метод запросов POST  

# Методы

<h2>Аккаунт (Cateble ID)</h2>

<h3>login</h3>

Метод авторизации для получения токена пользователя.  
https://id.cateble.ru/login

* <b>Параметры</b>  
`mail` - почта.  
`password` - пароль.

* <b>Возможные ошибки</b>  
Данные не введены  
Пользователь не существует  
Введён неверный пароль

<b>Результат при успешном выполнении</b>
```json
{"token": "ТОКЕН", "uid": "ID_ПОЛЬЗОВАТЕЛЯ"}
```

<h3>registration</h3>

Метод для регистрации пользователя.  
https://id.cateble.ru/registration

* <b>Параметры</b>  
`mail` - почта.  
`password` - пароль.

* <b>Возможные ошибки</b>  
Не введена почта или пароль  
Пользователь с таким ником или почтой уже существует  
Произошла ошибка

<b>Результат при успешном выполнении</b>
```json

```

<h3>activate</h3>

Метод для подтверждения почты пользователя.  
https://id.cateble.ru/activate

* <b>Параметры</b>  
`code` - код активации.

* <b>Возможные ошибки</b>  
Код не введён

<b>Результат при успешном выполнении</b>
```json
{"token": "ТОКЕН", "uid": "ID_ПОЛЬЗОВАТЕЛЯ"}
```

<h3>get_account</h3>

Метод для получения данных о пользователе.  
https://id.cateble.ru/get_account

* <b>Параметры</b>  
`nick` - никнейм пользователя (короткое имя пользователя).  
*Также можно получить данные о пользователе по токену (ключ доступа пользователя)*  
`token` - ключ доступа пользователя.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h2>Посты</h2>

<h3>create_post</h3>

Метод для создания поста.  
https://cateble.ru/Api/create_post

* <b>Параметры</b>  
`text` - текст поста.  
`token` - ключ доступа пользователя.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h3>get_post</h3>

Метод для получения определённого поста.  
https://cateble.ru/Api/get_post

* <b>Параметры</b>  
`id` - ID поста.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h3>get_posts</h3>

Метод для получения всех постов пользователя.  
https://cateble.ru/Api/get_posts

* <b>Параметры</b>  
`nick` - никнейм пользователя (короткое имя пользователя).

* <b>Необязательные параметры</b>  
`token` - ключ доступа пользователя.  
*Токен нужен для того чтобы узнать поставили ли вы лайк посту*

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h3>delete_post</h3>

Метод для удаления поста.  
https://cateble.ru/Api/delete_post

* <b>Параметры</b>  
`id` - ID поста.  
`token` - ключ доступа пользователя.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h3>change_pin</h3>

Метод для закрепления/открепления поста на странице пользователя.  
https://cateble.ru/Api/change_pin

* <b>Параметры</b>  
`post` - ID поста.  
`token` - ключ доступа пользователя.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h3>like</h3>

Метод для лайка поста.  
https://cateble.ru/Api/like

* <b>Параметры</b>  
`post_id` - ID поста.  
`token` - ключ доступа пользователя.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h3>send_comment</h3>

Метод для отправки комментария под определённый пост.  
https://cateble.ru/Api/send_comment

* <b>Параметры</b>  
`id` - ID поста.  
`text` - текст комментария.  
`token` - ключ доступа пользователя.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h3>get_comments</h3>

Метод для получения комментариев под постом.  
https://cateble.ru/Api/get_comments

* <b>Параметры</b>  
`id` - ID поста.

* <b>Возможные ошибки</b>  


<b>Результат при успешном выполнении</b>
```json

```

<h2>Чаты</h2>

<h3>chat_create</h3>

Метод для создания чатов.  
https://cateble.ru/Api/create_chat

* <b>Параметры</b>  
`token` - ключ доступа пользователя.  
`chat_name` - название создаваемого чата.  
`ico` - иконка создаваемого чата.

* <b>Возможные ошибки</b>  
Не определен token  
Не определен chat_name  
Не определен ico  
Неверный token

<b>Результат при успешном выполнении</b>
```json
{"chat": "successful creation"}
```

<h3>get_chats</h3>

Метод для получения всех чатов, в которых состоит пользователь.  
https://cateble.ru/Api/get_chats

* <b>Параметры</b>  
`token` - ключ доступа пользователя.  

* <b>Возможные ошибки</b>  
Не определен token  
Неверный token
Вы не состоите в чате

<b>Результат при успешном выполнении</b>
```json
{"chats": ["СПИСОК_ЧАТОВ"]}
```

<h3>get_chat_members</h3>

Метод для получения участников чата.  
https://cateble.ru/Api/get_chat_members

* <b>Параметры</b>  
`token` - ключ доступа пользователя.
`chat_id` - ID чата.

* <b>Возможные ошибки</b>  
Не определен token  
Не определен chat_id  
Неверный token  
Вы не состоите в чате

<b>Результат при успешном выполнении</b>
```json
{"Members": ["СПИСОК_УЧАСТНИКОВ"]}
```
