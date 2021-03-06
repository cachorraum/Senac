**# Senac**
Curso Desenvolvimento de Aplicativos Móveis

Usando **DART** e **FLUTTER**

##Aula 1 - Variáveis

Espaço reservado em memória para armazenar um valor temporarioamente.

###Tipos de Variáveis
- **string** -textos
- **int** -numeros inteiros
- **double** - numeros decimais

```
void(){
String nome = "Boaz";
int idade = 17;
double altura = 1,79
}

###Exemplo 2 - cálculo simples
```
void main() {
//Criar variaveis para nome,sobrenome,email e ano de nascimento,calcular a idade e mostrar ao final uma msg com todos esses dados.
  
  String nome,sobrenome,email;
    nome = "Boaz";
  sobrenome = "Matheus";
  email = "bmmb3004@gmail.com";
  
  print("Nome $nome");
  print("Sobrenome: $sobrenome");
  print("Email: $email");
  
  int ano_de_nascimento = 2002;
  
  ano_de_nascimento = 2019-2002;
    
  print("Idade $ano_de_nascimento");
  
  // \n= quebra de linha
   }
   
##Aula 2

**${renda_pessoa.toStringAsFixed(2)}**

O método toStringAsFixed() foi usado para formatar as casas(2) decimais da variável (renda_pessoa) double.
```dart
void main() {
String nome, sobrenome ,email, senha, cpf, endereco, sexo, celular, curso, nome_social;

int ano_nasc, idade, qtd_moradores;

double renda_familiar, renda_pessoa;

  
nome = "Boaz Matheus";
sobrenome = "Morais Benevides";  
email = "boazmmbenevides@gmail.com";
senha = "****";
cpf = "123456789";
endereco = "Rua Joaquim Jose de Oliveira Sobrinho";
sexo = "masculino";
curso = "Programador de Dispositivos Móveis";
nome_social = "";
celular = " (19)997710533";

  
ano_nasc = 2002;
idade = 2019 - ano_nasc;
qtd_moradores = 3;

renda_familiar = 213000;
renda_pessoa = renda_familiar / qtd_moradores; 

  
print("***************");
print("Seus dados estão corretos?");
print("***************");

  
print("Nome:$nome $sobrenome");
if(nome_social!="")
{  
print("Nome Social: $nome_social");
} 
print("Email: $email");
print("Sexo: $sexo");
print("Celular: $celular");
print("Ano de Nascimento: $ano_nasc");
print("Idade: $idade");
print("Cpf: $cpf");
print("Endereço: $endereco");

  
print("***************");
print("Informações SENAC");
print("***************");

 
print("Curso: $curso");
print("Renda Familiar: $renda_familiar");
print("Quantidade De Moradores: $qtd_moradores");
print("Renda por pessoa: ${renda_pessoa.toStringAsFixed(2)}");
   
}
 ```

### Condição lógica IF

O IF serve para determinar se um bloco **deve** ou **nao** ser executado, pode-se dizer que sempre que for necessário **testar** algum valor usaremos o *if*.

### Operadores lógicos

- == *Igualdade*
- \>= *maior ou igual*
- <= *menor ou igual*
- \> *maior*
- < *menor*

### Sintaxe

```dart
if(teste_lógico)
{
  //faz isso se o teste for verdadeiro
}
else
{
  //faz isso se o teste for falso
}
```

### Exemplo if

```dart
void main() {
  
  String curso = "programador android";
  
if(curso == "programador android")
{
  print("Parabéns, você fez ótimas escolhas");
  }
  else
  {
    print("vacilão, aposto que você faz ADM.");
    }
    
}
       
    ```
    
```dart
void main() 
{
  
double nota1, nota2, media;
  
nota1 = 5;
nota2 = 4;

media = (nota1 + nota2) / 2;

if(media >= 5)
{
  print("Aprovado com média $media");
}
else
{
  print("Reprovado com média $media");
}
 
}

```
### AULA 3 - Lógica com DART

### Exemplo Usando If (Login e Equação de 2°º grau)

Foi importada a *biblioteca* **dart:math** para podermos usar fuções matemáticas como pôtencia e raiz quadrada,no exemplo abaixo foi usada a função **math.sqrt()** para calcular a raiz de delta.

 - Após a importação foi dado um "apelido" para chamar a função através da sintaxe **as** (dart:math as **math**)
 - Foram usados 2 if,o 1º para dar acesso através da palavra mágica "empty" e o 2º para fazer a equação.
 - Cada if tem seu próprio else, daí a importancia de *identar* , organizar o código com **TABS**
 
```dart
import 'dart:math' as math;
void main() {
	String palavra_magica;
  
  palavra_magica = "empty";
  
  if(palavra_magica == "empty")
  {
  	print("Exercício 1 - Bhaskara");
    
    double delta, a, b , c;
    a = 1;
    b = -10;
    c = 25;
    delta = (b * b) - 4 * a * c;
    print("DELTA = $delta");
    
    if(delta < 0)
    {
    	print("Nenhuma raiz real pq o delta é menor que zero.");
    }
    else
    {
      double raiz_q, x1, x2;
      //Raiz Quadrada
      raiz_q = math.sqrt(delta);
      print("A RAIZ DE DELTA = $raiz_q");
      x1 = (-b + raiz_q) / (2 * a);
      x2= (-b - raiz_q) / (2 * a);
      print("X1 = $x1");
      print("X2 = $x2");
      }
  }
  	else	
    {
 	print("Acesso negado, você não é Digno.");
      }
}
```
## if aninhado ou if encadeado

Quando temos mais do que 2 testes possíveis, é necessário alterar a estrutura e acrescentar um **else if** após o primeiro if.

```dart
if(teste)
{
//faz isso
}
else
{
//faz isso
}
else if
{
//nenhum dos anteriores
}
```

## Exemplo if else if
```dart
void main() {
  String cidade_natal;
  cidade_natal = "Paraná";
  
  if(cidade_natal.toLowerCase() == "são jõao da boa vista")
  {
    print("São Joanense");
  }
	else if(cidade_natal.toLowerCase() == "bahia")
  {
    print("Baiano");
  }
  else if(cidade_natal.toLowerCase() == "pernambuco")
  {
    print ("Pernambucano");
  }
  else if(cidade_natal.toLowerCase() == "minas gerais")
  {
    print ("Mineiro");
  }
  else if(cidade_natal.toLowerCase() == "paraná")
  {
    print("Paranaense");
  } 
  else
  {
    print("Cidade Não Cadastrada");
  }
  
}
```
### AULA 4 - Operador Lógico

**E (AND) &&**

*"Somente será VERDADE se todas as expressões forem VERDADE".*

**OU (OR) ||**

*"Somente será FALSO se todas as expressões forem FALSAS".*

**Se tiver que acertar tudo &&, se tiver que acertar 1 ||** 

### Exemplo Teste *"booleano"*
```dart
void main() {
  bool var_a, var_b;

  var_a = true;

  var_b = false;

  print((!var_a && var_a) || (var_b || !var_b));

  int numero = 10;

  if (var_a == var_b) {
    numero = 666;
  } else {
    numero = numero + 1;
  }
  print(numero);
}
```
### AULA 5
//Trabalhando com FUNÇÕES

```dart
void main() {
	print (" Minha Calculadora =) \n----------------------");
	
  
  double n1 = 10;
  double n2 = 5;
  
  //Essa é a chamada da função
 
   calcular(n1, n2, "+");
   calcular(n1, n2, "-");
   calcular(n1, n2, "*");
   calcular(n1, n2, "/");
  
}

/*
 * Como criar uma função:
 * 
 * Primeiro, colocamos o RETORNO da função (tipo)
 * Depois, colocamos o NOME da função
 * Depois do nome, colocamos os PARENTESES. Dentro dos parenteses, "podemos" colocar PARÂMETROS.(pode ter ou não)
 * Por ultimo, colocamos abertura e fechamentos de CHAVES.Dentro das chaves, vai o código da função.
 * 
 * IMPORTANTE: Só criar a função não serve para NADA.
 * A gente tem que CHAMAR essa função no main.
 */

	void calcular(double novoNumero1, double novoNumero2, String operacao){
  	print ("\nQuanto é $novoNumero1 $operacao $novoNumero2?");
    
    double resposta;
    
    if(operacao == "+"){
      resposta = novoNumero1 + novoNumero2;
    }else if(operacao == "-"){
      resposta = novoNumero1 = novoNumero2;
    }else if(operacao == "/"){
      resposta = novoNumero1 / novoNumero2;
    }else if(operacao == "*"){
      resposta = novoNumero1 * novoNumero2;
    }else{
      resposta = 0;
    }
     
  	print("O resultado é: $resposta"); 
  }
  ```
  ### Aula Flutter
  
  **Primeiro contato**
  
  Entrar em flutter.dev (ou flutter.io) e procurar o local para começar a utilizar o flutter (Get Startet)
  Seguir os passos de instalação,que constituem basicamente de:
   -Baixar o SDK do Flutter e colocá-lo na pasta "C:\src\flutter"
   -Baixar e instalar o Android Studio
   -Configurar o plugin do flutter no Android Studio
   -Rodar o commando "flutter doctor"no Prompt de Commando para certificar que esta tudo ok.
   
   **Criação do primeiro App**
   
   Regra nº1:**Nunca feche a maquina virtual**
   
   1. Abrir o Andrpoid Studio
   2. Abrir a Maquina Virtual ( emulador de android)
   3. Apertar no botão "Start new Flutter Project" (iniciar novo projeto do flutter)
   4. Escolher Aolicativo Flutter
   5. Colocar o nome do projeto, descrição, e o caminho do SDK.
   6. Nome da empresa (não mudou nada)
  
   


