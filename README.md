# void-scape
using System;

namespace matrices
{

    public class IntMatriz {

        int[] matriz;
        
        public void inputTamaño()
        {
           
        }


        public IntMatriz(int i)
        {
            matriz = new int[i];
        }

        static void Main()
        {

            Console.WriteLine("Bienvenidos a el simulador de matrices bidimensional: Ingrese el tamaño de su matriz: ");

            int tmMatriz = Convert.ToInt32(Console.ReadLine());

            IntMatriz matriz1 = new IntMatriz(tmMatriz);


            Console.WriteLine("Su matriz bidimensional es de " + matriz1.matriz.Length + " filas.");


            for (int i = 0; i < matriz1.matriz.Length; i++)
            {
                Console.WriteLine($"Ingrese su {i +1} elemento: ");

                int elementoinput = Convert.ToInt32(Console.ReadLine());

                matriz1.matriz[i] = elementoinput;

            }

            bool exit = false;
            while (!exit)
            {
                Console.WriteLine("Elija una de las siguientes opciones: \n1- Intercambiar columnas \n2- Ver elementos de la matriz \n3- Salir del programa");

                string selec = Console.ReadLine();

                switch (selec)
                { 
                    case "1":


                        break;

                    case "2":

                        Console.WriteLine("Los elementos de la matriz son:");
                        for (int i = 0; i < matriz1.matriz.Length; i++)
                        {
                            Console.WriteLine(matriz1.matriz[i]);
                        }
                        break;

                    case "3":

                        exit = true;

                        break;

                    default:

                        Console.WriteLine("Opcion invalida");

                        break;


                }

            }
            




            // BUCLE PARA IMPRIMIR ELEMENTOS DE LA MATRIZ
           /* for (int i = 0; i < matriz1.matriz.Length; i++)
            {
                Console.WriteLine(matriz1.matriz[i]);
            }*/
        }

    }
}


