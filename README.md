# Основы разработки на Python
___
___
## Задача 1. Предподготовка
Откройте представленный файл в Jupyter Notebook и выполните предложенную там практическую работу. Эта практика содержит подсказки для самопроверки, сдавать её куратору не нужно. Если у вас возникнут трудности с выполнением, можете задать вопросы через форму для сдачи практической работы.
___
## Задача 2. Числа Фибоначчи
Напишите функцию `get_fib_numbers(qty)`, которая возвращает список, содержащий числа Фибоначчи. Аргумент `qty` определяет количество вычисляемых чисел Фибоначчи.

```python
def get_fib_numbers(qty): 
    # Вставьте свой код здесь.
    pass 
 
fib_numbers = get_fib_numbers(10) 
assert len(fib_numbers) == 10 
print(fib_numbers) 
```
**Пример вывода программы:**

```bash
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```
___
## Задача 3. FizzBuzz 
Реализуйте игру FizzBuzz. 

#### Описание игры: 
пользователь вводит максимальное число, после чего программа выводит значения в соответствии со следующими правилами:

Максимальное число должно быть не меньше единицы.
Каждое число выводится в новой строке, начиная с единицы и последовательно увеличиваясь на один.
Если число делится на три, оно заменяется на fizz, если число делится на пять, то произносится buzz.
Числа, делящиеся на три и пять одновременно, заменяются на fizz buzz. 
При достижении максимального числа мы выводим число в соответствии с правилами и завершаем программу. 

**Входные данные**
```bash
Введите максимальное число: 6
```
**Вывод программы**
```bash
Результат:
1
2
fizz
4
buzz
6
```
**Входные данные**

```bash
Введите максимальное число: 0
```
**Вывод программы**

```bash
Максимальное число должно быть не меньше 1
```
#### Рекомендации
Создайте функцию `fizz_buzz(max_number)`, которая выводит строки согласно правилам игры.
Используйте конструкцию `try...except` для проверки того, что введено целое число.
___
## Задача 4. Решение треугольника
Исторически решением треугольников называется задача отыскания всех остальных сторон и углов треугольника помимо известных. В этой задаче на вход подаются три стороны треугольника. Найдите все углы треугольника, а также его периметр и площадь. Обратите внимание, что сначала необходимо проверить, образуют ли эти три стороны треугольник. 

**Входные данные**
```bash
Введите сторону 1: 3 
Введите сторону 2: 4 
Введите сторону 3: 5 
```
**Вывод программы**
```bash
Угол 1 = 36.87
Угол 2 = 53.13
Угол 3 = 90.00
Периметр треугольника = 12.000
Площадь треугольника = 6.000
```
#### Рекомендации
Существование треугольника с заданными сторонами можно проверить при помощи проверки неравенства треугольника.

Используйте теорему косинусов для вычисления углов. Реализуйте функцию `angle(a, b, c)`, которая вычисляет угол, лежащий напротив стороны `a`.
Обратите внимание, что угол, вычисляемый при помощи арккосинуса, представлен в радианах и его необходимо преобразовать в градусы.
Для вычисления площади треугольника можно использовать формулу Герона.
Необходимые математические функции (корень, тригонометрические функции, постоянная пи) можно найти в пакете `math`. 
___
## Задача 5. Статистика успеваемости
Организуйте систему расчёта статистик успеваемости студентов. Для начала введите список предметов, после — список фамилий и имён студентов. После для каждого студента выведите оценку в диапазоне от 1 до 10. У вас 10-балльная система оценок.
Когда сбор данных будет завершён, выведите студента с лучшей средней успеваемостью и его средний балл. Также выведите средний балл студентов по каждому предмету.

**Входные данные**
```bash
Введите предмет: математика 
Введите предмет: физика 
Введите предмет: стоп

Введите фамилию и имя студента через пробел: Иванов Иван 
Введите фамилию и имя студента через пробел: Петров Дмитрий
Введите фамилию студента: стоп

Введите оценку по предмету 
Студент Иван Иванов 
математика: 5 
физика: 5 

Студент Дмитрий Петров 
математика: 5 
физика: 3 
```
**Вывод программы**
```bash
Статистика: 
Студент с лучшей успеваемостью 
Иван Иванов: 5.00 

Средний балл по предмету 
математика: 5.00 
физика: 4.00 
```
#### Рекомендации
Для остановки ввода предметов/студентов реализуйте обработку слова `stop`.
Создайте функцию `read_subjects` для ввода предметов, функцию `read_students` для ввода студентов, функцию `read_scores` для ввода оценок студентов, а также функцию `statistics` для определения студента с лучшей успеваемостью.
Фамилию и имя студента удобно хранить в виде кортежа: (фамилия, имя).
Для хранения оценок может оказаться полезным использование списка словарей: каждый словарь хранит оценки только одного студента, а ключи в словаре — это названия предметов.
___
## Задача 6. Простые числа
Введите максимальное число. Выведите все простые числа, которые не превосходят это число. Если само число является простым, то выведите и его. 
При решении используйте метод «Решето Эратосфена». В каждой строке выведите числа, принадлежащие одному десятку. 

**Входные данные**
```bash
Введите максимальное число: 20
```
**Вывод программы** 
```bash
Простые числа: 
2, 3, 5, 7, 
11, 13, 17, 19 
```
#### Рекомендации
Основная идея метода «Решето Эратосфена» — проверять числа на делимость, используя только простые делители.
Можно ограничить решение числом 1000. То есть максимальное простое число не должно превосходить 1000.
___
## Задача 7. «Война и мир»
Вам дан файл `war_and_peace.txt` с романом Льва Толстого «Война и мир».
Прочитайте файл и посчитайте статистику по буквам и символам. Необходимо вычислить частоту встречаемости символов — отношение количества этих букв в тексте к количеству всех символов во всём тексте.
Выведите 10 первых предложений, содержащих имя Андрей (формы «Андрея», «Андрею» и другие вариации). Для упрощения будем считать, что предложение начинается с окончания предыдущего «. » и заканчивается точкой «.».

**Вывод программы**
```shell
Статистика:
а : 0.05
б : 0.03
в : 0.03
. : 0.01
! : 0.01

Предложения со словом «Андрей»:
Новое лицо это был молодой князь Андрей Болконский, муж маленькой княгини.
Князь Андрей зажмурился и отвернулся.
```
#### Рекомендации
Используйте словарь для хранения статистики по символам и буквам. Сначала найдите количество символов в тексте, а после того как весь текст будет проанализирован, разделите каждое значение на общее число символов.
Для поиска предложений можно использовать функцию `split`.
___
## Задача 8. Калькулятор
Сделайте калькулятор, который поддерживает четыре операции: сложение (+), умножение (×), вычитание (−), деление (÷).
Калькулятор должен поддерживать операции с целыми числами и числами с плавающей точкой, а также должен быть толерантен к пробелам, то есть между операндами и числами может быть неограниченное число пробелов.

### Как работает калькулятор
Вы указываете имя файла, содержащего выражения, которые нужно вычислить. Одно выражение — одна строка. Если в выражении есть ошибки, калькулятор запоминает номера строк, в которых они встретились. 
Калькулятор выводит результаты расчётов, номер строки и результат вычисления, а также количество ошибок, номера строк, в которых они встретились, и тип ошибок. 

**Входные данные**
```bash
exprs.txt
2 + 3
-5 * 4
a+ 5
```
**Вывод программы**
```bash
results.txt
1 5
2 -20

errors.txt
3 name 'a' is not defined
```
### Рекомендации
Создайте отдельные функции для вычисления выражения, чтения данных, вывода данных, вывода ошибок в файл.
Рекомендуем использовать конструкцию `try…except` для отлавливания исключений.
В самом простом варианте можно использовать функцию `eval(str)` для исполнения выражения, находящегося в строке `str`. Также можно использовать функцию `parse_expr(str)` из пакета `sympy`, с которой мы подробнее познакомимся в следующих модулях.
___
___
# Модуль пройден
* Все задания выполнены. 
* Созданный код приложен к настоящей ветке репозитория.
