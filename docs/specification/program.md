# Програма

Програмою вважаються файли з розширенням .бр та .барвінок

!!! info "Важливо"
    Файл має бути закодований в UTF-8

## Структура програми

Програма складається з інструкцій(оголошення функцій, інструкції якщо, циклу, тощо) та виразів(присвоєння змінній значення, змінних, отримання атрибутів, літерали, виклики функції).

## Зони видимості

Все, що визначається за межами функції, належить до глобальної зони видимості. Тоді як, все, що визначається в межах функції, належить до локальної зони видимості.

``` periwinkle
число = 20 // глобальна зона видимості

функція тест() // функція теж належить до глобальної зони видимості
    стрічка = "Привіт, світ" // локальна зона видимості
кінець
```


## Виконання коду

У Барвінку немає поняття точки входу в програму, тому код виконується в порядку написання.

``` periwinkle
привітання = "Привіт, %ім'я%" // Виконання програми почнеться тут
друклн(привітання)
```