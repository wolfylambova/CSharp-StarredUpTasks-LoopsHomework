using System;
using System.Numerics;
class Zeros
{
    static void Main()
    {
        int number = int.Parse(Console.ReadLine());

        BigInteger factorial = 1;
        int count = 0;

        for (int i = 1; i <= number; i++)
        {
            factorial = i * factorial;
        }
        Console.WriteLine(factorial);

        string factorialStr = factorial.ToString();
        int lenghtNum = factorialStr.Length;
        BigInteger[] factArray = new BigInteger[lenghtNum];
        for (int i = lenghtNum - 1; i >= 0; i--)
        {
            BigInteger digit = factorial % 10;
            factArray[i] = (BigInteger)digit;
            factorial = factorial / 10;
        }
            
        Array.Reverse(factArray);


        for (int i = 0; i <= factArray.Length; i++)
        {
            while ((factArray[i] == 0))
            {
                count += 1;
            }
        }
        Console.WriteLine("trailing zeros ={0}",count);
    }
}

