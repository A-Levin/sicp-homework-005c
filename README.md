# Домашка 005c - Higher Order (Практика)

Функции высшего порядка + работа с файлами.

## Задания

### 1. `apply_to_all(f, items)`
Применяет функцию f к каждому элементу списка (как map).

```python
apply_to_all(lambda x: x * 2, [1, 2, 3])  # → [2, 4, 6]
```

### 2. `filter_by(predicate, items)`
Фильтрует список по условию.

```python
filter_by(lambda x: x > 0, [-1, 2, -3, 4])  # → [2, 4]
```

### 3. `compose(f, g)`
Композиция функций: h(x) = f(g(x)).

```python
compose(lambda x: x * 2, lambda x: x + 1)(5)  # → 12
```

### 4. Практика с файлами

- `find_large_files(directory, min_size)` — файлы больше min_size байт
- `get_python_files(directory)` — все .py файлы
- `get_file_sizes(directory)` — список (filename, size)

### 5. Бонус: `make_file_filter(extension)`
Замыкание — возвращает функцию-фильтр.

```python
py_filter = make_file_filter("py")
py_filter("main.py")   # → True
py_filter("data.csv")  # → False
```

## Тестовые файлы

В папке `test_files/` лежат файлы для тестирования:
- `small.txt` (5 байт)
- `medium.txt` (120 байт)
- `large.txt` (752 байт)
- `script.py`, `utils.py` (.py файлы)
- `data.csv`

## Как сдать

1. Форкни репозиторий
2. Реализуй функции в `homework.py`
3. `pytest tests/ -v`
4. Commit и push
5. Проверь Actions ✅

## Тесты

- 5 тестов на apply_to_all
- 5 тестов на filter_by
- 4 теста на compose
- 3 теста на find_large_files
- 2 теста на get_python_files
- 2 теста на get_file_sizes
- 3 теста на make_file_filter (бонус)
