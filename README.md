/*Priklad 5.1 (1)*/
/*
using System;
class Program
{
    public static bool JeSestupne(int[] pole)
    {
        for (int i = 0; i < pole.Length - 1; i++)
            if (pole[i] < pole[i + 1])
                return false;
        return true;
    }

    static void Main()
    {
        int[] pole = { 15, 12, 9, 9, 8, 5, 2, 2, 1 };
        bool je = JeSestupne(pole);
        Console.WriteLine(je); // true
    }
}
*/



/*Priklad 5.2 (1, 1/2, 1/2)*/
/*
using System;
class Program
{
    static int prirazeni = 0;
    static int porovnani = 0;

    public static void Prirazeni(ref int a, int b)
    {
        a = b;
        prirazeni++;
    }

    public static bool JeMensi(int a, int b)
    {
        porovnani++;
        return a < b;
    }

    public static bool JeVetsi(int a, int b)
    {
        porovnani++;
        return a > b;
    }

    static void Main()
    {
        int x = 5, y = 4, z = 3;
        
        bool je1 = JeMensi(y, z);
        bool je2 = JeMensi(x, z);
        bool je3 = JeVetsi(x, y);

        Prirazeni(ref x, y);
        Prirazeni(ref y, z);

        Console.WriteLine("Prirazeni: {0}, Porovnani: {1}", prirazeni, porovnani);
    }
}
*/



/*Priklad 5.5 (2, +1)*/
/*
using System;
class Program
{
    public static int BinarniVyhledavani(int[] arr, int hledanaHodnota, bool prvniVyskyt = false)
    {
        int left = 0;
        int right = arr.Length - 1;
        int result = -1;

        while (left <= right)
        {
            int mid = left + (right - left) / 2;

            if (arr[mid] == hledanaHodnota)
            {
                result = mid;
                
                if (prvniVyskyt)
                    right = mid - 1;
                else
                    return result;
            }
            else if (arr[mid] < hledanaHodnota)
                right = mid - 1;
            else
                left = mid + 1;
        }

        return result;
    }

    static void Main()
    {
        int[] p1 = { 12, 9, 6, 6, 6, 5, 3, 1, 1 };

        int indexA = BinarniVyhledavani(p1, 6);
        Console.WriteLine("(a) index = " + indexA);

        int indexB = BinarniVyhledavani(p1, 6, true);
        Console.WriteLine("(b) index = " + indexB);
    }
}
*/
