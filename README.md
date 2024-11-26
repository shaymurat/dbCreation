# Домашнее задание по теме "Создание БД, добавление, выбор и удаление элементов."

Если вы решали старую версию задачи, проверка будет производиться по ней.

Ссылка на старую версию [тут](https://docs.google.com/document/d/18EAwsKdiC_EPwyr2KXqXyoe16DBLBUBij9R3EqT2eGc/edit?usp=sharing).

Цель: освоить основные команды языка SQL и использовать их в коде используя
SQLite3.

## Задача "Первые пользователи":

Создайте файл базы данных ```not_telegram.db``` и подключитесь к ней,
используя встроенную библиотеку ```sqlite3```.

Создайте объект курсора и выполните следующие действия при помощи SQL
запросов:

Создайте таблицу ```Users```, если она ещё не создана. В этой таблице должны
присутствовать следующие поля:
1. ```id``` - целое число, первичный ключ
2. ```username``` - текст (не пустой)
3. ```email``` - текст (не пустой)
4. ```age``` - целое число
5. ```balance``` - целое число (не пустой)

Заполните её 10 записями:
```
User1, example1@gmail.com, 10, 1000
User2, example2@gmail.com, 20, 1000
User3, example3@gmail.com, 30, 1000
...
User10, example10@gmail.com, 100, 1000
```

Обновите balance у каждой 2ой записи начиная с 1ой на 500:
```
User1, example1@gmail.com, 10, 500
User2, example2@gmail.com, 20, 1000
User3, example3@gmail.com, 30, 500
...
User10, example10@gmail.com, 100, 1000
```

Удалите каждую 3ую запись в таблице начиная с 1ой:
```
User2, example2@gmail.com, 20, 1000
User3, example3@gmail.com, 30, 500
User5, example5@gmail.com, 50, 500
...
User9, example9@gmail.com, 90, 500
```

Сделайте выборку всех записей при помощи ```fetchall()```, где возраст не
равен ```60``` и выведите их в консоль в следующем формате (без ```id```):
```
Имя: <username> | Почта: <email> | Возраст: <age> | Баланс: <balance>
```

Пример результата выполнения программы:

Вывод на консоль:
```
Имя: User2 | Почта: example2@gmail.com | Возраст: 20 | Баланс: 1000
Имя: User3 | Почта: example3@gmail.com | Возраст: 30 | Баланс: 500
Имя: User5 | Почта: example5@gmail.com | Возраст: 50 | Баланс: 500
Имя: User8 | Почта: example8@gmail.com | Возраст: 80 | Баланс: 1000
Имя: User9 | Почта: example9@gmail.com | Возраст: 90 | Баланс: 500
```

Содержание БД:
```
Таблица: Users

id  username  email               age  balance
--  --------  ------------------  ---  -------
2   User2     example2@gmail.com  20   1000   
3   User3     example3@gmail.com  30   500    
5   User5     example5@gmail.com  50   500    
6   User6     example6@gmail.com  60   1000   
8   User8     example8@gmail.com  80   1000   
9   User9     example9@gmail.com  90   500
```

Файл module_14_1.py с кодом и базу данных not_telegram.db загрузите на ваш
GitHub репозиторий. В решении пришлите ссылку на него.

Успехов!
