# Чек лист чистого кода
Контрольный список разработчика, в основном основанный на книге **"Чистый код" Роберта К. Мартина**

## Содержание :bookmark_tabs:
  - [Именование всего](#Именование-всего-u5272)
  - [Функции](#functions-microscope)
  - [Форматирование](#formatting-rainbow)
  - [Объекты и структуры данных](#objects-and-data-structures-two_men_holding_hands)
  - [Обработка ошибок](#error-handling-interrobang)
  - [Юнит-тесты](#unit-tests-umbrella)
  - [Классы](#class-school_satchel)
  - [Появление](#emergence-green_book)
  - [Параллелизм](#concurrency-arrows_clockwise)
  - [Пахнущий код](#code-smells-speak_no_evil)
  - [Почетные упоминания](#honourable-mentions-basecamp)

<br/>

## Именование всего :u5272:

- [x] **Имя должно раскрывать намерение**
  - Оно должно сообщать, почему объект существует, что он делает и как используется.
  - Имя должно описывать контекст.

- [x] **Избегайте использования аббревиатур**
  - Используйте `hypotenuse` вместо `hp`.

- [x] **Не кодируйте имя с помощью структуры данных**
  - Используйте `accounts` вместо `accountList`.

- [x] **Не используйте имена, которые различаются совсем незначительно**
  - Найдите разницу между `ControllerForEfficientHandlingOfStrings` и `ControllerForEfficientStorageOfStrings` :dancers:

- [x] **Не давайте переменным имена только для удовлетворения компилятора**
  - Не называйте что-то `name1`, потому что `name` уже занято.

- [x] **Избегайте использования шумовых слов**
  - `ProductData` и `ProductInfo` означают примерно одно и то же.
  - Подобно этому, слова, такие как `a`, `an`, `the`, также являются шумовыми словами, например, назвать переменную `product` достаточно, не нужно `theProduct`.
  - Шумовые слова также **избыточны**, используйте `name` вместо `nameString`.

- [x] **Различайте имена таким образом, чтобы читатель знал, к чему обращаться.**

- [x] **Используйте произносимые имена**

- [x] **Используйте легко находимые имена**
  - Используйте константы вместо жестко закодированных значений, `WORK_DAYS_PER_WEEK = 5` вместо просто 5.

- [x] **Добавляйте единицы измерения к имени переменной**
  - Использование `expiryTimeInSeconds` лучше, чем `expiryTime`.

- [x] **Длина имени должна соответствовать размеру его области видимости**
  - Переменная `i` может быть внутри `for loop`, но `i` никогда не должна быть переменной экземпляра.

- [x] **Классы и объекты должны иметь имена существительных или именные фразы.**
  - Избегайте слов, таких как `Manager`, `Processor`, `Data` или `Info` в названии класса.
  - Если имя вашего класса заканчивается на `er`, `or` или `utils`, стоит пересмотреть ответственность класса.
  - Имя класса не должно быть глаголом.

- [x] **Методы должны иметь имена глаголов или глагольных фраз**

- [x] **Когда конструкторы перегружены, старайтесь использовать статические фабричные методы с именами, которые описывают аргументы**
  - `Complex fulcrumPoint = Complex.FromRealNumber(23.0)` лучше, чем `Complex fulcrumPoint = new Complex(23.0)`

- [x] **Выберите одно слово для одной абстрактной концепции и придерживайтесь его**
    - Например, запутанно иметь `fetch`, `retrieve` и `get` как эквивалентные методы разных классов.

- [x] **Не добавляйте излишний контекст**
  - Для приложения "Gas Station Deluxe" плохая идея префиксировать каждый класс `GSD`.
  - Например, используйте `AccountAddress` вместо `GSDAccountAddress`.

- [x] **Допустимо использовать термины компьютерных наук, названия алгоритмов, шаблонов, математические термины**
  - Постоянное использование проблемной области для выбора имен может привести к усложнению, поэтому при необходимости можно использовать имена из области решений.

- [x] **Добавляйте к имени не больше контекста, чем необходимо**
  - Более короткие имена обычно лучше длинных, если они ясны.

<br/>
