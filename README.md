# Semana-9
using System ;
using System.ComponentModel;
{
    namespace TiendaVirtual
    {
    class Program
    {
        static void Main(String[] args)
        {
            string nombre;
            double saldo;
            int opcion;
            //datos entrada
            Console.WriteLine("*** Creando mi Cuenta *** ");
            Console.WriteLine("\n1 Ingreso nombre del titular " );
            nombre = Console.ReadLine();
            Console.WriteLine(¨Ingrese el saldo inicial:¨);
            saldo = double.Parse(Console.ReadLine());
            //crear un objetivo de la clase Cuenta
            Cuenta cue = new Cuenta(nombre, saldo);
            Console.WriteLine( ¨Cuenta creada. . . . ¨ );
            cue.MostrarDatos();
            //menu de oeraciones 
            do {
                Console.WriteLine(¨***Operaciones Disponibles * ** ¨);
                Console.WriteLine("\n1. Despositar saldo " + 
                Console.WriteLine("\n2.  Retirar saldo" +
                Console.WhiteLine("\n3. Ver datos de la cuenta" + 
                Console.WriteLine("\n4. Salir");
                Console.WriteLine  ("Seleccione la opcion: ");
                opcion = int.Parse(Console.ReadLine());
                switch (opcion) {
                    case 1:
                        Console.WriteLine(¨Ingrese la cantidad a despositar:  ¨);
                        double cantDep = double.Parse(ConsoleConsole.readLine());
                        cue.Depositar(cantDep);
                        break;
                    case 2:
                        ConConsole.WriteLine(¨Ingrese la cantidad a retirar:  ¨);
                        double retiro = double.Parse(ConsoleConsole.readLine());
                        cue.retirar(retiro);
                        break;
                    case 3:
                        cue.MostrarDatos();
                        break;
                    case 4:
                        Console.WriteLine(¨Saliendo del programa¨);
                        break;
                }
                while (opcion != 4) ; }

        }



using System ;
using System.ComponentModel;
using System.Diagnostics.Eventing.Reader;
{
    namespace TiendaVirtual
    {
    class Program
    {
        static double stock;
        public static void AgregarStock(int cant) {
            if (canti > 0)
            {
                stock += canti;
                Console.WriteLine(Se agrego la cantidad de: ¨ +canti);
            }
            else
                Console.WriteLine(¨Ingrese una cantidad válida¨);

        }
        public static void ReducirStock(int cant)
        {
            if (cant > 0 && cant <= stock)
            {
                stock -= cant;
                Console.WriteLine(¨Stock reducido:¨+cant +
                                  ¨\nStock actual: ¨+stock
            }
            else
                Console.WriteLine(¨Error, cantiad inválida);
        }
        {
           public static void InicializarStock() {
            Console.WriteLine(¨Ingrese nombre del producto: ¨)}
            nombre = Console.ReadLine();
            Console.WriteLine(Ïngrese nombre del producto: ¨);
            precio = double.Parse(Console.ReadLine());
            Console.WriteLine(Ïngrese precio: ¨); 
            stock = double.Parse(Console.ReadLine());
        }
    public static vooid mostarrDatos()
        {
             Console.WriteLine(¨\nNombre    : ¨+ nombre+
                               ¨\nPrecio)   : ¨+precio+
                               ¨\nCantidad  : ¨+stock);

        }  
        while (opcion != 0) ; }

        +



otro dia miercoles 

using System;


namespace ConsoleAppFunciones
{
    class Program
    {

        static void Main(string[] args)
        {
            /*
            //ejemplo 01
            //**********            
            Program program = new Program();

            program.MostrarSaludo("Carlos");

            int resultado = program.Sumar(3, 5);
            Console.WriteLine("Resultado: " + resultado);

            Console.ReadKey();

            //ejemplo 02
            //**********
            Program a1 = new Program();
            a1.Incrementar();

            Program a2 = new Program();
            a2.Incrementar();

            Console.ReadKey();

             
            //ejemplo 03
            //**********
            // Por valor: se pasa una copia, no se modifica el valor original

            Program prog = new Program();

            int x = 5;
            prog.DuplicarPorValor(x);
            Console.WriteLine("Después de por valor: " + x); // x sigue siendo 5

            Console.ReadKey();


            //ejemplo 04
            //**********
            // Por referencia: se modifica el valor original

            int y = 5;
            prog.DuplicarPorReferencia(ref y);
            Console.WriteLine("Después de por referencia: " + y); // y ahora es 10

            Console.ReadKey();

            //ejemplo 05
            //**********
            int valor = 5;
            Console.WriteLine("Antes: " + valor);  // Salida: 5

            IncrementarRef(ref valor);

            Console.WriteLine("Después: " + valor); // Salida: 15

            Console.ReadKey();
            */

            Program a1 = new Program();

            int valorRef = 5;
            a1.IncrementarPorRef(ref valorRef);
            Console.WriteLine(valorRef); // Salida: 6

            int numero;
            a1.ObtenerResultado(out numero);
            Console.WriteLine(numero); // Salida: 100

            int valor = 4;
            a1.MostrarCuadrado(in valor); // Salida: 16

            Console.ReadKey();

            //MainEjercicio01();
            //MainEjercicio02();
            //MainEjercicio03();
            MainEjercicio04();
        }

        //ref – Pasar y modificar una variable ya inicializada
        static void IncrementarRef(ref int numero)
        {
            numero += 10;
        }

        void IncrementarPorRef(ref int numero)
        {
            numero += 1;
        }

        void ObtenerResultado(out int resultado)
        {
            resultado = 100;
        }

        void MostrarCuadrado(in int numero)
        {
            int cuadrado = numero * numero;
            Console.WriteLine(cuadrado);
        }


        void MostrarSaludo(string nombre)
        {
            Console.WriteLine($"Hola, {nombre}!");
        }

        int Sumar(int a, int b)
        {
            return a + b;
        }

        // Uso de variable global
        int contador = 0;

        // Uso de variable estática
        static int totalLlamadas = 0;
        void Incrementar()
        {
            // Variable local
            int incremento = 1;

            contador += incremento;

            totalLlamadas += incremento;

            Console.WriteLine($"Contador: {contador}, Total llamadas: {totalLlamadas}");
        }

        #region MyRegion

        //Variable global de instancia
        //(int contador = 0)

        //Se reinicia para cada instancia (cada objeto nuevo).
        //Cada objeto tiene su propia copia de la variable.

        //---------

        //Variable estática
        //(static int contador = 0)

        //Pertenece a la clase, no al objeto.
        //Comparte el mismo valor entre todas las instancias.
        //Mantiene su valor aunque se creen o destruyan objetos.


        #endregion


        // Por valor: se pasa una copia, no se modifica el valor original
        void DuplicarPorValor(int numero)
        {
            numero *= 2;
            Console.WriteLine("Dentro de la función (valor): " + numero);
        }

        // Por referencia: se modifica el valor original
        void DuplicarPorReferencia(ref int numero)
        {
            numero *= 2;
            Console.WriteLine("Dentro de la función (referencia): " + numero);
        }





