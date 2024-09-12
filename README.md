Projeto 1



using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Media_de_notas
{
    internal class Program
    {
        static void Main(string[] args)
        {
            //declaração das variaveis
            int nota1 = 7;
            int nota2 = 8;
            int nota3 = 9;
            // calculando media
            int media = (nota1 + nota2 + nota3) / 3;
            // $ serve para mostrar variaveis no meio do console
            Console.WriteLine($"A média é de {media}");
            // estrtura condicional para avaliar aluno
            if (media < 6)
            {
                Console.WriteLine("Aluno Reprovado");
            }
            else
            {
                Console.WriteLine("Aluno Aprovado");
            }

        }
    }
}     




Projeto 2 



using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Primeiro_Projeto
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int a;
            int b;
            int[] vetor = new int[6];
            string minhaFrase = "Olá Mundo";
            // Inicialização de variaveis
            a = 7;
            b = a - 6;
            // Processamento
            Console.WriteLine("Valores vetor[b]:");
            while (b < a) {
                vetor[b] = b + a;
                Console.WriteLine(vetor[b]);
                b = b + 2;
            }
            Console.WriteLine("Valor a =");
            Console.WriteLine(a);

            Console.WriteLine("Valor b=");
            Console.WriteLine(b);

            Console.WriteLine(minhaFrase);
        }
    }
}



projeto 3 



using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            decimal salarioFixo = 3000;
            decimal totalVendas = 1500;

            decimal comissao = 0;
            if (totalVendas > 2000)
            {
                comissao = (totalVendas - 2000) * 0.1m;
                comissao += (2000 * 0.05m);
            }
            else
            {
                comissao = totalVendas * 0.05m;
            }
            Console.WriteLine($"O salario total é: {comissao + salarioFixo}");

        }
    }
}

Projeto 4


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Constante
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /*
             Const é um comando para tarvar um tipo de uma variavel 
             fazendo com que ela não possa receber outro valor nessa varaivel 
             por exemplo o valor de pi que sempre vai valer 3.14
            */
            const float PI = 3.145655678f;
            Console.WriteLine(PI);
            Console.ReadLine();
        }
    }
}

Projeto 5

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Estrtura_Condicional
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // (E ou AND) é representado por && - (OU ou OR) é representado por ||
            int a = 20;
            int b = 40;
            int c = 60;
            if (a < b || a >c)// ||
            {
                Console.WriteLine("Verdade");
            }
            else if(a< b){
                Console.WriteLine("Estou usando else if");
            }
            else
            {
                Console.WriteLine("É mentira");

            }
            Console.ReadLine();
        }
    }
}


Projeto 6

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Recebendo_dado_do_usuario
{
    internal class Program
    {
        static void Main(string[] args)
        {

            /*Parse ele é um codigo para converter oque o usuario digita para um determiando tipo de variavel 
              pois no c# todo numero recebido pelo usuario é tratado como string 
              assim com o .Parse voce converte ele no tipo desejado
              */
            Console.WriteLine("Digite sua idade: ");
            int idade = int.Parse(Console.ReadLine());
            if(idade >= 0 && idade <= 11)
            {
                Console.WriteLine("Você é uma criança");
            } 
            else if(idade >= 12  && idade <= 18)
            {
                Console.WriteLine("Você é um adolescente");

            }else if(idade >= 19 & idade <= 60)
            {
                Console.WriteLine("Você é um adulto");

            }
            else
            {
                Console.WriteLine("Você é um idoso");
            }
        }
    }
}


Projeto 7

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Funçôes
{
    internal class Program
    {
        static void Main(string[] args)
        {
            //Para chamar a função basta colocar o nome da função e parenteses depois
            GerarPreco(60, "faca");
            // para chamar uma funcao com parametros é obrigatorio que tenha um retorno dentro da função
            GerarPreco(20,"garfo");
            GerarPreco(200, "prato");
            PrecoTotal(20);
            PrecoTotal(-20);

            Console.ReadLine();
        }
        // para criar uma função em C# deve usar o comando static e definir o tipo da funçao como esta abaixo o void
        static void ExibirMsg()
        {
            Console.WriteLine("Esse sistema é legal");
            Console.WriteLine("Estou usando funções");
            Console.WriteLine("Bem Vindo");
        }
        // o int preco é um parametro e ele só vai funcionar dentro da funçao
        static void GerarPreco(int preco, string nome)
        {
            Console.WriteLine("Nome do produto: " + nome);
            Console.WriteLine(preco);
        }
        static void PrecoTotal(int preco)
        {
            /* Math.Abs faz com que tire o modulo do seu  numero
             nesse caso preco pois o preco nunca pode ser um numero negativo
             assim faz com que ele seja sempre positivo
            */
            int precoAbs = Math.Abs(preco);
            int valorFinal = precoAbs + (2 * precoAbs);
            //  + valorFinal isso é uma concatenação
            Console.WriteLine("Valor final:" + valorFinal);
        }
    }
}




