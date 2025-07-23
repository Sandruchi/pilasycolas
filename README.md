using System;
using System.Collections.Generic;

namespace ParqueDiversiones
{
    class Persona
    {
        public string Nombre { get; set; }
        public int ID { get; set; }

        public Persona(string nombre, int id)
        {
            Nombre = nombre;
            ID = id;
        }
    }

    class Atraccion
    {
        private Queue<Persona> colaEspera = new Queue<Persona>();
        private List<Persona> asientosAsignados = new List<Persona>();
        private const int maxAsientos = 30;

        public void IngresarPersona(Persona p)
        {
            if (colaEspera.Count + asientosAsignados.Count < maxAsientos)
            {
                colaEspera.Enqueue(p);
                Console.WriteLine($"Ingreso exitoso: {p.Nombre} está en espera.");
            }
            else
            {
                Console.WriteLine("Lo sentimos, todos los asientos están ocupados.");
            }
        }

        public void AsignarAsientos()
        {
            while (colaEspera.Count > 0 && asientosAsignados.Count < maxAsientos)
            {
                Persona p = colaEspera.Dequeue();
                asientosAsignados.Add(p);
                Console.WriteLine($"Asiento asignado a: {p.Nombre} (ID: {p.ID})");
            }
        }

        public void MostrarEstado()
        {
            Console.WriteLine("\nPersonas en cola:");
            foreach (var persona in colaEspera)
                Console.WriteLine($"- {persona.Nombre} (ID: {persona.ID})");

            Console.WriteLine("\nPersonas con asiento:");
            foreach (var persona in asientosAsignados)
                Console.WriteLine($"✓ {persona.Nombre} (ID: {persona.ID})");
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            Atraccion atraccion = new Atraccion();

            for (int i = 1; i <= 35; i++)
            {
                Persona persona = new Persona($"Visitante{i}", i);
                atraccion.IngresarPersona(persona);
            }

            atraccion.AsignarAsientos();
            atraccion.MostrarEstado();
        }
    }
}


/PilasColasSandraCSharp/
├── Persona.cs
├── Atraccion.cs
├── Program.cs
├── README.md
├── /evidencias/
│   ├── captura1.png
│   ├── captura2.png

Atraccion.cs
using System;
using System.Collections.Generic;

namespace ParqueDiversiones
{
    public class Atraccion
    {
        private Queue<Persona> colaEspera = new Queue<Persona>();
        private List<Persona> asientosAsignados = new List<Persona>();
        private const int maxAsientos = 30;

        public void IngresarPersona(Persona p)
        {
            if (colaEspera.Count + asientosAsignados.Count < maxAsientos)
            {
                colaEspera.Enqueue(p);
                Console.WriteLine($"Ingreso exitoso: {p.Nombre} está en espera.");
            }
            else
            {
                Console.WriteLine("Lo sentimos, todos los asientos están ocupados.");
            }
        }

        public void AsignarAsientos()
        {
            while (colaEspera.Count > 0 && asientosAsignados.Count < maxAsientos)
            {
                Persona p = colaEspera.Dequeue();
                asientosAsignados.Add(p);
                Console.WriteLine($"Asiento asignado a: {p.Nombre} (ID: {p.ID})");
            }
        }

        public void MostrarEstado()
        {
            Console.WriteLine("\nPersonas en cola:");
            foreach (var persona in colaEspera)
                Console.WriteLine($"- {persona.Nombre} (ID: {persona.ID})");

            Console.WriteLine("\nPersonas con asiento:");
            foreach (var persona in asientosAsignados)
                Console.WriteLine($"✓ {persona.Nombre} (ID: {persona.ID})");
        }
    }
}

Program.cs
using System;

namespace ParqueDiversiones
{
    class Program
    {
        static void Main(string[] args)
        {
            Atraccion atraccion = new Atraccion();

            for (int i = 1; i <= 35; i++)
            {
                Persona persona = new Persona($"Visitante{i}", i);
                atraccion.IngresarPersona(persona);
            }

            atraccion.AsignarAsientos();
            atraccion.MostrarEstado();

            Console.WriteLine("\nSimulación completada.");
        }
    }
}
