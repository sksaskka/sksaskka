using System;
using System.Threading;

class Program
{
    static int sum1 = 0;
    static int sum2 = 0;
    static int sum3 = 0;

    static void Main()
    {
        Thread potok1 = new Thread(() => { for (int i = 1; i <= 100; i++) sum1 += i; });
        Thread potok2 = new Thread(() => { for (int i = 101; i <= 200; i++) sum2 += i; });
        Thread potok3 = new Thread(() => { for (int i = 201; i <= 300; i++) sum3 += i; });

        potok1.Start();
        potok2.Start();
        potok3.Start();

        potok1.Join();
        potok2.Join();
        potok3.Join();

        int result = sum1 + sum2 + sum3;

        Console.WriteLine($"Первый поток: {sum1}");
        Console.WriteLine($"Второй поток: {sum2}");
        Console.WriteLine($"Третий поток: {sum3}");
        Console.WriteLine($"Общая сумма: {result}");
