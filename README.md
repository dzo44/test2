# test2

using System;
using static System.Console;

namespace Funkcija
{
    class Program
    {
        static void TablicaMnozenja(byte broj)
        {
            WriteLine($"Ovo je {broj} tablice mnozenja: ");

            for (int red = 1; red <= 12; red++)
            {
                WriteLine($"{red} * {broj} = {red * broj}");
            }
            WriteLine();
        }

        static void PokreniTablicuMnozenja()
        {
            bool daLiJeBroj;

            do
            {
             Write("Unesite broj izmedju 0 i 255: ");

             daLiJeBroj = byte.TryParse(ReadLine(), out byte broj);

             if (daLiJeBroj)
             {
                 TablicaMnozenja(broj);
             }
             else
             {
                 WriteLine("Niste uneli validan broj!");
             }   
            } while (daLiJeBroj);
        }
        static void Main(string[] args)
        {
            PokreniTablicuMnozenja();
        }
    }
}
