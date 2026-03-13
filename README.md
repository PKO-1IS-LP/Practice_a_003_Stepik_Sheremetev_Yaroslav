# Stepik
# 2.1 Объекты и переменные
## Задания:
1.
```
name = "Ярослав"
courses_completed = 1
```
2.
```
# hello, world!
```

# 3.1 Числа 1
## Задания:
1.
```
num1 = 20 + 30
num2 = 50 - 40
num3 = 4 * 5.0
num4 = 120 / 3
```
2.
```
result1 = chest1 + chest2
result2 = chest1 - chest2
result3 = chest1 * chest2
result4 = chest1 / chest2
```
3.
```
print(100)
print(200)
```
4.
```
print("2 4 6 8")
print("1 3 5 7 9")
```
5.
```
print("1")
print("1 1")
print("1 1 1")
print("1 1")
print("1")
```
6.
```
radius_of_my_wheel = 30
average_speed_of_my_car = 140
this_number_is_very_big_but_i_love_it = 1234567890987654321

print(radius_of_my_wheel, average_speed_of_my_car, this_number_is_very_big_but_i_love_it)
```
7.
```
balance = 789
balance = balance + 567
balance = balance - 456
print(balance)
```
8.
```
r, g, b = 255, 100, 0
age, weight, height = 24, 70, 175
line_length, radius, diagonal = 15, 60, 120
len_of_car = len_of_sofa = len_of_carpet = 1.37

print(r, g, b, age, weight, height,
      line_length, radius, diagonal,
      len_of_car, len_of_sofa, len_of_carpet)
```

# 3.2 Числа 2
## Задания:
1.
```
squidward = -5
patrick_starfish = 4
spongebob = 25

print(squidward ** 2, patrick_starfish ** 2, spongebob ** 2)
```
2.
```
mr_krabs = 4
gary = 9
sandy = 16

print(mr_krabs ** 0.5, gary ** 0.5, sandy ** 0.5)
```
3.
```
print(friend_count // 4)
```
4.
```
minutes = number // 60
seconds = number % 60
print(minutes, seconds)
```
5.
```
# Переменная cake_number уже создана, просто используйте её в своём коде
alon = cake_number // 100000
van_dama = (cake_number // 10000) % 10
stal_one = (cake_number // 1000) % 10
jecki_kachan = (cake_number // 100) % 10
chack_no_rise = (cake_number // 10) % 10
bruslya = cake_number % 10
```
6.
```
a = (20 + 20) * 2        # должно получиться 80
b = 2 ** (2 + 1)         # должно получиться 8
c = 3 * (3 ** (2 + 1))   # должно получиться 81
d = 2 ** 2 * -2       # должно получиться -8

print(a, b, c, d)
```
6.
```
print(kassa == check)
```
7.
```
print(150 <= height <= 190)
```
8.
```
print(exam_score != 2)
```

# 4.1 Строки 1
## Конспект:
### Аргументы
Аргументы — это объекты, которые мы передаем в функцию print() при её вызове. Это могут быть строки, числа, списки и любые другие типы данных.
```
print("строка", 123)  # "строка" и 123 - это аргументы функции print()
```

### Параметры end и sep
```
print("Привет", "Мир", sep=" ", end="\n")
```
Параметры end и sep можно представлять как переменные, значения которых влияют на поведение функции print(). Вы можете установить эти значения самостоятельно, чтобы поменять поведение функции print().

По умолчанию sep равен " ", а end равен "\n", ниже мы поговорим подробнее о том, что это значит.

### Параметр end
В Python существуют специальные символы и один из них, это \n — символ переноса строки. Также, в Python существует понятие курсора, на подобие курсора в текстовом редакторе.

Параметр end по умолчанию равен "\n", что означает перенос курсора на следующую строку. Когда все объекты, указанные в print() выведены на экран, курсор оказывается в конце текста и в этот момент активируется параметр end (с англ. "конец") и переносит курсор на следующую строку (абзац). Посмотрите на пример:
```
print("Привет")
print("Мир")
# Привет
# Мир
```
                  
Сначала мы выводим на экран слово Привет, курсор оказывается после символа т, затем активируется end и переносит курсор на следующую строку (абзац). Именно поэтому слово Мир начинается с новой строки, постарайтесь хорошенько понять это. Давайте поменяем значение end и посмотрим как изменится поведение.
```
print("Здравствуйте", end=" ")
print("Дорогие", end=" ")
print("Друзья")

# Здравствуйте Дорогие Друзья
```
                  
В примере, первая команда выводит на экран слово Здравствуйте, курсор остаётся за буквой е. Активируется параметр end и вставляет то, что мы ему указали, то есть один пробел " ". После слова Дорогие произойдёт то же самое. То есть после буквы е вставится пробел и курсор переместится на один пробел вперёд. Слово Друзья начнётся на той же строке, а по окончанию курсор переместится на следующую строку, так как end мы здесь не указали и сработает значение по умолчанию равное \n.

Для закрепления, посмотрите на другой пример ниже и попробуйте сами понять почему так выводится текст:
```
print("Здравствуйте", end=", ")
print("Дорогие", end=" ")
print("Друзья", end="! ")

# Здравствуйте, Дорогие Друзья! 
```
                  
Конечно, можно было написать всё в одну строчку, воспринимайте это только как демонстрацию возможностей end.

### Параметр sep
Параметр sep (сокр. "separator", "разделитель"), активируется в конце каждого объекта, кроме последнего. Он отвечает за то, как будут отделяться друг от друга аргументы на экране. Посмотрите пример:
```
print("Здравствуйте", "Дорогие", "Друзья")

# Здравствуйте Дорогие Друзья
```
                  
В примере, строки разделены одним пробелом, и это заслуга sep, так как по умолчанию он равен " ", то есть одному пробелу. Если вы хотите изменить поведение sep, нужно явно указать другое значение. Посмотрите на пример:
```
print("Здравствуйте", "Дорогие", "Друзья", sep="\n")

# Здравствуйте
# Дорогие
# Друзья
```
                  
Как мы помним, специальный символ \n переносит курсор на следующую строку, подобно клавише enter при печати на клавиатуре. Сначала выводится строка Здравствуйте, затем активируется sep равный \n и переносит курсор на следующую строку. Поэтому слово Дорогие начинается с новой строки. После слова Дорогие снова активируется sep и переносит курсор на следующую строку. После слова Друзья активируется end, а не sep, так как это слово является последним объектом.

Код написан в одну строчку, но на экране мы видим текст на трёх строках и это заслуга sep="\n". 

### sep и end
В функции print() можно изменить сразу оба параметра, если вам нужно такое поведение. Посмотрите пример:
```
print("Привет", "дорогие", "друзья.", sep="_", end=" ")
print("Как дела?")

# Привет_дорогие_друзья. Как дела?
```
                  
Конечно, в таком коде нет нужды, воспринимайте этот код, как демонстрацию возможностей sep и end.

### Переменная, sep и end
В будущем вы узнаете о функциях и параметрах более подробно. Пока можете воспринимать параметры sep и end − как переменные, в которые можно присваивать только строки. 

Кстати, в переменные можно присвоить и другие переменные. Например:
```
a = "Hello"
b = a
```
                  
В этом случае переменные a и b будут ссылаться на одну и ту же строку "Hello". Если переменная ссылается на строку, то подобный трюк можно сделать и с параметрами sep и end.
```
dots = " ... "
print("Привет", "Как дела?", sep=dots, end=dots)  # Привет ... Как дела? ... 
```
                  
Так как dots является строкой " ... ", то мы можем присвоить в sep и end переменную dots. Не скажу, что это хорошая практика, но такое возможно. Воспринимайте это просто как пример, что такое возможно.
## Задания:
1.
```
bot_response = "Спасибо за вопрос. В ближайшее время с вами свяжется наш сотрудник и поможет вам."
print(bot_response)
```
2.
```
print("Здравствуй, друг!", "Пишу тебе письмо,", "Используя одну строку кода!", sep="\n")
```
3.
```
# исправьте код, меняя  лишь то, что внутри print()
print("Друг,", end=" ")
print("смотри", end=" ") 
print("как я могу!")
```
4.
```
print("Развиваться в чём-то - это как идти в гору по скользкой дорожке.", sep=". ")
print("Даже, чтобы просто устоять - нужно прикладывать усилия.", sep=". ")
print("А для того чтобы идти вверх - нужно ещё больше усилий.", sep=". ")
print("Деградация - это путь вниз с горы по скользкой дорожке.", sep=". ")
print("Чтобы деградировать - достаточно просто расслабиться и скатиться вниз.", sep=". ")
print("Будьте мудрыми, прикладывайте усилия!", sep="! ")
```
5.
```
text = "Дорогой друг! Сегодня я осознал одну вещь: в программировании всегда есть возможность решить задачу разными способами. Это словно разные дороги, ведущие к одному и тому же пункту назначения. Где-то эта дорога прямая и короткая, а где-то извилистая и долгая."

print(text)
```
6.
```
print(r'''Привет, меня зовут Алон Миск, я живу "в ваших сердцах".
Hello, my name is Alon Misk, and I live 'in your hearts'.
C:\Users\new_project\googlik''')
```
7.
```
message1 = input()
print(message1)

message2 = input()
print(message2)
```

# 4.2 Строки 2
## Информация:
# Срез.
```
"строка"[start:stop:step]
```

# Строка.
```
"строка".upper() # делает все буквы заглавными
"строка".lower() # делает все буквы нижним регистром
```

# Replace и тд.
```
.replace(old, new[, count])
          
# old: Подстрока, которую нужно заменить.
# new: Подстрока, на которую нужно заменить old.
# count (необязательный): Количество замен. По умолчанию заменяются все совпадения.
```
```
.strip([chars])

# chars (необязательный): Символы, которые нужно удалить. Если не указан, удаляются пробелы и специальные символы.
# Есть lstrip и rstrip убирающие символы со стороны соответсвующей букве
```

# Поиск в строках.
```
.find(sub[, start[, end]]) 
.index(sub[, start[, end]]) 
     
# sub: подстрока, которую мы ищем. 
# start (необязательный параметр): индекс начала поиска. Если не указывать, то поиск начинается с начала строки.
# end (необязательный параметр): индекс конца поиска. Если не указывать, то поиск производится до конца строки.
```

```
count(x[, start[, end]])
                 
# x: подстрока, которую мы ищем. 
# start (необязательный параметр): индекс начала поиска. Если не указывать, то поиск начинается с начала строки.
# end (необязательный параметр): индекс конца поиска. Если не указывать, то поиск производится до конца строки.
```
## Задания:
1.
```
print(input(), input(), input())
```
2.
```
a = "Люблю "
b = "тебя, "
c = "Эйлинсбург!"

print(a + b + c[0] + c[1] + c[2] + c[3] + c[10])
```
3.
```
a = "Люблю тебя, Петра творенье, "
b = "Эйли Биллиш"
c = " Ты удивительно прекрасна, как изумруд среди песка!"

# ваш код ниже:
message = a[:12] + b[:4] + c[-1] + c[:4] + c[16:25] + c[-1]
print(message)
```
4.
```
code = "HДBрEуYг ,b dяh yсsдbе3л2а9л* #э9т3оb,f bяY Eнbаmпnиxс;аeлw nеeйu!"

print(code[1::2])
```
5.
```
# вариант 2
word = input()
small, big = word.lower(), word.upper()
print(small, big, sep="\n")
```
6.
```
text = input()
text_copy = text[:]
text_copy = text_copy.replace("1", "П").replace("2", "и").replace("3", "е")
print(text_copy)
```
7.
```
password = input()

test1 = password[0].isupper()
test2 = password.isidentifier()
password_check = test1 + test2

print(password_check == 2)
```

# 5.1 Списки
## Информация:
```
[]  # Пустой список
[1, 2, 3, 4.44]  # Числа в списке
["строка1", "строка2"]  # Строки в списке
[переменная1, переменная2]  # Переменные в списке
[[1, 2, 3], [4, 5, 6]]  # Списки внутри списков
[True, False]  # Булевы значения в списке
[input(), input()]  # Функции в списке
[1, 2, "строка1", True, False, переменная1]  # Разные объекты в списке
```
```
list1 = [1, 2, 3]
print(list1[0], list1[1], list1[-1])  # 1 2 3 выбор из списка
```

### Метод .append(object)
Метод append() изменяет оригинал списка, путём добавления одного элемента в конец списка. В скобках вы указываете один аргумент (object), и он добавится в конец списка.
```
my_list = [1, 2, 3]
my_list.append(4)
my_list.append("строка")
my_list.append([5, 6, 7])
print(my_list)  # [1, 2, 3, 4, 'строка', [5, 6, 7]]
```

### Метод .extend(iterable)
Этот метод используется для добавления нескольких элементов в конец списка. Для этого нужно в скобках указать, например список (или другой итерируемый объект, об этом позже). Метод extend() возвращает None, поэтому его нужно только вызвать.
```
my_list = [1, 2, 3]
my_list.extend([4, 5, 6])
print(my_list)  # [1, 2, 3, 4, 5, 6]
```

### Метод .insert(index, object)
Этот метод используется для добавления одного элемента в список по указанному индексу. Метод возвращает None. Метод принимает два аргумента:
```
# index: указываем число, означающее индекс, то есть место, куда нужно вставить элемент.
# object: объект, который вы планируете вставить в список.
my_list = [1, 2, 3]
my_list.insert(1, 5)
print(my_list)  # [1, 5, 2, 3]
```
### Метод .split()
Метод split() преобразует строку в список по указанному разделителю. Рассмотрим синтаксис метода:
```
split([sep[, maxsplit]])

# sep (необязательный): Разделитель в формате строки (например, ", "). Если не указан, строка будет разбита по пробелам.
# maxsplit (необязательный): Максимальное количество разделений. По умолчанию метод разделяет строку на все возможные подстроки.
```
## Задания:
1.
```
rating = ["чудовищно", "не фонтан", "середнячок" , "недурно", "отлично"]
students = ["Dony Jepp", "Mill Buray", "Lorlando Bum"]

print(f"{students[0]} вёл себя сегодня {rating[0]}")
print(f"{students[1]} вёл себя сегодня {rating[1]}")
print(f"{students[2]} вёл себя сегодня {rating[3]}")
```
2.
```
print([5, 1])
```
3.
```
# Список result уже создан волшебным образом
print(f"""Имя: {result[0]}
Предмет: {result[1]}
Количество 1: {result.count(1)}
Количество 2: {result.count(2)}
Количество 3: {result.count(3)}
Количество 4: {result.count(4)}
Количество 5: {result.count(5)}""")
```
4.
```
students = input().split()
print(students)
```
5.
```
all_list = dony_jepp + mill_burey + lorlando_bum
all_list.sort()
print(all_list, all_list[::-1], sep='\n')
```
6.
```
student = []

student.append(["Политология"])
student.append(["Физкультура"])
student.append(["География"])

student[0].extend([5, 5, 5])
student[1].extend([3, 3, 3])
student[2].extend([4, 4, 4])

print(student)
```
7.
```
p1, p2, p3, *p4, p5 = present
print(p1, p2, p3, p4, p5)
```

# 6.1 Встроенные функции
## Информация:

## Задания:
1.
```
number = input().split('.')
number = [int(number[0]), int(number[1])]
print(number)
```
2.
```
list_number = [float(input()), float(input()), float(input())]
print(list_number)
```
3.
```
# переменные num1 и num2 уже созданы, используйте их в вашем коде:
number = str(num1) + str(num2)
number = int(number)
print(number)
```
4.
```
point1 = float(input())  # принимаем от пользователя первую координату
point2 = float(input())  # принимаем от пользователя вторую координату

# ваш код ниже:
distance = abs(point2 - point1)
distance = round(distance, 1)
print(distance)
```
5.
```
# Список data уже создан волшебным образом:

summa = sum(map(int, data[1]))  # количество товаров
price = round(sum(map(float, data[3])) / 3)  # средняя цена
description = ', '.join(data[2])  # описание товаров

print(f'''Название: {data[0]}
Количество: {summa}
Описание товара: {description}
Средняя цена: {price}
Отзыв: {data[4]}''')
```
6.
```
# Переменная exchange_rate уже создана волшебным образом
max_num = max(exchange_rate, default='неизвестно')
min_num = min(exchange_rate, default='неизвестно')

print(f'Максимальное значение валюты: {max_num}')
print(f'Минимальное значение валюты: {min_num}')
```
7.
```
list_grade = list(map(int, input().split()))
result_average = round(sum(list_grade) / len(list_grade))
print(f'Оценка за четверть: {result_average}')
```
8.
```
str_input = input().lower()
sort_str = sorted(str_input)
sort_str = "".join(sort_str)
print(sort_str)
```

# 7.1 Условные и логические операторы
## Информация:

## Задания:
1.
```
if input() == 'start':
    print('Запускаю программу')
```
2.
```
w_1, w_2 = input().lower().split()

if w_1[-1] == w_2[0]:
    print("Слово подходит")
else:
    print("Слово не подходит")
```
3.
```
garbage = input()

if garbage == 'металл':
    print('жёлтый')
elif garbage == 'бумага':
    print('синий')
elif garbage == 'стекло':
    print('зелёный')
elif garbage == 'пластик':
    print('оранжевый')
else:
    print('ручная сортировка')
```
4.
```
list_name = ["Джони Депп", "Джеки Чан", "Билли Айлиш"]
# ваш код ниже:
name = input()
if name not in list_name:
    print("Мошенник!")
```

5.
```
word = input()

if len(word) < 3:
    print(False)
elif word[0].isupper() and word[-1].isdigit() and " " not in word:
    print(True)
else:
    print(False)
```
6.
```

```
7.
```
login, password = input(), input()

if login == "admin":
    if password == "read":
        print("Редактор в режиме чтения")
    elif password == "edit":
        print("Редактор в режиме редактирования")
    else:
        print("Неправильный пароль")
else:
    print(f"Пользователь {login}")
```
8.        
```
if isinstance(request[0],str) or isinstance(request[2],str):
    print("Алон, исправь строки на числа!")
else:
    print("Алон, всё нормально, это числа!")
```

# 8.1 Цикл while и for
## Информация:

## Задания:
1.
```
a = 1
b = 5

while a != b:
    print(a, end=' ')
    a += 1

print(b)
```
2.
```
users, number = list(map(int,input().split()))
count = 1
list = []

while count <= users:
    if count % number == 0:
        list.append(count)
    count += 1

print(list)
```
3.
```
```
4.
```
for i in list_in:
    print(i)
```
5.
```
n = int(input()) + 1
for i in range(n):
    print(i, end=' ')
```
6.
```
num = int(input())

for i in range(1, 10):
    print(f'{num} * {i} = {num * i}')
```
7.
```
for num in sorted(list_num, reverse=True)[:4]:
    print(num, end=' ')
```
8.
```
```
9.
```
result = []

for i in list_in:
    for a in i:
        result.append(a)

print(result)
```

# 8.2 Итератор, функции и for
## Информация:

## Задания:
1.
```
n = int(input())

lcm = 146520

result = []
for i in range(lcm, n + 1, lcm):
    result.append(i)

print(*result)
```
2.
```
my_list = [10, 20, 30, 40]
my_iterator = iter(my_list)

print(next(my_iterator))  
print(next(my_iterator))  

my_iterator = iter(my_list)

print(next(my_iterator))
print(next(my_iterator))
print(next(my_iterator))
print(next(my_iterator))
```
3.
```
total = 0
for game1, game2 in list_in:
    total += game1 + game2
print(total)
```
4.
```
print("№:   Имя:")
for i, name in enumerate(list_q, 1):
    print(f"{i}    {name}")
```
5.
```
estimates = sorted(input().split())
max_est = estimates[-1]  # самая высокая оценка
count = 0  # будем подсчитывать количество высокой оценки

for i in reversed(estimates):  # чтобы в решении было и sorted() и reversed()
    if i < max_est:
        break
    else:
        count += 1

print(f"Самая высокая оценка: {max_est}")
print(f"Количество: {count} шт")
```
6.
```
for sub, est in zip(subjects, estimates):
    est = str(est)[1:-1]  # убирает скобки в строке, например в "[5, 5, 5]"
    print(f'{sub}: {est}')
```
7.
```
list_result = [[], [], [], [], []]

for i in map(int, input().split()):
    list_result[i-1].append(i)

print(list_result)
```

# 9.1 Кортежи и множества
## Информация:

## Задания:
1.
```
result = tuple(input().split())
print(result)
```
2.
```
# Переменные t1 и t2 уже созданы волшебным образом.
result = t1 + t2
print(result)
```
3.
```
# Переменная tuple_orig уже создана волшебным образом.
tuple_orig = tuple(sorted(tuple_orig))
print(tuple_orig)
```
4.
```
# ваш код:
right_answer = tuple(input().split())
person_answer = tuple(input().split())
count = 0

for right, person in zip(right_answer, person_answer):
    if right == person:
        count += 1
        
print(count)
```
5.
```
input_list = input().split()
duplicate_count = 0

for i in set(input_list):
    if input_list.count(i) > 1:
        duplicate_count += 1
        
print(duplicate_count)
```
6.
```
all_checks = set(input().split())
persons_checks = input()

if persons_checks in all_checks:    
    print('Осуществляем возврат')
else:
    print('Такой суммы нет')
```
7.
```
set_pers = set(input().split())

for i in list(set_pers):
    if i[0] == 'Р':
        set_pers.discard(i)

set_pers.add('Алон')
set_pers.add('Эйли')

print(sorted(set_pers))
```
8.
```
s1 = set(input().split())
s2 = set(input().split())
result = s1 | s2
print(sorted(result))
```
9.
```
s1 = set(input().split())
s2 = set(input().split())
reference = set(input().split())

sklad1 = sorted(reference - s1)
sklad2 = sorted(reference - s2)

print('Склад 1:', sklad1)
print('Склад 2:', sklad2)
```
10.
```
str1 = input().split()
str2 = input().split()
str3 = input().split()
str4 = input().split()

count1 = len(set(str1) & set(str4))
count2 = len(set(str2) & set(str3))
rating = count1 + count2

print(rating)
```
11.
```
s1 = set(input().split())
s2 = set(input().split())

for i in sorted(s1 ^ s2):
    print(i, end=' ')
```

# 10.1 Словари
## Информация:

## Задания:
1.
```
data = {"Имя": "Алон", "Работа": "Middle Программист"}
data["Компания"] = "Маркософт"
data["Работа"] = "Junior Программист"
print(data)
```
2.
```
data_in = input().split()
lessons = {}

for i in data_in:
    lessons[i] = []

print(lessons)
```
3.
```
list_lessons = input().split()
dict_lessons = {}

for i in list_lessons:
    num = list(map(int, input().split()))  # принимаем оценки и сохраняем их в список из чисел
    dict_lessons[i] = num  # создаём ключ:значение, где значением будут наши оценки
   
print(dict_lessons)
```
4.
```
s = sorted(input().split())
d = {}

for i in s:
    if i in d:
        d[i] += 1
    else:
        d[i] = 1

print(d)
```
5.
```
description.update(description_new)
print(description)
```
6.
```
search = input()
all_students = class_7A | class_7B | class_3A
print(all_students.get(search, "Такого ученика нет"))
```
7.
```
for key, value in stock.items():
    result = "отсутствует" if value == 0 else f"остаток: {value} шт"
    print(f"Товар: {key}, {result}")
```
8.
```
product = input().split()
stock = dict.fromkeys(product, 0)
print(stock)
```
9.
```
list_names = list(students.keys()) 
l = len(list_names) 

for i in range(l):
    m, f, h = map(int, input().split()) 
    name = list_names[i]  
    
    students[name]["математика"].append(m)
    students[name]["физика"].append(f)
    students[name]["химия"].append(h)

print(students)
```

# 11.1 Функции 1
## Информация:

## Задания:
1.
```
def check_even(number):
    if number % 2 == 0:
        print("Число чётное")
    else:
        print("Число нечётное")

num = int(input())
check_even(num)
```
2.
```
def convert_to_float(string):
    try:
        return float(string)
    except ValueError:
        return None

user_input = input()
result = convert_to_float(user_input)
print(result)
```
3.
```
def check_login_password(login, password, true_login="admin", true_password="admin"):
    if login == true_login and password == true_password:
        print(True)
    else:
        print(False)

user_login = input()
user_password = input()
check_login_password(user_login, user_password)
```
4.
```
def super_sum(*args):
    return sum(args)
```
5.
```
def super_minus(**kwargs):    
    list_value = tuple(kwargs.values())
    result = list_value[0] 
    for value in list_value[1:]:
        result -= value
    return result

num1 = super_minus(n1=10, n2=2, n3=5)  # 10-2-5 = 3
num2 = super_minus(n1=100, n2=20, n3=50, n4=10, n5=10, n6=5)
num3 = super_minus(n1=700, n2=100, n3=300, n4=200) 
```
6.
```
balance = int(input())
price = int(input())

def buy():
    def check_balance():
        if balance >= price:
            return True
        else:
            return False
    
    if check_balance():
        print("Покупка совершена")
    else:
        print("Недостаточно средств")

buy()
```
7.
```
balance = int(input())
price = int(input())

def buy():
    def check_balance():
        return balance >= price
    
    def change_balance():
        global balance
        balance -= price
    
    def show_balance():
        print(f"Ваш баланс: {balance}")
    
    if check_balance():
        print("Покупка совершена")
        change_balance()
        show_balance()
    else:
        print("Недостаточно средств")

buy()
```

# 11.2 Функции 2 (lambda)
## Информация:

## Задания:
1.
```
def input_my_desires(*desires: str) -> None:
    """
    Функция принимает желания пользователя и выводит мотивирующее сообщение.
    
    :param desires: Произвольное количество желаний в виде строк
    :return: None
    """
    print("Ваши желания приняты! А теперь приложите усилия для их исполнения!")

input_my_desires("Стать успешным программистом", "Путешествовать по миру", "Выучить Python")
```
2.
```
def filter_age(item):
    name, age = item
    return 18 <= age <= 30

filtered_names = [name for name, age in filter(filter_age, persons.items())]
filtered_names.sort()
print(filtered_names)
```
3.
```
sorted_persons = sorted(persons, key=lambda x: (x['bad_habits'], -x['age'] if not x['bad_habits'] else 0))
for person in sorted_persons:
    print(person)
```
4.
```
filtered_persons = [person for person in persons if person['rating'] >= 4.5]
sorted_persons = sorted(filtered_persons, key=lambda x: x['name'])
for person in sorted_persons:
    print(person['name'])
```





















