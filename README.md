# HW5

namespace HW5_1
{
    class Program
    {
        static void Main(string[] args)
        {
            string filename = "text.txt";
            File.WriteAllText(filename, "write into a file a string");
        }
    }
}

//Ввести с клавиатуры произвольный набор данных и сохранить его в текстовый файл.

namespace HW5_2
{
    class Program
    {
        static void Main(string[] args)
        {
            {
                string filename = "startup.txt";
                DateTime localDate = DateTime.Now;
                string nowTime = localDate.ToString();

                File.WriteAllText(filename, nowTime);
                Console.ReadLine();
            }
        }
    }
}

/*Написать программу, которая при старте дописывает текущее время в файл                   
«startup.txt»*/

namespace HW5_3
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Введите набор чисел (0...255)");
            string setOfNumbers = Console.ReadLine();
            byte[] arrayNumbers = new byte[setOfNumbers.Length];
            for (int i = 0; i < arrayNumbers.Length; i++)
            {
                arrayNumbers[i] = Convert.ToByte(setOfNumbers[i]);
            }
            
            
             File.WriteAllBytes("bytes.bin",arrayNumbers);
            

            Console.ReadLine();
        }
    }
}

//Ввести с клавиатуры произвольный набор чисел (0...255) и записать их в бинарный файл
