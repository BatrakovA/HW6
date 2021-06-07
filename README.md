# Homework6
## todo

### Домашнее задание к лекции «Исключения и обработка ошибок»

***Задание 1***

Печатные газеты использовали свой формат дат для каждого выпуска. Для каждой газеты из списка напишите формат указанной даты для перевода в объект datetime:
The Moscow Times - Wednesday, October 2, 2002
The Guardian - Friday, 11.10.13
Daily News - Thursday, 18 August 1977

***Задание 2***

Дан поток дат в формате YYYY-MM-DD, в которых встречаются некорректные значения:
stream = [‘2018-04-02’, ‘2018-02-29’, ‘2018-19-02’]

Напишите функцию, которая проверяет эти даты на корректность. Т. е. для каждой даты возвращает True (дата корректна) или False (некорректная дата).

***Задание 3***

Напишите функцию date_range, которая возвращает список дат за период от start_date до end_date. Даты должны вводиться в формате YYYY-MM-DD. В случае неверного формата или при start_date > end_date должен возвращаться пустой список.

***Задание 4 (бонусное)***

Ваш коллега прислал код функции:

DEFAULT_USER_COUNT = 3

def delete_and_return_last_user(region, default_list=[‘A100’, ‘A101’, ‘A102’]):
""“
Удаляет из списка default_list последнего пользователя
и возвращает ID нового последнего пользователя.
”""
element_to_delete = default_list[-1]
default_list.remove(element_to_delete)

1
return default_list[DEFAULT_USER_COUNT-2]
При однократном вызове этой функции все работает корректно:
delete_and_return_last_user(1)
‘A101’

Однако, при повторном вызове получается ошибка IndexError: list index out of range.

Задание:

Что значит ошибка list index out of range?
Почему при первом запуске функция работает корректно, а при втором - нет?