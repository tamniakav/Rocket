using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Rocket
{
    class Rocket
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int side = (3 * n) / 2 - 1;
            int middle = 0;
            

            for (int i = 0; i < n; i++)
            {
                Console.WriteLine("{0}/{1}\\{0}", new string('.', side), new string(' ', middle));
                side--;
                middle += 2;
            }
            side++;
            Console.WriteLine("{0}{1}{0}", new string('.', side), new string('*', (3 * n) - (2 * side)));
            middle -= 2;
            for (int i = 0; i < n * 2; i++)
            {
                Console.WriteLine("{0}|{1}|{0}", new string('.', side), new string('\\', middle));
            }
            for (int i = 0; i < n / 2; i++)
            {
                Console.WriteLine("{0}/{1}\\{0}", new string('.', side), new string('*', middle));
                side--;
                middle += 2;
            }
        }
    }
}
