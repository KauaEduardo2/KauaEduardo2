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


Projeto 8 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace SWITCH
{
    internal class Program
    {
        static void Main(string[] args)
        {
            string cor = "Verde";
            // switch usado para dar varias condicoes a uma unica variavel
            // exemplo abaixo
            switch (cor)
            {
                case "Vermelho":
                    Console.WriteLine("Sua cor favorita é Vermelho");
                    break;
                case "Amarelo":
                    Console.WriteLine("Sua cor favorita é Amarelo");
                    break;
                case "Azul":
                    Console.WriteLine("Sua cor favorita é Azul");
                    break;
                default:
                    Console.WriteLine("Verde");
                    break;

            }
            Console.ReadLine(); 
        }
    }
}

Projeto 9 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Enum
{
    internal class Program
    {
        /* Enum serve para que voce consiga Definir valores fixos a uma variavel 
         * nesse exemplo Cor ai voce define os valores para cor ai 
         * depois pode chamar cor no seu main
         * */
        enum Cor {Azul, Vermelho, Verde, Amarelo }
        static void Main(string[] args)
        {
            Cor corfavorita = Cor.Azul;
            Cor corFavoritaDoKaua = Cor.Amarelo;

            Console.WriteLine((Cor)2);
            Console.WriteLine(corfavorita);
            Console.WriteLine(corFavoritaDoKaua);
            Console.ReadLine(); 
        }
    }
}



Projeto 10


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Vetor
{
    internal class Program
    {
        static void Main(string[] args)
        {
            /*
             Para criar um vetor em C
             precisa definir o tipo dele igual de uma variavel 
             depois o nome dele em seguida usar o comando NEW e a 
             seguir o tamanho que o vetor tera
             */
            string[] produtos = new string[5]
             {
                "Maça",//[0]
                "Pera",//[1]
                "Couve",//[2]
                "Batata",//[3]
                "Leite",//[4]

             };
            // para alterar o valor de algum indice do vetor é igual de uma variavel
            produtos[0] = "Maça verde";
            Console.WriteLine(produtos[0]);
            // outra forma de criar um vetor é definir o tipo dele e o nome depois passar seus valores
            int[] valores = { 40, 24, 15, 99 };
            Console.WriteLine(valores[0]);
            Console.WriteLine(valores[1]);

            Console.ReadLine();
        }
    }
}


Projeto 11


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Enum_com_swicht
{
    internal class Program
    {
        enum Opcao{ Criar = 1, Deletar, Editar, Listar, Atualizar}
        static void Main(string[] args)
        {
            Console.WriteLine("Escolha uma das opções abaixo: ");
            Console.WriteLine(" 1 - Criar\n 2 - Deletar \n 3 - Editar\n 4 - Listar\n 5 - Atualizar");
            int index = int.Parse(Console.ReadLine());
            Opcao opcaoSelecionada = (Opcao)index;
            switch(opcaoSelecionada)
            {
                case Opcao.Criar:
                    Console.WriteLine("Criar é foda");
                    break;
                case Opcao.Deletar:
                    Console.WriteLine("Delete Imediatamente");
                    break;
                case Opcao.Editar:
                    Console.WriteLine("Edite manualmente");
                    break;
                case Opcao.Listar:
                    Console.WriteLine("Seu Programa foi listado");
                    break;
                case Opcao.Atualizar:
                    Console.WriteLine("Editado");
                    break;
                default:
                    Console.WriteLine("Opcao Invalida");
                    break;
            }
            Console.ReadLine();
            
        }
    }
}











