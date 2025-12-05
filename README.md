using System;

namespace FigurasGeometricas
{
    class Program
    {
        static void Main(string[] args)
        {
            // Habilita UTF-8 para que salgan bien tildes y ñ
            Console.OutputEncoding = System.Text.Encoding.UTF8;

            // Crear un círculo con radio 5
            Circulo circulo = new Circulo(5);

            Console.WriteLine($"Área del círculo: {circulo.CalcularArea():0.00}");
            Console.WriteLine($"Perímetro del círculo: {circulo.CalcularPerimetro():0.00}");

            // Crear un rectángulo de base 4 y altura 7
            Rectangulo rect = new Rectangulo(4, 7);

            Console.WriteLine($"Área del rectángulo: {rect.CalcularArea():0.00}");
            Console.WriteLine($"Perímetro del rectángulo: {rect.CalcularPerimetro():0.00}");
        }
    }

    // Clase para círculos
    class Circulo
    {
        private double radio;

        public Circulo(double r)
        {
            radio = r;
        }

        public double CalcularArea()
        {
            return Math.PI * radio * radio;
        }

        public double CalcularPerimetro()
        {
            return 2 * Math.PI * radio;
        }
    }

    // Clase para rectángulos
    class Rectangulo
    {
        private double baseRect;
        private double altura;

        public Rectangulo(double b, double h)
        {
            baseRect = b;
            altura = h;
        }

        public double CalcularArea()
        {
            return baseRect * altura;
        }

        public double CalcularPerimetro()
        {
            return 2 * (baseRect + altura);
        }
    }
}
