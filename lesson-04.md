# Модуль 2. Занятие 2. Массивы и функции

## Задача 7 - Функции

Напиши функцию `min(a,b)`, которая возвращает меньшее из чисел `a` и `b`.

```js
console.log(min(2, 5)); // 2
console.log(min(3, -1)); // -1
console.log(min(1, 1)); // 1
```

## Задача xxx - Перебор массива

Напиши скрипт, который перебирает массив `fruits` циклом `for`. Для каждого
элемента массива выведи в консоль строку в формате
`номер_элемента: значение_элемента`. Нумерация элементов должна начинаться с
`1`.

Напиши функцию `logItems(array)`, которая получает массив и использует цикл
`for`, который для каждого элемента массива будет выводить в консоль сообщение в
формате `<номер элемента> - <значение элемента>`. Нумерация элементов должна
начинаться с `1`.

Например для первого элемента массива `['Mango', 'Poly', 'Ajax']` с индексом `0`
будет выведено `1 - Mango`, а для индекса 2 выведет `3 - Ajax`.

```js
const fruits = ['🍎', '🍇', '🍑', '🍌', '🍋'];
```

## Задача XXX - Массивы и циклы

Напиши скрипт который выводит в консоль имя и телефонный номер пользователя. В
переменных `names` и `phones` хранятся строки имен и телефонных номеров,
разделенные запятыми. Порядковый номер имен и телефонов в строках указывают на
соответствие. Количество имен и телефонов гарантированно одинаковое.

```js
const names = 'Jacob,William,Solomon,Artemis';
const phones = '89001234567,89001112233,890055566377,890055566300';
```

## Пример 1 - Поиска самого длинного слова

Напиши фукцнию `findLongestWord(string)` которая принимает произвольную строку
состоящую только из слов разделённых пробелом (параметр `string`) и возвращает
самое длинное слово в этой строке.

### Код

```js
function findLongestWord(string) {
  const words = string.split(' ');
  let longestWord = words[0];

  for (let i = 1; i < words.length; i += 1) {
    if (longestWord.length < words[i].length) {
      longestWord = words[i];
    }
  }

  return longestWord;
}

findLongestWord('The quick brown fox jumped over the lazy dog'); // 'jumped'
findLongestWord('Google do a roll')`; // 'Google'
findLongestWord('May the force be with you'); // 'force'
```

## Пример 2 - Дефолтные значения параметров функции

Напишите функцию `greet(name)`, которая при вызове будет получать имя (например,
«Василий») и логировать строку «Привет, <имя>». В случае отсутствующего
аргумента выводить «Привет, гость»

### Код

```js
const greet = function (name) {};

greet('Манго');
greet();
```

## Пример 3 - Псевдомассив arguments

Напишите функцию `calculateAverage()` которая принимает произвольное кол-во
аргументов и возвращает их среднее значение. Все аругменты будут только числами.

### Код

```js
function calculateAverage() {}

console.log(calculateAverage(1, 2, 3, 4)); // 2.5
console.log(calculateAverage(14, 8, 2)); // 8
console.log(calculateAverage(27, 43, 2, 8, 36)); // 23.2
```

## Пример 4 - Стрелочные функции (explicit return)

Выполните рефакторинг заменив объявление функции на стрелочную функцию.

```js
function checkNumbers(a, b) {
  if (a > b) {
    return `число ${a} больше ${b}`;
  }

  return `число ${b} больше ${a}`;
}
```

## Пример 5 - Стрелочные функции (implicit return)

Выполните рефакторинг заменив объявление функции на стрелочную функцию.

```js
function mult(x, y, z) {
  return x * y * z;
}
```

## Пример 6 - Коллекция курсов (includes, indexOf, push и т. д.)

Напишите функции для работы с коллекцией обучающих курсов `courses`:

- `addCourse(name)` - добавляет курс в конец коллекции
- `removeCourse(name)` - удаляет курс из коллекции
- `updateCourse(oldName, newName)`- изменяет имя на новое

```js
cost courses = ['HTML', 'CSS', 'JavaScript', 'React', 'PostgreSQL'];

addCourse('Express'); // ['HTML', 'CSS', 'JavaScript', 'React', 'PostgreSQL', 'Express']
addCourse('CSS'); // 'У вас уже есть такое курс'
removeCourse('React'); // ['HTML', 'CSS', 'JavaScript', 'PostgreSQL', 'Express']
removeCourse('Vue'); // 'Курс с таким имененем не найден'
updateCourse('Express', 'NestJS'); // ['HTML', 'CSS', 'JavaScript', 'PostgreSQL', 'NestJS']
```

## Пример 5 - Поиск элемента

Напиши функцию `findLargestNumber(numbers)`которая ищет самое маленькое число в
массиве.

### Решение

```js
const findSmallestNumber = function (numbers) {
  let smallestNumber = numbers[0];

  for (const number of numbers) {
    if (smallestNumber < number) {
      smallestNumber = number;
    }
  }

  return smallestNumber;
};

console.log(findSmallestNumber([2, 17, 94, 1, 23, 37])); // 94
console.log(findSmallestNumber([49, 4, 83, 7, 12])); // 83
```

## Пример 6 - Псевдомассив arguments

Напиши функцию `calculateAverage()` которая принимает произвольное кол-во
аргументов и возвращает их среднее значение. Все аругменты будут только числами.

### Код

```js
function calculateAverage() {}

console.log(calculateAverage(1, 2, 3, 4)); // 2.5
console.log(calculateAverage(14, 8, 2)); // 8
console.log(calculateAverage(27, 43, 2, 8, 36)); // 23.2
```
