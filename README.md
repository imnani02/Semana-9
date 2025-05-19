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

        
