# Стрічка

Стрічка - це послідовність символів. В коді записується за допомогою символів в UTF-8 у подвійних лапках:

``` periwinkle linenums="0"
"привіт"
```

## Екранування, спеціальні символи

За допомогою символу "\" в стрічку можна вписати спеціальні символи. У Барвінку для поліпшення ергономіки спеціальні символи мають як англійський варіант, так і українську версію.

### Таблиця спеціальних символів

| Символ | Українізована версія | Опис |
| ------ | -------------------- | ---- |
| \"     |                      | Вставляє в стрічку символ `"`                                               |
| \\\\   |                      | Вставляє в стрічку символ `\`                                               |
| \a     | \а                   | Звуковий сигнал                                                             |
| \b     | \б                   | Вставляє в стрічку символ `Backspace`                                       |
| \f     | \ф                   | Перехід на нову сторінку(Після використання символу, принтер продовжує друкування з нової сторінки. В консолі зазвичай працює як `\в`.)     |
| \n     | \н                   | Перехід на новий рядок                                                      |
| \r     | \р                   | Повернення каретки(переміщує каретку до лівого краю)                        |
| \t     | \т                   | Табуляція(відступ)                                                          |
| \v     | \в                   | Вертикальна табуляція(переміщення на один рядок униз у тому самому стовпці) |
| \0     |                      | Вставляє в стрічку нульовий символ                                          |


## Конкатенація

Конкатенація проходить за допомогою оператора `+`

``` periwinkle linenums="0"
друклн("число " + 1) // Виведе в консоль "число 1"
```

В стрічках оператора `+` перевантажений так, що він може приймати будь який тип об'єкта, якщо в ньому реалізований метод `toString`, винятком є тип [Нич](null.md)

``` periwinkle linenums="0" title="конкатенація.бр"
друклн("" + нич)
```
Виведе:
``` console linenums="0"
$ барвінок конкатенація.бр
 На стрічці 1 знайдено помилку
 ПомилкаТипу: Непідтримувані типи операндів "String" та "Null" для оператора +
```

## Атрибути

+ `#!periwinkle Стрічка.довжина()` - Повертає кількість символів в стрічці.