# Fundamentos do C# #

- Linguagem de programação tipada, compilada e gerenciada
- Criada por Anders Hejlsbern em meados de 2001
- Principal linguagem da Microsoft
- Orientada a Objetos

## Linguagem e compiladores

 **Linguagem interpretada x compilada**
Linguagens compiladas são traduzidas para código de máquina uma única vez, antes da execução, enquanto linguagens interpretadas são traduzidas linha por linha durante a execução
 O C# é compilado inicialmente para IL (Intermediate language)

## .NET Framework
 - C# é a linguagem
 - O framework se chama .net iniciou em 2001
 - Primeira versão foi chamada de .net Framework
 - Pode ser intalado side-by-side

## .NET Core
 - Versão moderna do .NET framework
 - Lancado em 2015
 - Suporte para Linux/Windows e Mac
 - Core significa núcleo, ou seja o essencial
 
## .NET Standard
 - Junção do sistema legado .NET Framework e sistema novo .NET Core
 - Ele irá garantir os 2 rodarem no mesmo projeto
 - Não é um Framework
 
## .NET
- Unificação dos Framework
- Agora é somente .NET

## Versionamento
 - Alpha, beta, release Candidate, final
 - Dividia em três partes:
  - Major, Minor, Patch

**Major:** Pode conter incompatibilidade com versões anteriores e são Breaking Changes
**Minor:** Possui mudanças mas é totalmente compatível com versões anteriores e são Backward Compatibility
**Patch:** Correções de bugs e outros itens simples

**Alpha**: 0.0.1-a1
**Beta:** 0.0.2-b1
**Release Candidate:** 1.0.0-rc1
**Final:** 1.0.0
Normalmente alpha e beta tem versões menores que 1.0.0

## Runtime e SDK
- Runtime executa e SDK Cria

## Instalação
- dotnet --version
- dotnet --list-sdk
- dotnet --list-runtimes
- dotnet help
- dotnet build
- dotnet restore = baixar dependencias
- dotnet clean = Limpar a aplicação
- dotnet run = Excutar a aplicação

## dotnet cli (novo projeto)
- dotnet new console = Novo Console Application
- dotnet classlib = Nova Class Library
- dotnet web = Novo projeto ASP.NET Core
- dotnet webapi = Novo projeto ASP.NET Core
- dotnet mvc = Novo projeto ASP.NET Core
- dotnet mstest = Novo projeto Microsoft Test

## Definições
- Importações
- Namespace = São divisões logicas
- Classe
- Método principal

## Variáveis
- No C# o tipo vem sempre antes do nome da variável, inicie com letra minuscula, padrão camel-case.
**exemplo:** 
int idade;
int idade = 25
var idade = 25
var suaIdade = 25

## Constantes
Boas praticas usar em maiúsculo.
const int IDADE_MINIMA;
const int IDADE_MINIMA = 25;

## Comentários
 // comentar linha
 /***** Comentar bloco ***/
 
## Tipos primitivos (built-in types)
- São chamados como Tipos de valor
- Armazeam o valor e não a referência para um item na memória
- São Classificados em:
	- Tipos Simples (simple Types)
	- Estruturas (structs)
	- Tipos Nulos (Nullable Types)

## Byte
- byte (8-bit) = 0 até 255
- Sbyte (8-bit) -128 até 127

## Inteiros
- long
- int

## Reais
- float = float salario = 2.500f
- double = sem anotação no final do valor
- decimal = decimal salario = 25.000m

## Boolean
bool =  bool usuarioCadastrado = true

## char
- Utilizado para armazenar apenas um caractere no formato Unicode
- Definido pela palavra reservada **char**
- aspas simples para usar o char

## String 
string primeiraLetra = "teste";
var primeiraLetra = "teste"

## Var
- Substitui o nome de um tipo
- Será do tipo do primeiro valor atribuidoo
var idade = 25  // será do tipo int
var nome = "Vini"  // será do tipo string

## Null
- Significa vazio, nada
- Diferente de zero ou uma string vazia
- Todo tipo, primitivo ou complexo pode receber o valor null
- O tipo deve ser marcado como Nullable Type
- Sempre colocar o ? pós tipo da variável
Exemplo:
int? idade = null;

## Valores Padrões
Todo tipo built-in ja possui valor padrão:
- int = 0
- float = 0
- decimal = 0
- bool = 0
- char = '\0'
- String = ""

## Conversão implícita
- Podem ser executadas apenas como passagem de dados
- Possuem tipos compatíveis
float valor = 25.8f;
int outro = 25;
valor = outro; 
// conversão implícida, ao contrario não daria certo, por que nã conseguimos colocar inteiro em um numero real

## Conversão explícita
- Ocorre quando os tipos não são compatíveis
- É dada pelo uso doo tipo entre parênteses antes da atribuição
- Segue as mesma regras anteriores
int inteiro = 100;
uint inteiroSemSinal = (uint)inteiro; // conversão explícida

## Parse
- Usado para converter um caractere ou string para um tipo qualquer
- Caso haja alguma incompatibilidade, gera um erro
int inteiro = int.Parse("100");

## Convert
- Simular ao parse
- Porém permite converter vários tipos de valor, não apenas string
- Devemos informar o tipo na chamada da conversão
int inteiro = Convert.ToInt32("100");

## Operadores de comparação

== igual

!= difetente

## Structs (estruturas)
- Tipo de dado estruturado
- Estruturar bem nossos tipos
- Value Type	
- Apenas estrutura, o esqueleto
- Tipo de valor
- Armazenam outros tipos de dados
- Definido pela palavra Struct
- Composto de propriedades e métodos
- Nome sempre com maiusculo (O mesmo para propriedades e métodos)
- Criado a partir 	da palavra new (Nesse momento sim teremos os valore)

