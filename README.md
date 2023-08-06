# seminar-ex
Решение задач на семинаре

Задача 0
/* программа, которая на вход принимает число и выдает его квадрат (число умноженное на само себя)
4 - 16
-3 - 9 
*/

Console.Write("Введите целое число: ");
int number = int.Parse(Console.ReadLine() ?? "");

int result = number * number;

Console.WriteLine($"{number} -> {result}");






Задача 1
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





Задача 2
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





Задача 3

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





Задача 4
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



Задача 11
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




Задача 12
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




Задача 14
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




    Задача 16
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



    Задача 18
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





Задача 24
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




Задача 25 
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

