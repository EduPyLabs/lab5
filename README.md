# Лабораторна робота 5
## Завдання 1
Натуральне число називається [досконалим](https://uk.wikipedia.org/wiki/%D0%94%D0%BE%D1%81%D0%BA%D0%BE%D0%BD%D0%B0%D0%BB%D0%B5_%D1%87%D0%B8%D1%81%D0%BB%D0%BE), якщо воно дорівнює сумі всіх своїх дільників,
крім самого цього числа (наприклад, числа 6 i 28: 6=1+2+3, 28=1+2+4+7+14).

Натуральне число називається [щасливим](https://uk.wikipedia.org/wiki/%D0%A9%D0%B0%D1%81%D0%BB%D0%B8%D0%B2%D0%B5_%D1%87%D0%B8%D1%81%D0%BB%D0%BE), якщо послідовність, яка починається з цього числа,
і кожен наступний член якої є сумою квадратів цифр попереднього, містить член рівний одиниці.

Написати програму, яка визначає усі щасливі досконалі числа у проміжку від `М` до `N`
(`М` і `N` вводяться з клавіатури). 

Результат має виводитися *через кому по 5 чисел в одному рядку*.
Рядок від рядка відділяється *крапкою з комою*. В кінці всієї послідовності має стояти *крапка*.

Якщо в заданому користувачем проміжку *немає жодного такого числа*, то має виводитися порожня стрічка (без крапки).

Доктести:
```python
import doctest


def search_perfect_happy_number(m: int, n: int) -> None:
    """

    :param m: int
    :param n: int


    >>> search_perfect_happy_number(-12, -10)
    Границі проміжку мають бути невід'ємними числами

    >>> search_perfect_happy_number(-12, 10)
    Границі проміжку мають бути невід'ємними числами

    >>> search_perfect_happy_number(12, -10)
    Границі проміжку мають бути невід'ємними числами

    >>> search_perfect_happy_number(1, 100)
    28.
    
    """
    # Ваш код реалізації функції

```

## Завдання 2
Скласти програму [наближеного обчислення](https://uk.wikipedia.org/wiki/%D0%A7%D0%B8%D1%81%D0%BB%D0%BE_%D0%BF%D1%96) числа $\pi$ з заданою точність $\epsilon$ ($\epsilon$ задається користувачем з клавіатури):
- за формулою ряду Лейбніца:

$$
\pi = 4   (1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + ...)
$$


- за формулою Валліса:

$$
{\displaystyle {\frac {2}{1}}\cdot {\frac {2}{3}}\cdot {\frac {4}{3}}\cdot {\frac {4}{5}}\cdot {\frac {6}{5}}\cdot {\frac {6}{7}}\cdot {\frac {8}{7}}\cdot {\frac {8}{9}}\cdots ={\frac {\pi }{2}}}
$$


Програма повинна виводити на екран значення числа $\pi$ з заданою точність $\epsilon$ і кількість доданків/множників,
які було взято для отримання результату, у формі:
```
The Gregory formula gives value (value1} with the accuracy (accuracy) by using (N1} members of series.
The Vallis formula gives value (value2} with the accuracy (accuracy) by using (N2) members of series.
```

Доктести:

```python
import doctest


def pi_gregory_vallis(eps: float) -> None:
    """

    :param eps: float


    >>> pi_gregory_vallis(-0.0002)
    Точність має бути більшою за 0

    >>> pi_gregory_vallis(0.9)
    The Gregory formula gives value 4 with the accuracy 0.14 by using 1 members of series.
    The Vallis formula gives value 4 with the accuracy 0.14 by using 1 members of series.

    >>> pi_gregory_vallis(0.01)
    The Gregory formula gives value 3.1315929036 with the accuracy 0.01 by using 100 members of series.
    The Vallis formula gives value 3.119167469083 with the accuracy 0ю01 by using 100 members of series.

    """

    # Ваш код реалізації функції
```


## Завдання 3
Знайти значення 

$$
S_n = \sum_{k=1}^n \frac{5^k}{(a^k + b^k)k!},
$$

для заданого з клавіатури значення `n`, де

$$
a_1 = 1, \ a_2 = 1, \  a_k = \frac{a_{k-1}}{k} +a_{k-2}b_k
$$

$$
b_1 = 0, \ b_2 = 1, \ b_k = b_{k-1} + a_{k-1}
$$

> Для розрахунків можна використовувати лише один цикл.
> Результати заокруглити до десятитисячних.

Доктести:
```python
import doctest


def calculate_s(n: int) -> None:
    """

    :param n: int


    >>> calculate_s(-2)
    Число n має бути більше за 1

    >>> calculate_s(0)
    Число n має бути більше за 1

    >>> calculate_s(3)
    16.0576

    """

    # Ваш код реалізації функції
```


## Завдання 4
Скласти програму для обчислення визначника порядку `n` (задається користувачем з клавіатури),
який має таку структуру:

 * На головній діагоналі стоять **одиниці**;

 * Над і під головною діагоналлю стоять **двійки**.

```python
import doctest


def determinant_solver(n: int) -> None:
    """

    :param n: int


    >>> determinant_solver(-2)
    Визначник має бути більшим за 0

    >>> determinant_solver(1)
    1

    >>> determinant_solver(2)
    -3

    >>> determinant_solver(3)
    5

    >>> determinant_solver(4)
    -7
    """

    # Ваш код реалізації функції
```