# Кортеж

Тип даних Кортеж дозволяє зберігати послідовність об'єктів не залежно від їхнього типу, але на відміну від списків, кортеж після ініціалізації змінити неможливо. Оголошення кортежу в Барвінку має наступний синтаксис:

``` periwinkle linenums="0"
Кортеж(елементи...)
```

## Ітератор кортежу

Кортеж реалізовує [ітератор](../iterators.md), який обходить його елементи зліва направо.

## Оператори

### оператор `рівно` та `нерівно`
порівнює кортежі поелементно

``` periwinkle linenums="0"
Кортеж(1, 2, 3) рівно Кортеж(1, 2, 3) ! істина
Кортеж(1, 2, 3, 4) рівно Кортеж(1, 2, 3) ! хиба
```

## Атрибути

+ `#!periwinkle Кортеж.розмір()` - Повертає кількість елементів в кортежу.
+ `#!periwinkle Кортеж.знайти(обєкт)` - Повертає індекс першого входження об'єкта в кортежу. Якщо елемента з таким індексом не існує, то поверне -1.
+ `#!periwinkle Кортеж.кількість(обєкт)` - Повертає кількість елементів в кортежу, які рівні переданому об'єкту.
+ `#!periwinkle Кортеж.містить(елемент)` - Перевіряє, чи кортеж містить заданий елемент.
+ `#!periwinkle Кортеж.отримати(індекс)` - Повертає елемент з кортежу по індексу. Викидає помилку `ПомилкаІндексу`, якщо індекс більший за розмір кортежу.
+ `#!periwinkle Кортеж.зріз(початок, кількість=максимальнеЧисло)` — Повертає новий кортеж, що містить елементи з вихідного кортежу, починаючи з переданого індексу `початок` і охоплюючи задану кількість елементів. Якщо параметр `кількість` не передано, береться максимальна можлива кількість елементів від індексу `початок` до кінця кортежу. Викидає помилку `ПомилкаІндексу`, якщо значення параметра `початок` перевищує розмір кортежу.
