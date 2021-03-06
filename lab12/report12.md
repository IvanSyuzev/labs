# Отчет по лабораторной работе №12

### Цель работы

Изучить основы программирования в оболочке ОС UNIX, научиться писать более сложные командные файлы с использованием логических управляющих конструкций и циклов

### Ход выполнения работы

#### 1. Написали командный файл, реализующий упрощенный механизм семафоров, и протестировали его

![photo1](https://sun9-44.userapi.com/s/v1/if2/x339-oFSx2cT2zvg8hvwjTAHMBYOERA8SyDTMpNy5YKbqrU2g4nFiK_g_bzvlyMU9RBtg8Yyq5a2NxlCICF4Nlr7.jpg?size=405x296&quality=96&type=album)
![photo2](https://sun9-38.userapi.com/s/v1/if2/KWFPRROIdPXW6_TeZOExphfrUeN6aftg602_dhuJHDo5Sy8Kep3UObaLMTN6-pmrvL-BDX_W-2P34U5S4Uacfa-r.jpg?size=172x125&quality=96&type=album)

#### 2. Реализовали команду man с помощью командного файла

![photo3](https://sun9-84.userapi.com/s/v1/if2/lJQYxCBC2jnTAia71mD6LW9EKB9ZzXZ79as3bfy08Q4JxEfFtQQMI3Mro3iWVAZ4ldPIrzBvGx6fGn4lJmDccxWP.jpg?size=406x137&quality=96&type=album)
![photo4](https://sun9-83.userapi.com/s/v1/if2/Dwf8LQijmFWZSOGk-DbEtAFS9bXZijugVuVLTbHzeiO9vgLvntkYml409Vn78vZ15g_QFWksFPYE-jgS_clZl1T2.jpg?size=212x35&quality=96&type=album)

#### 3. Используя встроенную переменную RANDOM написали командный файл, генерирующий случайную последовательность букв латинского алфавита

![photo5](https://sun9-27.userapi.com/s/v1/if2/s2x5bmgSXJ-1fTVGTtHvTP3T5mQIiH4L72tNTVrVu0pSf-YFXABhObGE_wA9zy7kf-GOSIStWsqwX2Q4uPWlbjAg.jpg?size=404x158&quality=96&type=album)
![photo6](https://sun9-82.userapi.com/s/v1/if2/fqd9EmKuckW19e1Nf2dIHyDZzCNtxTJKWJejsYjGXTWAaSertl3FUfErnhRN08iOWMq0frjPgj6CBBlYr4H06HT7.jpg?size=161x22&quality=96&type=album)

### Выводы

В ходе выполнения лабораторной работы я изучил основы программирования в оболочке ОС UNIX и научился писать более сложные командные файлы с использованием логических управляющих конструкций и циклов

### Ответы на контрольные вопросы

#### 1. 

while [$1 != "exit"]

В данной строчке допущены следующие ошибки:

- не хватает пробелов после первой скобки [и перед второй скобкой ]

- выражение $1 необходимо взять в “”, потому что эта переменная может содержать пробелы.

- Таким образом, правильный вариант должен выглядеть так: while [“$1”!= "exit"]

#### 2. 

Чтобы объединить несколько строк в одну, можно воспользоваться несколькими способами:

Первый:
VAR1="Hello,

"VAR2=" World"

VAR3="$VAR1$VAR2"

echo "$VAR3"

Результат: Hello, World

Второй:
VAR1="Hello, "

VAR1+=" World"

echo "$VAR1"

Результат: Hello, World

#### 3. 
Команда seq в Linux используется для генерации чисел от ПЕРВОГО до ПОСЛЕДНЕГО шага INCREMENT.

Параметры:

- seq LAST: если задан только один аргумент, он создает числа от 1 до LAST с шагом шага, равным 1. Если LAST меньше 1, значение is не выдает.

- seq FIRST LAST: когда заданы два аргумента, он генерирует числа от FIRST до LAST с шагом 1, равным 1. Если LAST меньше FIRST, он не выдает никаких выходных данных.

- seq FIRST INCREMENT LAST: когда заданы три аргумента, он генерирует числа от FIRST до LAST на шаге INCREMENT . Если LAST меньше, чем FIRST, он не производит вывод.

- seq -f «FORMAT» FIRST INCREMENT LAST: эта команда используется для генерации последовательности в форматированном виде. FIRST и INCREMENT являются необязательными.

- seq -s «STRING» ПЕРВЫЙ ВКЛЮЧЕНО: Эта команда используется для STRING для разделения чисел. По умолчанию это значение равно /n. FIRST и INCREMENT являются необязательными.

- seq -w FIRST INCREMENT LAST:эта команда используется для выравнивания ширины путем заполнения начальными нулями. FIRST и INCREMENT являются необязательными.

#### 4. 
Результатом данного выражения $((10/3))будет 3, потому что это целочисленное деление без остатка.

#### 5. 
Отличия командной оболочки zshот bash:

- В zsh более быстрое автодополнение для cdс помощью Тab

- В zsh существует калькулятор zcalc, способный выполнять вычисления внутри терминала

- В zsh поддерживаются числа с плавающей запятой

- В zsh поддерживаются структуры данных «хэш»

- В zsh поддерживается раскрытие полного пути на основе неполных данных

- В zsh поддерживаетсязаменачастипути

- В zsh есть возможность отображать разделенный экран, такой же как разделенный экран vim

#### 6. 
for((a=1; a<= LIMIT; a++)) синтаксис данной конструкции верен, потому что, используя двойные круглые скобки, можно не писать $ перед переменными ().

#### 7. 
Преимущества скриптового языка bash:

- Один из самых распространенных и ставится по умолчаниюв большинстве дистрибутивах Linux, MacOS

- Удобное перенаправление ввода/вывода

- Большое количество команд для работы с файловыми системами Linux

- Можно писать собственные скрипты, упрощающие работу в Linux

Недостатки скриптового языка bash:

- Дополнительные библиотеки других языков позволяют выполнить больше действий

- Bash не является языков общего назначения

- Утилиты, при выполнении скрипта, запускают свои процессы, которые, в свою очередь, отражаются на быстроте выполнения этого скрипта

- Скрипты, написанные на bash, нельзя запустить на других операционных системах без дополнительных действий.
