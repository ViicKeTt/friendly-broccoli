using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            string opcion = "";
            bool continuar = true;
            while (continuar) 
            {
                Console.Clear();

                Console.WriteLine("[1] Saludo de estudiante");
                Console.WriteLine("[2] numeros 1-50");
                Console.WriteLine("[3] Loteria");
                Console.WriteLine("[4] Datos del vehiculo");
                Console.WriteLine("[4] salir");
                Console.WriteLine();
                Console.Write("Digite el numero: ");
                opcion =Console.ReadLine();
                Console.WriteLine();

                    switch (opcion)
                    {
                        case "1":
                            HolaEstudiante();
                            break;
                        case "2":
                            numeros();
                            break;
                        case "3":
                            aleatorio();
                            break;
                        case "4":
                        vehiculo carro = new vehiculo();

                        Console.WriteLine(carro.Marca);
                        Console.WriteLine(carro.Modelo);
                        Console.WriteLine(carro.Año);
                        Console.WriteLine(carro.Color);
                        Console.WriteLine(carro.estado);

                        break;
                        case "5":
                            continuar = false;
                            break;
                    default:
                            Console.WriteLine("Error...");
                            break;
                    }
                    Console.ReadKey();
            }
        }
        static void HolaEstudiante()
        {
            string name= "Esmerlin borges Corporan";

            Console.WriteLine("Hola, estudiante" + name + ". Bienvenido a programación I");

            Console.ReadKey();
        }
        static void numeros()
        {
            for (int i = 0; i <= 50; i++) 
            {
                Console.WriteLine(i);
            }
        }
        static void aleatorio()
        {
            int cant=6;
            Random rnd = new Random();
            int num = rnd.Next();
            int mumero = rnd.Next(0, 100);
            
            int[] bgt = new int[cant];

            for (int i = 0; i < bgt.Length; i++)
            {
                Console.WriteLine("usted tiene 6 intentos para acertar el numero de la loto, si se lo saca automaticamente" +
                    "el programa le dice si gano.");
                Console.WriteLine();
                Console.Write("Introducir un numero" + "(" + i + "): ");
                bgt[i] = int.Parse(Console.ReadLine());

                if ( i == mumero)
                {
                    Console.WriteLine();
                    Console.WriteLine("-------------------------------------------------------------");
                    Console.WriteLine("----------FELICIDADES AMIGO USTED SE GANOOO LA LOTO----------");
                    Console.WriteLine("-------------------------------------------------------------");
                }
            }
            Console.WriteLine();
            Console.WriteLine("El numero de la loteria es: "+ mumero+"");
        }
    }
    class  vehiculo
    {
        public string Marca ="sonata";
        public string Modelo= "Y12";
        public string Año = "2005";
        public string Color = "negro";
        public bool estado = false;

        public void cambiar()
        {

        }

      
    }
    
}
