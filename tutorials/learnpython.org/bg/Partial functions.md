Можете да създадете частични функции в Python, като използвате функцията partial от библиотеката functools.

Частичните функции позволяват извеждането на функция с x параметри до функция с по-малко параметри и фиксирани стойности за ограничения вариант.

Необходимо е импорт:

    from functools import partial

Този код ще върне 8.

    from functools import partial
    
    def multiply(x, y):
            return x * y
    
    # създайте нова функция, която умножава по 2
    dbl = partial(multiply, 2)
    print(dbl(4))

Важно забележка: първоначалните стойности ще започнат да заменят променливите отляво. 2 ще замени x. y ще бъде равно на 4, когато се извика dbl(4). Това няма значение в този пример, но има в примера по-долу.

Exercise
--------
Редактирайте предоставената функция, като извикате partial() и замените първите три променливи в func(). След това отпечатайте с новата частична функция, използвайки само една входна променлива, така че резултатът да бъде равен на 60.