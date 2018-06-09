Доска обьявлений только в виде *REST API на Flask* - нужно написать только API
без визуальной части. а также добавить:
- авторизацию
- лайки для обьявления
- лимит количества комментариев и лайков для пользователя
(5 лайков и 5 комментариев в час)

Полный текст заания
*Функционал/Endpoints*:
1) Логин, Регистрация:
signup поля:
username. обязательное, 20 символов максимум.
password. обязательное, 20 символов максимум
confirm_password. обязательное, 20 символов максимум

Для логина ко всем эндпоинтам передавать заголовок в формате
```Authorization: {username}:{password}```

(кто хочет может сделать Token based authorization  но это не обязательно)

если на любой из ниже приведенных эндпоинтов пришел неверный заголовок авторизации
выдавать 401 Unbauthorized.

2)  Обьявления. - список обьявлений

3)  Добавить    обьявление
поля:
- Имя Username: обязательное, 20 символов максимум
- Название обьявления: обязательное, 50 символов максимум

4)  Просмотреть обьявление
Выводит информацию про обьявление
- Создатель (creator)
- Название обьявления
- Дата создания
- Комментарии

5)  Добавить    комментарий к   обьявлению
параметры:
- Имя Username(creator): обязательное, 30 символов максимум
- Текст комментария (comment): обязательное, 255 символов максимум

6) Лайк для обьявления
7) Эндпоинты для добавления комментария и лайка должны иметь лимит по 5 лайков/комментариев от одного пользователя  в час.