# Класс CLeakyReLULayer

<!-- TOC -->

- [Класс CLeakyReLULayer](#класс-cleakyrelulayer)
    - [Настройки](#настройки)
    - [Обучаемые параметры](#обучаемые-параметры)
    - [Входы](#входы)
    - [Выходы](#выходы)

<!-- /TOC -->

Класс реализует слой, вычисляющий функцию активации `LeakyReLU` для каждого элемента единственного входа.

Имеет формулу:

```c++
f(x) = alpha * x    при x <= 0
f(x) = x            при x > 0
```

## Настройки

```c++
void SetAlpha( float alpha );
```

Установка множителя в случае отрицательного аргумента. По умолчанию равен `0` (аналогично ReLU).

## Обучаемые параметры

Слой не имеет обучаемых параметров.

## Входы

На единственный вход подается блоб с данными произвольного размера.

## Выходы

Единственный выход содержит блоб тех же размеров, что и вход, с результатами функции над его элементами.