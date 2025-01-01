# `new Date()`, `new Map()`, `new Set()` и их методы в JavaScript

## `new Date()`
`Date` — это встроенный объект JavaScript, используемый для работы с датами и временем.

### Создание объекта `Date`
```javascript
const now = new Date(); // Текущая дата и время
const specificDate = new Date("2025-01-01T12:00:00Z"); // Указанная дата
```

### Методы `Date`
- Получение данных:
  - `.getFullYear()` — год.
  - `.getMonth()` — месяц (0-11).
  - `.getDate()` — день месяца (1-31).
  - `.getDay()` — день недели (0-6).
  - `.getHours()`, `.getMinutes()`, `.getSeconds()`, `.getMilliseconds()` — время.
  - `.getTime()` — таймстамп (количество миллисекунд с 1 января 1970 года).

- Установка данных:
  - `.setFullYear(year, [month], [date])`
  - `.setMonth(month, [date])`
  - `.setDate(date)`
  - `.setHours(hours, [minutes], [seconds], [ms])`

## `new Map()`
`Map` — коллекция, хранящая пары ключ-значение, где ключи могут быть любого типа.

### Создание объекта `Map`
```javascript
const map = new Map();
const mapWithData = new Map([["key1", "value1"], ["key2", "value2"]]);
```

### Методы `Map`
- Работа с данными:
  - `.set(key, value)` — добавляет пару ключ-значение.
  - `.get(key)` — возвращает значение по ключу.
  - `.delete(key)` — удаляет пару по ключу.
  - `.clear()` — очищает коллекцию.

- Проверка:
  - `.has(key)` — проверяет наличие ключа.

- Итерация:
  - `.keys()` — возвращает итерируемый объект ключей.
  - `.values()` — возвращает итерируемый объект значений.
  - `.entries()` — возвращает итерируемый объект пар [ключ, значение].
  - `.forEach((value, key) => {})` — перебирает элементы.

### Пример использования
```javascript
const map = new Map();
map.set("name", "Alice");
map.set("age", 30);

console.log(map.get("name")); // Alice
console.log(map.has("age")); // true
map.delete("age");
console.log(map.size); // 1
```

## `new Set()`
`Set` — коллекция, хранящая уникальные значения любого типа.

### Создание объекта `Set`
```javascript
const set = new Set();
const setWithData = new Set([1, 2, 3, 3]); // {1, 2, 3}
```

### Методы `Set`
- Работа с данными:
  - `.add(value)` — добавляет значение.
  - `.delete(value)` — удаляет значение.
  - `.clear()` — очищает коллекцию.

- Проверка:
  - `.has(value)` — проверяет наличие значения.

- Итерация:
  - `.values()` — возвращает итерируемый объект значений.
  - `.keys()` — то же самое, что `.values()` (для совместимости с `Map`).
  - `.entries()` — возвращает итерируемый объект пар [значение, значение].
  - `.forEach((value) => {})` — перебирает элементы.

### Пример использования
```javascript
const set = new Set();
set.add(1);
set.add(2);
set.add(2); // Дубликаты игнорируются

console.log(set.has(1)); // true
console.log(set.size); // 2
set.delete(2);
set.clear();
console.log(set.size); // 0
