# Laboratory work 2.1. Dynamic memory and structures
Задача 1 

Требуется реализовать функцию, которая распечатывает в выходной файл время, и решить с её помощью тестовую задачу. Функция должна иметь сигнатуру: void printTime (int h , int m , int s ); Здесь h — количество часов (от 0 до 23), а m и h — количество минут и секунд соответственно (от 0 до 59)

Задача 2 

Требуется реализовать функцию, будет считывать время из заданной строки.
Функция должна иметь сигнатуру:
int readTime ( char * iStr , int * oHours , int * oMinutes , int * oSeconds );
Здесь iStr — указатель на строку, в которой должно быть записано время. Параметры
oHours, oMinutes, oSeconds — выходные параметры, т.е. вызывающий должен передать в них
указатель на свои локальные переменные, куда будет записаны соответсвующие результаты:
*oHours — количество часов, oMinutes — количество минут, oSeconds — количество секунд.
Функция должна возвращать код возврата: 1, если прочитать время удалось, и 0 в случае
неудачи.
Параметры oMinutes, oSeconds опциональные: вызывающий может передать в них NULL,
если его, например, не интересует количество секунд. При этом если указатель oMinutes
нулевой, то и указатель oSeconds тоже должен быть нулевой.
Время записано в формате H:M:S или H:M. То есть строка состоит из двух или трёх
частей, отделённых друг от друга одним двоеточием. Каждая часть — это целое число из
одной или двух цифр, возможно с ведущими нулями. При этом если задано две части, то это
часы и минуты, а если три — то это часы, минуты и секунды. Заметим, что часы должны
быть в диапазоне до 0 до 23, а минуты и секунды в диапазоне от 0 до 59.
Используя функцию, нужно решить тестовую задачу. В файле записана тестовая строка
длины от 3 до 15 символов без пробелов. Нужно применить функцию readTime к каждой
строке и распечатать результат её вызова.
Нужно вызвать функцию три раза:
1. Указатели oHours, oMinutes, oSeconds ненулевые. После вызова нужно распечатать
код возврата и числа *oHours, *oMinutes, *oSeconds через пробел.
2. Указатель oSeconds нулевой. После вызова нужно распечатать код возврата и числа
*oHours, *oMinutes через пробел.
3. Указатели oMinutes и oSeconds нулевые. После вызова нужно распечатать код возврата
и число *oHours через пробел.
Заметим, что вызывать функцию три раза подряд по сути бессмысленно: мы делаем это
только для того, чтобы протестировать все случаи с нулевыми указателями
