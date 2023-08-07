# seminar-ex
Решение задач на семинаре

********  Задача 0 *************
/* программа, которая на вход принимает число и выдает его квадрат (число умноженное на само себя)
4 - 16
-3 - 9 
*/

Console.Write("Введите целое число: ");
int number = int.Parse(Console.ReadLine() ?? "");

int result = number * number;

Console.WriteLine($"{number} -> {result}");






************* Задача 1 *******************
/* программа, которая на вход принимает 2 числа и проверяет, являетсяли первое число квадратом второго
а=25, в=5 - да
а=2, в = 10 - нет
*/

Console.Write("Введите первое число: ");
int number1 = int.Parse(Console.ReadLine() ?? "");
Console.Write("Введите второе число: ");
int number2 = int.Parse(Console.ReadLine() ?? "");

int number2sq = number2 * number2;
if (number1 == number2sq)
{
    Console.WriteLine("Первое число является квадратом второго");
}
else
{
    Console.WriteLine("Первое число не является квадратом второго");
}





************* Задача 2 ***************
/* программа, которая выдает название дня недели по заданному номеру
 3 - среда
 5 - пятница
 */

Console.Write("Введите число от 1 до 7: ");
int number = int.Parse(Console.ReadLine() ?? "");

if (number == 1)
{
    Console.WriteLine("Понедельник");
}
if (number == 2)
{
    Console.WriteLine("Вторник");
}
if (number == 3)
{
    Console.WriteLine("Среда");
}
if (number == 4)
{
    Console.WriteLine("Четверг");
}
if (number == 5)
{
    Console.WriteLine("Пятница");
}
if (number == 6)
{
    Console.WriteLine("Суббота");
}
if (number == 7)
{
    Console.WriteLine("Воскресенье");
}

if (number < 1)
{
  Console.WriteLine("Число не является днем недели");
}
if (number > 7)
{
    Console.WriteLine("Число не является днем недели");
}





************ Задача 3 *************

/* программа, которая на вход принимает одно число, а на выходе показывает все целые числа в промежутке от -N до N
4 - -4,-3,-2,-1,0,1,2,3,4
2- -2,-1,0,1,2
*/

Console.WriteLine("Введи целое число больше нуля");

string answer1 = Console.ReadLine() ?? "";
int number1 = int.Parse(answer1);

// Проверка корректности ввведеного числа
if (number1 <= 0)
{
    Console.WriteLine("Читай внимательнее, человек!");
    return; //выход из программы
}

// выводим сроку
int i = -number1;
while (i <= number1)
{
    Console.Write($"{i}");
    i = i + 1;
}





**************** Задача 3 ************
/* программа, которая на вход трехзначное число и на выходе показывает последнюю цифру этого числа
456 - 6
782 - 2 
918 - 8
*/

Console.WriteLine("Введи число");

string userInput1 = Console.ReadLine() ?? "";
int a = int.Parse(userInput1);

int i = a % 10;

Console.Write($"{a} -> {i}");





************ Задача 4 ****************
﻿// Задача 4
Console.WriteLine("Введите первое число");
string number1 = Console.ReadLine() ?? "";
int a = int.Parse(number1);

Console.WriteLine("Введите второе число");
string number2 = Console.ReadLine() ?? "";
int b = int.Parse(number2);

Console.WriteLine("Введите третье число");
string number3 = Console.ReadLine() ?? "";
int c = int.Parse(number3);

int max;

if (a > b)
{
    max = a;
}
else
{
    max = b;
}
if (c > max)
{
    max = c;
}

Console.Write("Максимальное число ");
Console.WriteLine(max);






************** Задача 5 ******************
//void (пустота) - процедура которая похожа на функцию, но не возвращает никаких значений
void FillArray(int[] collection) // обозначаем процедуру с названием FillArray (заполнения массива) на вход данной процедуры должен поступать массив
{
    int length = collection.Length;   // целочисленная переменная length (длина) в которую помещаем значение метода Length (возвращает длину или количество элементов массива)
    int index = 0;
    while (index < length)
    {
       collection[index] = new Random() .Next(1, 10);
        //index = index +1
        index ++;
    }
}

void PrintArray(int[] col) // процедура с названием PrintArray(печать массива) для вывода массива в консоле
{
    int count = col.Length; //count - подсчет
    int position = 0;
    while (position < count)
    {
        Console.WriteLine(col[position]);
        position ++;
    }
}

int indexOF(int[] collection, int find) // функция целочисленного числа с названием indexOF, на вход поступают2 переменные: 1 массив, 2 элемент индекс которого мы должны найти
{
    int count = collection.Length; 
    int index = 0;
    int position = -1;
    while (index < count)
    {
        if(collection[index]== find)
        {
            position = index; 
            break; // прерывание цикла
        }
        index++;
    }
    return position; //возвращает значение того же типа данных как и функция, после выполнения данной функции
}

int [] array = new int [10];

FillArray(array); // на вход процедуры мы впускаем массив под названием array который назначили выше
array[4] = 4;
array[6] = 4;

PrintArray(array);
Console.WriteLine();

int pos = indexOF(array, 444);
Console.WriteLine(pos);







*************** Задача 6 ****************
﻿// задача 6: Напишите программу, которая на вход принимает число и выдает, является ли число четным (делится ли оно на два без остатка)

Console.WriteLine("Введите число");
string number = Console.ReadLine() ?? "";
int even = int.Parse(number);

if (even % 2 == 0)
{
    Console.WriteLine("четное");
}
else
{
    Console.WriteLine("не четное");
}




************* Задача 8 *****************
﻿// Напишите программу, которая на вход принимает число N, а на выходе показывает все четные числа от 1 до N

Console.WriteLine("Введите число");
string number = Console.ReadLine() ?? "";
int N = int.Parse(number);
int index = 2;

while(index <= N)
{
    Console.Write($"{index} ");
    index = index + 2;
}





************* Задача 9 ********************
/*программа, которая выводит случайное трехзначное число и удаляет вторую цифру этого числа
456 -> 46
782 -> 72
918 - > 98
*/

int num = new Random ().Next(100,1000);
int a1 = num / 100;
int a2 = num % 10;
int resalt = a1 * 10 + a2;
Console.WriteLine($"num = {num}, resalt = {resalt}");




**************** Задача 10 ***************** 
﻿/* Напишите программу, которая принимает на вход трёхзначное число и на выходе показывает вторую цифру этого числа.
456 -> 5
782 -> 8
918 -> 1
*/

Console.WriteLine("Введите трехзначное число ");
int num = int.Parse(Console.ReadLine() ?? "");

if (num <= 99 || num >= 1000)
{
    Console.WriteLine("Читай внимательнее, человек!");
    return; 
}

int a1 = num / 10;
int a2 = a1 % 10;
Console.WriteLine($"num = {num}, resalt = {a2}");






******************* Задача 11 ******************
/*программа, которая выводит случайное трехзначное число и удаляет вторую цифру этого числа
456 -> 46
782 -> 72
918 - > 98
*/

int num = new Random ().Next(100,1000);
int a1 = num / 100;
int a2 = num % 10;
int resalt = a1 * 10 + a2;
Console.WriteLine($"num = {num}, resalt = {resalt}");




***************** Задача 12 ********************
/* программа, которая принимает на вход2 числа и выводит ,является ли второе число кратным первому. 
Если число 2 не кратно числу 1, то программа выводит остаток от деления. 
34,5 -> не кратно, остаток 4
16,4 -> кратно */

Console.WriteLine("Введите первое число ");
string number1 = Console.ReadLine() ?? "";
int a = int.Parse(number1);

Console.WriteLine("Введите второе число ");
string number2 = Console.ReadLine() ?? "";
int b = int.Parse(number2);

if (a % b == 0)
    Console.WriteLine($"{a}, {b} -> кратно");
else 
    Console.WriteLine($"{a}, {b} -> не кратно, остаток { a % b}");




*************** Задача 13 *********************
﻿/* Напишите программу, которая выводит третью цифру заданного числа или сообщает, что третьей цифры нет.
645 -> 5
78 -> третьей цифры нет
32679 -> 6
*/

Console.WriteLine("Введите число ");
long num = long.Parse(Console.ReadLine() ?? "");    // при вводе больших чисел ошибка: Value was either too large or too small for an Int32. Поэтому стоит long
    
if (num <= 99) 
{
    Console.WriteLine($"num = {num}, resalt = третьей цифры нет");
    return;
}

long s = 1;  //переменная на которую делится N значное число 
while(true)
{
    if (num >= 1000 * s)  //находим насколько нужно разделить число перед нахождением отстатка отделения, чтоб осталось 3 первых цыфры
        s = s * 10;
    else break;
}
    
long a2 = num / s;
a2 = a2 % 10;

Console.WriteLine($"num = {num}, resalt = {a2}");




************** Задача 14 ****************
// Напишите программу,которая принимает на вход число и проверяет,  кратно ли оно одновременно 7 и 23

Console.WriteLine("Введите число ");
int number = int.Parse(Console.ReadLine() ?? "");
int a = 7;
int b = 23;
int c = (number % a) + (number % b); //(a % 7 == 0 && a % 23 == 0)

if (c == 0 )
    Console.WriteLine("Число кратно 7 и 23"); //Console.WriteLine($"{a} -> да")
else 
    Console.WriteLine("Число не кратно 7 и 23");  //Console.WriteLine($"{a} -> нет")




*************** Задача 15 **************
﻿/* Напишите программу, которая принимает на вход цифру, обозначающую день недели, и проверяет, является ли этот день выходным.
6 -> да
7 -> да
1 -> нет
*/

Console.Write("Введите число от 1 до 7: ");
int number = int.Parse(Console.ReadLine() ?? "");

if (number <= 0 || number >= 8)
{
    Console.WriteLine("Читай внимательнее, человек! Такого дня недели не существует!");
    return; 
}
if (number == 1)
    Console.WriteLine("Понедельник "); // можно сократить убрав перечисление дней недели
if (number == 2)
    Console.WriteLine("Вторник ");
if (number == 3)
    Console.WriteLine("Среда ");
if (number == 4)
    Console.WriteLine("Четверг ");
if (number == 5)
    Console.WriteLine("Пятница ");
if (number == 6)
    Console.WriteLine("Суббота ");
if (number == 7)
    Console.WriteLine("Воскресенье ");
if (number <= 5)
  Console.WriteLine("Рабочий день");
if (number >= 6)
    Console.WriteLine("Выходной день");


    


**************    Задача 16 ****************
    // программа, которая принимает на вход 2 числа и проверяет, является ли одно число квадратом другого. (5,25; -4,16; 25,5)

Console.WriteLine("Введите первое число ");
int number = int.Parse(Console.ReadLine() ?? "");
Console.WriteLine("Введите второе число ");
int number2 = int.Parse(Console.ReadLine() ?? "");
int a = number * number;
int b = number2 * number2;

 if (number == b )
    Console.WriteLine("Первое число является квадратом второго");
else if (number2 == a )
     Console.WriteLine("Второе число является квадратом первого");
else 
    Console.WriteLine("Ни одно число не является квадратом другого"); 



************    Задача 18 ****************
    /*программа, которая по заданному номеру четверти, показывает диапозон возможных координат точек в этой четверти (х и у) */


Console.Clear();

int Qvdrnt = GetNumQvdrnt("Введите номер квадранта", "Ошибка ввода данных!");
PrintRange(Qvdrnt);

Console.WriteLine ("Нажмите любую кнопку");
Console.ReadLine();

static int GetNumQvdrnt(string MesWelcome, string ErrMes)       //операция ввода номера квадранта
{
   while (true)
   {
    try
    {
         Console.WriteLine(MesWelcome);
         int NumQvdrnt = int.Parse(Console.ReadLine() ?? "");
         return NumQvdrnt;
    }
    catch (Exception exc)
    {
        Console.WriteLine($"{ErrMes} {exc.Message}");
    }
   }
}

static void PrintRange(int Qvdrnt)
{
if (Qvdrnt == 1) Console.WriteLine ("X = (0...+oo), Y = (0...+oo)");
else if (Qvdrnt == 2) Console.WriteLine ("X = (-oo...0), Y = (0...+oo)");
else if (Qvdrnt == 3) Console.WriteLine ("X = (-oo...0), Y = (-oo...0)");
else if (Qvdrnt == 4) Console.WriteLine ("X = (0...+oo), Y = (-oo...0)");
else Console.WriteLine("Неверно введен номер квадрата");
}




***************** задача 19 ***************
﻿/* Напишите программу, которая принимает на вход пятизначное число и проверяет, является ли оно палиндромом.
14212 -> нет
23432 -> да
12821 -> да
*/

int Prompt(string message)
{
    Console.Write(message);
    string value = Console.ReadLine() ?? "";
    int result = Convert.ToInt32(value);
    return result;
}

void GetNRank(int number)
{
    if (number / 10000 == number %10 && number / 1000 % 10 == number % 100 / 10)
    Console.WriteLine("Число является полиндромом");
    else 
    Console.WriteLine("Число НЕ является полиндромом");
}

bool ValidateNumber(int number)
{
    if (number < 10000 || number > 99999)
    {
        Console.WriteLine("Ошибка ввода числа, попробуй еще");
        return false;
    }
    return true;
}

int number = Prompt("Введите пятизначное число ");
if (ValidateNumber(number))
{
    GetNRank(number);
}




**************** Задача 21 ****************
﻿/* Напишите программу, которая принимает на вход координаты двух точек и находит расстояние между ними в 3D пространстве.
A (3,6,8); B (2,1,-7), -> 15.84
A (7,-5, 0); B (1,-1,9) -> 11.53
*/

int Prompt (string message)
{
    Console.WriteLine(message);
    string value = Console.ReadLine()?? "";
    int result = Convert.ToInt32(value);
    return result;
}

int Xa = Prompt("Введите первое число первой координаты ");
int Ya = Prompt("Введите второе число первой координаты ");
int Za = Prompt("Введите третье число первой координаты ");

int Xb = Prompt("Введите первое число второй координаты ");
int Yb = Prompt("Введите второе число второй координаты ");
int Zb = Prompt("Введите третье число второй координаты ");

Console.WriteLine($"Первая координата: {Xa}{Ya}{Za}");
Console.WriteLine($"Вторая координата: {Xb}{Yb}{Zb}");

Console.WriteLine($"Расстояние между точками координат в 3D пространстве составляет: {Math.Sqrt(Math.Pow((Xa-Xb),2) + Math.Pow((Ya-Yb),2) + Math.Pow((Za-Zb),2))}");




***************** задача 23 *****************
﻿/* Напишите программу, которая принимает на вход число (N) и выдаёт таблицу кубов чисел от 1 до N.
3 -> 1, 8, 27
5 -> 1, 8, 27, 64, 125
*/

int Prompt (string message)
{
    Console.WriteLine(message);
    string value = Console.ReadLine()?? "";
    int result = Convert.ToInt32(value);
    return result;
}
int N = Prompt("Введите число ");

void NumRes (int N)
{
int i = 1;
while (i <= N)
{
    if (i == N)
        Console.Write ($"{Math.Pow((i),3)} ");
    else
        Console.Write ($"{Math.Pow((i),3)}, ");
    i++;
}
}
NumRes (N);





***************** Задача 24 **************
/* Напишите программу, которая
принимает на вход число (А) и выдаёт сумму
чисел от 1 до А
4 -> 10 (1+2+3+4=10)
7 -> 28
8 -> 36
*/

Console.Clear();
int num = GetNumberFromUser("Введите целое число A: ","Ошибка ввода!");
int sumNumbers = GetSumNumbers(num);
Console.WriteLine($"{num} -> {sumNumbers}");
// Выводит в консоль сообщение message,
// преобразовывает введённую пользователем строку в число типа int.
// В случае ошибки выводит в консоль сообщение errorMessage
int GetNumberFromUser(string message, string errorMessage)
{
while(true)
{
    Console.Write(message);
    bool isCorrect = int.TryParse(Console.ReadLine(), out int userNumber);
    if(isCorrect)
        return userNumber;
    Console.WriteLine(errorMessage);
}
}
// Возвращает сумму чисел от 1 до number
int GetSumNumbers(int number)
{
    int sum = 0;
    while(number > 0);
    {
        sum += number;
        number--;
    }
    return sum;
}




************** Задача 25 ************** 
/*Напишите цикл, который принимает на вход два числа (A и B) и возводит число A в натуральную степень B.
3, 5 -> 243 (3⁵)
2, 4 -> 16
*/
int a = GetNumberFromUser("Введите первое число: ", "Ошибка! Введите целое число.");
int b = GetNumberFromUser("Введите второе число: ", "Ошибка! Введите целое число.");
int result = GetStepen(a, b);

Console.Write($"{a}, {b} -> {result}");

int GetStepen(int A, int B)
{
    int result = A;
    for (int i = 0; i < B-1; i++)
    {
        result = result * A;
    }
    return result;
}

int GetNumberFromUser(string message, string errorMessage)
{
    while(true)
    {
        Console.Write(message);
        bool isCorrect = int.TryParse(Console.ReadLine(), out int userNumber);
        if(isCorrect)
            return userNumber;
        Console.WriteLine(errorMessage);
    }
}




****************** Задача 27 ***************
/*Задача 27: Напишите программу, которая принимает на вход число и выдаёт сумму цифр в числе.
452 -> 11
82 -> 10
9012 -> 12
*/

int number = GetNumberFromUser("Введите число: ", "Ошибка! Введите целое число."); 
GetSum(number);

int GetNumberFromUser(string message, string errorMessage)
{
    while(true)
    {
        Console.Write(message);
        bool isCorrect = int.TryParse(Console.ReadLine(), out int userNumber);
        if(isCorrect)
            return userNumber;
        Console.WriteLine(errorMessage);
    }
}

void GetSum (int num)
{
    if (num < 0)
        num = num * -1;
int sum = 0;
int cif = 0;

    while (num > 0)
    {
        cif = num % 10;
        num = num / 10;
        sum = sum + cif;
    }
Console.WriteLine($"{sum}");
}



 
******************* Задача 28 **************
/* Напишите программу, которая
принимает на вход число N и выдаёт
произведение чисел от 1 до N.
4 -> 24
5 -> 120
*/

Console.Clear();
int num = GetNumberFromUser("Введите целое число A: ","Ошибка ввода!");
int proiz = GetProiz(num);
Console.WriteLine($"{num} -> {proiz}");
int GetNumberFromUser(string message, string errorMessage)
{
while(true)
{
    Console.Write(message);
    bool isCorrect = int.TryParse(Console.ReadLine(), out int userNumber);
    if(isCorrect)
        return userNumber;
    Console.WriteLine(errorMessage);
}
}

int GetProiz(int n)
{
    int proiz = 1;
    int i = 1;
    while(i <= n);
    {
        proiz = proiz * i;
        i++;
    }
    return proiz;
}




*************** Задача 29 ***************
/* Напишите программу, которая задаёт массив из 8 элементов и выводит их на экран.
1, 2, 5, 7, 19 -> [1, 2, 5, 7, 19]
6, 1, 33 -> [6, 1, 33] */

int[] GetMassiv(int count)
{
    int[] arr = new int[count];
    for (int i = 0; i < arr.Length; i++)
    {
        arr[i] = GetNumberFromUser($"Введите {i} элемент массива: ", "Ошибка! Введите целое число."); 
    }
    return arr;
}

int GetNumberFromUser(string message, string errorMessage)
{
    while(true)
    {
        Console.Write(message);
        bool isCorrect = int.TryParse(Console.ReadLine(), out int userNumber);
        if(isCorrect)
            return userNumber;
        Console.WriteLine(errorMessage);
    }
}

void PrintArr(int[] array)
{
    Console.Write("[");
    for (int i = 0; i < array.Length; i++)
    {
        if(i < array.Length-1)
            Console.Write($"{array[i]}, ");
        else
            Console.Write($"{array[i]}");
    }
Console.Write("]");
}
PrintArr (GetMassiv(8));






************** Задача 30 ************
/*Напишите программу, которая выводит массив из 8 элементов, заполненный нулями и единицами в случайном порядке.
[1,0,1,1,0,1,0,0] */

int[] GenMassiv(int count)
{
    int[] arr = new int[count];
    for (int i = 0; i < arr.Length; i++)
    {
        arr[i] = new Random().Next(0, 10); 
    }
    return arr;
}

void PrintArr(int[] array)
{
    Console.Write("[");
    for (int i = 0; i < array.Length; i++)
    {
        if(i < array.Length-1)
            Console.Write($"{array[i]}, ");
        else
            Console.Write($"{array[i]}");
    }
Console.Write("]");
}
PrintArr (GenMassiv(10));



**************** Задача 31**************
/* Задача 31: Задайте массив из 12 элементов, заполненный случайными числами из промежутка [-9, 9]. Найдите сумму отрицательных
 и положительных элементов массива. Например, в массиве [3,9,-8,1,0,-7,2,-1,8,-3,-1,6] сумма положительных чисел равна 29, 
 сумма отрицательных равна -20. */

 Console.Clear();

int[] array = GetArray(12, -9, 9);
Console.WriteLine(String.Join(" ", array));

int positiveSum = GetPositiveSum(array);
int negativeSum = GetNegativeSum(array);

Console.WriteLine($"Positive sum = {positiveSum}, negative sum = {negativeSum} ");
//////////////////////////////////////////////////////////////////////////////////
// Возвращает массив из size элементов,
// заполненный случайными числами из промежутка [minValue, maxValue]
int[] GetArray(int size, int minValue, int maxValue)
{
int[] res = new int[size];
for (int i = 0; i < size; i++)
    {
        res[i] = new Random().Next(minValue, maxValue + 1);
    }
    return res;
}
// Возвращает сумму положительных чисел массива arr
int GetPositiveSum(int[] arr)
{
    int positiveSum = 0;
    foreach (int el in arr)
    {
        if (el > 0) positiveSum += el;
    }
    return positiveSum;
}
// Возвращает сумму отрицательных чисел массива arr
int GetNegativeSum(int[] arr)
{
    int negativeSum = 0;
    foreach (int el in arr)
    {
        negativeSum += el < 0 ? el : 0;
    }
    return negativeSum;
}




******************* Задача 32 **************
/*Задача 32: Напишите программу замены элементов массива: положительные элементы замените на
соответствующие отрицательные, и наоборот. [-4, -8, 8, 2] -> [4, 8, -8, -2] */

Console.Clear();

int[] array = GetArray(4, -10, 10);
Console.WriteLine(String.Join(" ", array));
Replace(array);
Console.WriteLine(string.Join(" ", array));


int[] GetArray(int size, int minValue, int maxValue)
{
    int[] res = new int[size];
    for (int i = 0; i < size; i++)
    {
        res[i] = new Random().Next(minValue, maxValue + 1);
    }
    return res;
}

void Replace(int[] arr)
{
    for (int i = 0; i < arr.Length; i++)
    {
        arr[i] *= -1;
    }
}



************* Задача 33 ***************************
/* Задача 33: Задайте массив. Напишите программу, которая определяет, присутствует ли заданное число в массиве.
4; массив [6, 7, 19, 345, 3] -> нет
3; массив [6, 7, 19, 345, 3] -> да */

Console.Clear();

int[] array = GetArray(5, 1, 500);
Console.WriteLine(String.Join(" ", array));

Console.Write ("Введите целое число: ");
int UserNamber = int.Parse(Console.ReadLine() ?? "");

bool FindRes = FindUserNumInArray(array, UserNamber);

if (FindRes) Console.WriteLine("да");
else Console.WriteLine("нет");

//генерация массива
int[] GetArray(int size, int min, int max)
{
    int[] res = new int[size];
    for (int i = 0; i < size; i++)
    {
        res[i] = new Random().Next(min, max + 1);
    }
    return res;
}


// логика
bool FindUserNumInArray(int[] array, int UserNamber)
{
    foreach (int el in array)
    {
        if (el == UserNamber)
        return true;
    }
    return false;
}



******************* Задача 35 ******************

/* Задача 35: Задайте одномерный массив из 123 случайных чисел.
Найдите количество элементов массива, значения которых лежат в
отрезке [10,99].
Пример для массива из 5, а не 123 элементов. В своём решении сделайте для 123
[5, 18, 123, 6, 2] -> 1
[1, 2, 3, 6, 2] -> 0
[10, 11, 12, 13, 14] -> 5 */

Console.Clear();

int[] array = GetArray(12, 1, 100);
Console.WriteLine(String.Join(" ", array));

int count = GetCount(array);
Console.WriteLine($"количество элементов массива: {count}");

int GetCount(int[] arr)
{
    int count = 0;
    foreach (int el in array)
    {
        if (el > 10 && el < 100) count++;
    }
    return count;
}

int[] GetArray(int size, int minValue, int maxValue)
{
    int[] res = new int[size];
    for (int i = 0; i < size; i++)
    {
        res[i] = new Random().Next(minValue, maxValue + 1);
    }
    return res;
}



************ Задача 37 ****************

/* Задача 37: Найдите произведение пар чисел в одномерном массиве. Парой считаем первый и последний элемент, второй и предпоследний
и т.д. Результат запишите в новом массиве.
[1 2 3 4 5] -> 5 8 3
[6 7 3 6] -> 36 21 */

Console.Clear();

int[] array = GetArray(5, 1, 15);
Console.WriteLine(String.Join(" ", array));

int[] arrNew = GetSumPar(array);
Console.WriteLine(String.Join(" ", arrNew));

int[] GetArray(int size, int min, int max)
{
    int[] res = new int[size];
    for (int i = 0; i < size; i++)
    {
        res[i] = new Random().Next(min, max + 1);
    }
    return res;
}

int[] GetSumPar(int[] array)
{
    int s = array.Length / 2;
    int j = array.Length - 1;
    int[] arrNew = new int [s];
    for (int i = 0; i < s; i++)
    {
        arrNew[i] = array[i] * array[j];
        j--;
    }
    return arrNew;
}

