# tasks
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Task1
{
    class Program
    {
        static void Main(string[] args)
        {
            Random rand = new Random();
            int[] n = new int[20];
            int max = int.MinValue;
            int min = int.MaxValue;
            int sum = 0;
            int max_pos = -1;
            int min_pos = -1;
            int multi = 1;
            for (int i = 0; i < n.Length; i++)
            {
                n[i] = rand.Next(-100, 101);
                Console.Write($"{n[i]} ");
                if (n[i] > max)
                {
                    max = n[i];
                }
                if (n[i] < min)
                {
                    min = n[i];
                }
                if (n[i] > max_pos)
                {
                    max = n[i];
                    max_pos = i;
                }
                if (n[i] < min_pos)
                {
                    min = n[i];
                    min_pos = i;
                }
                multi *= n[i];
                sum += n[i];
            }
            int average = sum / 20;
            Console.WriteLine($"Минимум: {min}, максимум: {max}, сумма: {sum}, произведение: {multi}, среднее арифметическое: {average}, позиция минимума: {min_pos}, позиция максимума: {max_pos}");
        }


    }
}
