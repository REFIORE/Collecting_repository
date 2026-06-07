# Вводные данные необходимые для запуска каждого из файлов
Путь к файлу базы данных

Название фильма для поиска


# Запускается первым — find_similar.py
## Что делает скрипт?

Скрипт находит фильмы, похожие на заданный пользователем.

## Как его запустить?

1. Убедитесь, что у вас установлен Python
2. Сохраните скрипт как find_similar.py
3. Запустите через терминал:
```
python find_similar.py
```

## Что он требует для запуска?

- Python 3
- Модуль ```own_db_helpers```
- Файлы базы данных - содержит список фильмов со строго определёнными полями:
> - original_title, belongs_to_collection, original_language, budget, genres.

## Где взять необходимые для его запуска штуки?

- [Python](https://www.python.org/downloads/) - Официальный сайт
- Модуль ```own_db_helpers```
- Файлы базы данных

## Что он выведет?

```
Enter path to DataBase: films.json
Enter film to search for: The Matrix
The Dark City
Equilibrium
Inception
```

Если фильм не найден:
```
File not found, sorry...
```


# Файл hello_api_TMDB.py
## Что делает скрипт?
Обращается к API сайта [The Movie Database](https://www.themoviedb.org/) и получает бюджет фильма сномером 215

## Как его запустить?
1. Убедитесь, что у вас установлен Python
2. Сохраните рядом два файла:
> - hello_api_TMDB.py
> - tmdb_helpers.py
3. Запустите через терминал:
```
python hello_api_TMDB.py
```

## Что он требует для запуска?
- Python 3
- Модуль requests.
```
pip install requests
```
- Действующий API-ключ TMDB
- Файл tmdb_helpers.py с функциями get_user_api_key() и make_tmdb_api_request()

## Где взять необходимые для его запуска штуки?
- Сам скрипт и tmdb_helpers.py
- API-ключ TMDB (бесплатно):
> 1. Зарегистрируйтесь на TMDB.
> 2. Войдите в аккаунт → перейдите в Настройки → API.
> 3. Создайте новый ключ (тип "Developer").
> 4. Скопируйте полученную строку (пример: 1a2b3c4d5e6f7g8h9i0j).

## Что он выведет?
```
Enter your API key: 1a2b3c4d5e6f7g8h9i0j63000000
```

При ошибке (неверный ключ):
```
Enter your API key: wrong_key
Invalid api key
```

При ошибке (Нет подключения к интернету):
```
Enter your API key: 1a2b3c4d5e6f7g8h9i0j
Traceback (most recent call last):
...
requests.exceptions.ConnectionError
```


# Файл search_in_db.py
## Что делает скрипт?
Ищет фильм в базе данных по названию. Он находит все фильмы, в оригинальном названии которых встречается введенная пользователем подстрока, и выводит их в алфавитном порядке.

## Как его запустить?
1. Убедитесь, что у вас установлен Python
2. Сохраните скрипт как search_in_db.py
3. Запустите через терминал:
```
python search_in_db.py
```

## Что он требует для запуска?
- Python 3
- Модуль ```own_db_helpers```
- Файлы базы данных - содержит список фильмов со строго определённым полем:
> - original_title

## Где взять необходимые для его запуска штуки?
- [Python](https://www.python.org/downloads/) - Официальный сайт
- Модуль ```own_db_helpers```
- Файлы базы данных

## Что он выведет?
```
Enter path to DataBase: movies.json
Enter film to search for: star
Star Trek: The Motion Picture
Star Wars: A New Hope
Star Wars: The Empire Strikes Back
```

Ничего не найдено:
```
Enter path to DataBase: movies.json
Enter film to search for:
```

Если фильм не найден:
```
Enter path to DataBase:
File not found, sorry...
```
