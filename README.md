# Домашняя работа 10.1 "Продвинутый Git"

## Цель проекта
- Ознакомиться с технологией ***GitHub***:
  - создавать и настраивать удаленные репозитории;
  - обучиться работать с ветками, создавать их, объединять, удалять;
  - изучить операции ***git push***, ***git merge***, ***pull request***.

- Закрепить усвоение материала урока 9.2 ("Основы Git"): команды ***git add***, ***git commit***.

## Инструкция по установке

1. Клонируйте репозиторий:
```python
git clone https://github.com/DoniyoRich/homework_10_1.git
```

2. Установите зависимости:
```
pip install -r requirements.txt
```

## Новые фичи
В домашнем задании добавлен модуль ***processing***, в котором реализованы две функции:
- ***filter_by_state()***
- ***sort_by_date()***

1. Функция ***filter_by_state()*** принимает список словарей и опционально значение для ключа 
'state' (по умолчанию 'EXECUTED').
Функция возвращает новый список словарей, содержащий только те словари, у которых ключ 
'state' соответствует указанному значению.


2. Функция ***sort_by_date()*** принимает список словарей и необязательный параметр, задающий порядок сортировки (по умолчанию — убывание).
Функция возвращает новый список, отсортированный по дате ('date').

## Примеры использования функций

### Функция ***filter_by_state()***
#### *Пример входных данных для функции*
```python
[
{'id': 41428829, 'state': 'EXECUTED', 'date': '2019-07-03T18:35:29.512364'},
{'id': 939719570, 'state': 'EXECUTED', 'date': '2018-06-30T02:08:58.425572'},
{'id': 594226727, 'state': 'CANCELED', 'date': '2018-09-12T21:27:25.241689'},
{'id': 615064591, 'state': 'CANCELED', 'date': '2018-10-14T08:21:33.419441'}
]
```
#### *Пример работы функции*
#### Выход функции со статусом по умолчанию *'EXECUTED'*
```python
[
{'id': 41428829, 'state': 'EXECUTED', 'date': '2019-07-03T18:35:29.512364'},
{'id': 939719570, 'state': 'EXECUTED', 'date': '2018-06-30T02:08:58.425572'}
]
```
#### Выход функции, если вторым аргументов передано *'CANCELED'*
```python
[
{'id': 594226727, 'state': 'CANCELED', 'date': '2018-09-12T21:27:25.241689'},
{'id': 615064591, 'state': 'CANCELED', 'date': '2018-10-14T08:21:33.419441'}
]
```
### Функция ***sort_by_date()***
#### *Пример входных данных для функции*
```python
[
{'id': 41428829, 'state': 'EXECUTED', 'date': '2019-07-03T18:35:29.512364'},
{'id': 939719570, 'state': 'EXECUTED', 'date': '2018-06-30T02:08:58.425572'},
{'id': 594226727, 'state': 'CANCELED', 'date': '2018-09-12T21:27:25.241689'},
{'id': 615064591, 'state': 'CANCELED', 'date': '2018-10-14T08:21:33.419441'}
]
```
#### *Пример работы функции*
#### Выход функции (сортировка по убыванию, т. е. сначала самые последние операции)
```python
[
{'id': 41428829, 'state': 'EXECUTED', 'date': '2019-07-03T18:35:29.512364'},
{'id': 615064591, 'state': 'CANCELED', 'date': '2018-10-14T08:21:33.419441'},
{'id': 594226727, 'state': 'CANCELED', 'date': '2018-09-12T21:27:25.241689'},
{'id': 939719570, 'state': 'EXECUTED', 'date': '2018-06-30T02:08:58.425572'}
]
```
## Лицензия

[SkyPro IT School](#)